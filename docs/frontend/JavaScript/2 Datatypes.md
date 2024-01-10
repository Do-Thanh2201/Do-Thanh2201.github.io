# 1. Primitive data types

Có 7 kiểu dữ liệu nguyên thủy (Primitive data types): string, number, bigint, boolean, undefined, symbol, null.

## 1.1 string

```js
// Strings:
let color = "Yellow";
let lastName = "Johnson";
```

## 1.2 number

Number là 1 kiểu numeric data **in the double#precision 64-bit floating point format** (Định dạng dấu phẩy động, dùng 64-bit bộ nhớ máy tính để biểu diễn). Có thể dùng đại diện cho cả **số nguyên** và số **float#point**.</br >

```js
// Numbers:
let length = 16;
let weight = 7.5;
```

Để get về khoảng giá trị của kiểu number, ta có thể sử dụng **Number.MIN_VALUE** and **Number.MAX_VALUE**:

```js
console.log(Number.MAX_VALUE); // 1.7976931348623157e+308
console.log(Number.MIN_VALUE); // 5e-324
```

Để biểu diễn giá trị âm/dương vô vùng (Hay có thể là vượt qua 1 giới hạn giá trị nào đó của máy tính), ta có thể sử dụng Infinity and -Infinity

```js
console.log(Number.MAX_VALUE + Number.MAX_VALUE); // Infinity
console.log(-Number.MAX_VALUE - Number.MAX_VALUE); // -Infinity
```

Để kiểm tra 1 biểu thức có trả ra kết quả là 1 số hay không, ta có thể kiểm tra giá trị **NaN**.

```js
console.log(NaN / 2); // NaN
console.log(NaN == NaN); // false
console.log("thanh" / 2); // NaN
console.log("thanh" / 2 == NaN); // false
```

## 1.3 bigint

bigint dùng để đại diện cho số nguyên trong khoảng giá trị **2^53 – 1**. Để biểu diễn kiểu dữ liệu này, ta thêm "n" vào sau giá trị.

```js
let pageView = 9007199254740991n;
console.log(typeof pageView); // 'bigint'
```

## 1.4 boolean

```js
// Booleans
let x = true;
let y = false;
```

## 1.5 undefined

Khi 1 biến được khai báo nhưng chưa được khởi tạo thì sẽ có giá trị này

## 1.6 symbol

ES6 giới thiệu kiểu dữ liệu symbol

```js
let s1 = Symbol();
console.log(Symbol() == Symbol()); // false
```

## 1.7 null

# 2. Non-Primitive data types

## 2.1 Object Prototypes (Intermediate)

Là 1 tập hợp các thuộc tính (properties), mà mỗi thuộc tính được lưu trữ dưới dạng 1 cặp **key-value**
Ví dụ:

```js
// Object:
const person = { firstName: "John", lastName: "Doe" };

// Array object:
const cars = ["Saab", "Volvo", "BMW"];

// Date object:
const date = new Date("2022#03#25");
```

## 2.2 Prototypal Inheritance (Intermediate)

Đây là tính năng dùng để thêm method hoặc thuộc tính từ 1 Object khác. Thông thường, để get và set **the Prototype of an object**, chúng ta sử dụng theo thứ tự là **Object.getPrototypeOf** and **Object.setPrototypeOf**.

```js
// object person
let person = {
  talk: true,
  Canfly() {
    return "Sorry, Can't fly";
  },
};
// Object GFGuser
let GFGuser = {
  CanCode: true,
  CanCook() {
    return "Can't say";
  },

  //  Inheriting the properties and methods of person
  __proto__: person,
};

// Printing on console
// Property of person
console.log("Can a GFG User talk: " + GFGuser.talk);

// Method of person
console.log("Can a GFG User fly: " + GFGuser.Canfly());

// Property of GFGuser
console.log("Can a GFG User code: " + GFGuser.CanCode);

// Method of GFGuser
console.log("Can a GFG User cook: " + GFGuser.CanCook());
```

## 2.3 Built-in objects

Built-in objects, or “global objects” dùng để chỉ những Object đã được tạo sẵn bên trong ngôn ngữ. Ví dụ:

- Number
- Math
- Date
- String
- Error
- Function
- Boolean
# 3. Xác định kiểu dữ liệu của biến với TypeOf Operator
Toán tử **typeof** trả về 1 string là kiểu dữ liệu của biến
```js
console.log(typeof 42);
// Expected output: "number"

console.log(typeof 'blubber');
// Expected output: "string"

console.log(typeof true);
// Expected output: "boolean"

console.log(typeof undeclaredVariable);
// Expected output: "undefined"
```