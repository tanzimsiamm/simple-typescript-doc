# TypeScript Documentation

## Introduction
TypeScript is a strongly typed, object-oriented, compiled language that builds on JavaScript. It is developed and maintained by Microsoft. TypeScript compiles to plain JavaScript, which can run anywhere JavaScript runs.

## Why Use TypeScript?
- **Static Typing:** Helps catch errors during development.
- **Improved Code Readability:** Type annotations make code easier to understand.
- **Better IDE Support:** Provides autocompletion, inline documentation, and error detection.
- **Object-Oriented Features:** Supports classes, interfaces, and modules.
- **Compatibility:** Works with JavaScript and existing JavaScript libraries.

---

## Installation
To install TypeScript globally, use:
```sh
npm install -g typescript
```
To check if TypeScript is installed:
```sh
tsc --version
```

---

## Setting Up a TypeScript Project
Initialize a TypeScript project with:
```sh
tsc --init
```
This creates a `tsconfig.json` file to configure TypeScript.

To compile a TypeScript file:
```sh
tsc filename.ts
```
This generates a `filename.js` file.

---

## Basic Syntax
### Variables (Defining static types)
```ts
let age: number = 25;
let username: string = "Siyam";
let isDeveloper: boolean = true;
```

### Functions (Defining parameter and return types)
```ts
function add(a: number, b: number): number {
    return a + b;
}
```

### Arrays (Defining typed arrays)
```ts
let numbers: number[] = [1, 2, 3, 4];
let names: string[] = ["Alice", "Bob"];
```

### Tuples (Fixed-length arrays with specific types)
```ts
let user: [string, number] = ["Alice", 25];
```

### Enums (Defining named constants)
```ts
enum Role {
    Admin,
    User,
    Guest
}
let myRole: Role = Role.Admin;
```

### Interfaces (Defining object structures)
```ts
interface User {
    name: string;
    age: number;
}
let user: User = { name: "Siyam", age: 20 };
```

### Classes (Object-oriented programming in TypeScript)
```ts
class Person {
    name: string;
    constructor(name: string) {
        this.name = name;
    }
    greet() {
        console.log(`Hello, my name is ${this.name}`);
    }
}
let person = new Person("Siyam");
person.greet();
```

### Generics (Reusable functions with different types)
```ts
function identity<T>(value: T): T {
    return value;
}
let output = identity<string>("Hello");
```

### Type Aliases (Creating custom types)
```ts
type ID = string | number;
let userId: ID = "123";
```

### Union and Intersection Types (Combining multiple types)
```ts
let value: string | number; // Union type

interface A {
    propA: string;
}
interface B {
    propB: number;
}
type AB = A & B; // Intersection type
let obj: AB = { propA: "Hello", propB: 42 };
```

### Modules (Splitting and importing code)
```ts
// file: math.ts
export function add(a: number, b: number): number {
    return a + b;
}

// file: main.ts
import { add } from "./math";
console.log(add(2, 3));
```

---

## TypeScript with React
To use TypeScript in a React project:
```sh
npx create-react-app my-app --template typescript
```

### Defining props in React components
```tsx
interface ButtonProps {
    text: string;
    onClick: () => void;
}
const Button: React.FC<ButtonProps> = ({ text, onClick }) => {
    return <button onClick={onClick}>{text}</button>;
};
```

---

## TypeScript Configuration (`tsconfig.json`)
Some important options:
```json
{
  "compilerOptions": {
    "target": "ES6",
    "module": "CommonJS",
    "strict": true,
    "outDir": "./dist",
    "rootDir": "./src"
  }
}
```

---

## Conclusion
TypeScript enhances JavaScript by adding static typing and other powerful features. It improves code maintainability and reduces runtime errors. Learning TypeScript can greatly benefit web developers.

For more details, visit the [official TypeScript documentation](https://www.typescriptlang.org/docs/).

---

Happy Coding! 🚀

