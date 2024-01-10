# 1. Variable Declaration

## 1.1 var

Dùng để khai báo với 1 biến thuộc **function-scoped** or **globally-scoped** variables.</br >
Biến khai báo với **var** có thể được khai báo lại.

```js
/*==============================*/
var var1 = 23;
console.log(var1); // Output: 23
var var1 = "thanh";
console.log(var1); // Output: thanh
/*==============================*/
function hoist() {
  a = 20;
  var b = 100;
}

hoist();

console.log(a);
/* 
Accessible as a global variable outside hoist() function
Output: 20
*/

console.log(b);
/*
Since it was declared, it is confined to the hoist() function scope.
We can't print it out outside the confines of the hoist() function.
Output: ReferenceError: b is not defined
*/
```

## 1.2 let

Dùng để khai báo các biến cục bộ, thuộc **block-scoped** local variables.
Biến khai báo với **let** không thể được khai báo lại, nhưng cho phép thay đổi giá trị của biến.

```js
let greeting = "say Hi";
console.log(greeting); //"say Hi"

greeting = "say Hello instead";
console.log(greeting); //"say Hello instead"

let greeting2 = "say Hi";
let greeting2 = "say Hello instead"; // error: Identifier 'greeting' has already been declared
```

## 1.3 const

Dùng để khai báo các biến cục bộ, thuộc **block-scoped** local variables.</br >
Trong biến **const** nếu trường hợp kiểu của biến là **primitive** (bao gồm string, number, boolean, null, và undefined) thì chúng ta sẽ không thể tái khai báo hay cập nhật giá trị mới để thay thế cho giá trị trước đó của biến.</br >

```js
const greeting = "say Hi";
greeting = "say Hello instead"; // error : Assignment to constant variable.

const greeting2 = "say Hi";
const greeting2 = "say Hello instead"; // error : Identifier 'greeting' has already been declared
```

# 2. Hoisting

Tức là quá trình **trình thông dịch interpreter** di chuyển phần khai báo hàm, biến, class **lên đầu phạm vi của chúng** trước khi được thực hiện (Sử dụng trước khi khai báo).</br >

## 2.1 Hoisting variable

Chỉ biến khai báo bằng **var** mới có tính chất này.

Ví dụ 1:

```js
console.log(greeting);
var greeting = "say hello";
```

Đoạn code trên sẽ được biên dịch là:

```js
var greeting;
console.log(greeting); // greeting is undefined
greeting = "say hello";
```

Ví dụ 2:

```js
console.log(hoistLet); // Output: ReferenceError: hoistLet is not defined ...
let hoistLet = "The variable has been hoistLet.";

console.log(hoistConst); // Output: ReferenceError: hoistConst is not defined
const hoistConst = "The variable has been hoistConst.";
```

## 2.2 Hoisting functions

Chỉ **Function declaration** mới được Hoisting

```js
hoisted(); // Output: "This function has been hoisted."

function hoisted() {
  console.log("This function has been hoisted.");
}
```

Ví dụ 2 với function expressions

```js
var expression1 = function () {
  console.log("It is work OK");
};
expression1(); //Output: "It is work OK"

expression2(); //Output: "TypeError: expression2 is not a function

var expression2 = function () {
  console.log("Will this work?");
};
```

## 2.3 Hoisting classes

Trong ES6, class không được Hoisting.

# 3. Variable scopes

## 3.1 Block Level Scope
Biến được khai báo **bên trong bất kỳ block nào**, chẳng hạn như bên trong body của 1 function, hoặc câu lệnh **if/switch conditions or for/while loops** thì có Block Level Scope</br >
Tức là các biến chỉ được truy cập từ bên trong Block

```js
{
  let p = 110;
  const q = 111;
  var r = 1101;
}
console.log(r); // Output: 1101
console.log(p); // Uncaught ReferenceError: p is not defined
console.log(q); // Uncaught ReferenceError: q is not defined
```

## 3.2 Function Level Scope
Biến được khai báo **trong 1 functio**n thì có Function Level Scope</br >
Tức là các biến chỉ được truy cập từ bên trong function

```js
function printIfGFG(text) {
  if (text == "GeeksforGeeks" || text == "GFG") {
    var message = "Verified Geek";
    console.log(message); // Output: Verified Geek
  }
  console.log(message); // Output: Verified Geek
}
printIfGFG("GFG");
console.log(message); // Output: "ReferenceError: message is not defined"
```

## 3.3 Global Level Scope
Biến được khai báo ở Globally, tức là không khai báo bên trong bất kỳ function nào thì có **Global Scope**