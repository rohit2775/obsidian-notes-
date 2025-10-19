
### **1. Basic Data Types**

``let age: number = 20; 
let name: string = "Rohit";
let isStudent: boolean = true; 
console.log(`Name: ${name}, Age: ${age}, Student: ${isStudent}`);

### **. Any Type**

`let value: any = 42; 
value = "Now it's a string!";
value = { key: "value" }; 
console.log(value);`


### **3. Array Type**

`let scores: number[] = [90, 85, 100];
let fruits: Array<string> = ["Apple", "Banana", "Mango"];  
console.log(scores[1]); 

4. Tuple Type 

let person: [string, number, boolean] = ["Rohit", 20, true];  
console.log(`Name: ${person[0]}, Age: ${person[1]}, Student: ${person[2]}`);

5. Enum Type

enum Direction {   Up,   Down,   Left,   Right }  
let move: Direction = Direction.Left; 
console.log(move); 