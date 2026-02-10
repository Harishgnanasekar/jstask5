## TASK 1 – Employee Merge System (Spread Operator)

**Code:**

```js
let empBasic = { name: "Naveen", role: "Trainee", salary: 20000 };
let empPromotion = { role: "Developer", bonus: 10000 };

let finalEmployee = {
  ...empBasic,
  ...empPromotion,
  salary: 40000,
  experience: "2 years"
};

console.log(finalEmployee);
```

**Final Output:**

```js
{
  name: "Naveen",
  role: "Developer",
  salary: 40000,
  bonus: 10000,
  experience: "2 years"
}
```

---

## TASK 2 – Shopping Cart (Spread + Array)

**Code:**

```js
let cart1 = ["Shoes", "Shirt"];
let cart2 = ["Watch", "Cap"];

let finalCart = ["Socks", ...cart1, ...cart2, "Bag"];

console.log(finalCart);
```

**Final Output:**

```js
["Socks", "Shoes", "Shirt", "Watch", "Cap", "Bag"]
```

---

## TASK 3 – Rest Operator Salary Calculator

**Code:**

```js
function calculateTotalSalary(baseSalary, ...bonuses) {
  let bonusSum = 0;

  for (let bonus of bonuses) {
    bonusSum += bonus;
  }

  return baseSalary + bonusSum;
}

let totalSalary = calculateTotalSalary(30000, 2000, 3000, 5000);
console.log("Total Salary:", totalSalary);
```

**Final Output:**

```text
Total Salary: 40000
```

---

## TASK 4 – Advanced Destructuring

**Code:**

```js
let student = {
  name: "Rahul",
  marks: {
    maths: 90,
    science: 85,
    english: 88
  }
};

let { name } = student;
let { maths, science } = student.marks;

console.log(name + " scored " + maths + " in maths and " + science + " in science");
```

**Final Output:**

```text
Rahul scored 90 in maths and 85 in science
```

---

## TASK 5 – Array Manipulation

**Code:**

```js
let numbers = [10, 20, 30, 40, 50];

// Remove 30 and add 25
numbers.splice(2, 1, 25);

// Reverse the array
numbers.reverse();

// Check if 50 exists
let result = numbers.includes(50);

console.log("Final Array:", numbers);
console.log("50 exists:", result);
```

**Final Output:**

```js
Final Array: [50, 40, 25, 20, 10]
50 exists: true
```

---

## TASK 6 – Flatten Data

**Code:**

```js
let apiData = [1, 2, [3, 4, [5, 6, [7, 8]]]];

let flatArray = apiData.flat(Infinity);

console.log(flatArray);
console.log("Index of 6:", flatArray.indexOf(6));
```

**Final Output:**

```js
[1, 2, 3, 4, 5, 6, 7, 8]
Index of 6: 5
```

---

## TASK 7 – Sorting Problem

**Code:**

```js
let prices = [100, 5, 25, 300, 45];

// Ascending order
let ascendingOrder = prices.slice().sort((a, b) => a - b);

// Descending order
let descendingOrder = prices.slice().sort((a, b) => b - a);

console.log("Ascending:", ascendingOrder);
console.log("Descending:", descendingOrder);
```

**Final Output:**

```js
Ascending: [5, 25, 45, 100, 300]
Descending: [300, 100, 45, 25, 5]
```

---

## BONUS HARD TASK – Team Level

**Code:**

```js
let users = [
  { name: "A", salary: 20000 },
  { name: "B", salary: 40000 },
  { name: "C", salary: 30000 }
];

// Increase salary and sort high to low
let updatedUsers = users
  .map(user => ({
    ...user,
    salary: user.salary + 5000
  }))
  .sort((a, b) => b.salary - a.salary);

console.log(updatedUsers);
```

**Final Output:**

```js
[
  { name: "B", salary: 45000 },
  { name: "C", salary: 35000 },
  { name: "A", salary: 25000 }
]
```

---




