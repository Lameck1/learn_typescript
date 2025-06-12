# Typescript: Assigning Types, Type Inference, and Literal Types

## Assigning Types

```typescript
let myString: string = "Hello, TypeScript!";
let myNumber: number = 42;
let myBoolean: boolean = true;
let myArray: string[] = ["apple", "banana", "cherry"];
let myTuple: [string, number] = ["TypeScript", 3.9];
let myObject: { name: string; age: number } = { name: "Alice", age: 30 };
```

## Type Inference

```typescript
let inferredString = "This is inferred as a string";
let inferredNumber = 100; // Inferred as number
let inferredBoolean = false; // Inferred as boolean
let inferredArray = [1, 2, 3]; // Inferred as number[]
let inferredTuple = ["inferred", 42]; // Inferred as [string, number]
let inferredObject = { key: "value", count: 10 }; // Inferred as { key: string; count: number }
```

## Literal Types

```typescript
const a = 42; // Literal type number
const b = "Hello"; // Literal type string
const c = true; // Literal type boolean
type Direction = "up" | "down" | "left" | "right"; // Literal type union
let move: Direction = "up"; // Valid assignment
let invalidMove: Direction = "forward"; // Error: Type '"forward"' is not assignable to type 'Direction'
```

## Type Assertions

```typescript
let someValue: any = "This is a string";
let strLength: number = (someValue as string).length; // Using 'as' syntax
let anotherStrLength: number = (<string>someValue).length; // Using angle-bracket syntax
```

## Type Aliases

```typescript
type Point = { x: number; y: number };
let point: Point = { x: 10, y: 20 };
type StringOrNumber = string | number;
let value: StringOrNumber = "Hello"; // Valid
value = 100; // Also valid
```

## Enums

```typescript
enum Color {
    Red = "RED",
    Green = "GREEN",
    Blue = "BLUE"
}
let myColor: Color = Color.Green; // Valid assignment
let invalidColor: Color = "YELLOW"; // Error: Type '"YELLOW"' is not assignable to type 'Color'
```

## Interfaces

```typescript
interface User {
    name: string;
    age: number;
    isActive: boolean;
}
let user: User = {
    name: "Bob",
    age: 25,
    isActive: true
};
interface Point3D extends Point {
    z: number; // Extending the Point interface
}
let point3D: Point3D = { x: 1, y: 2, z: 3 }; // Valid assignment
```
