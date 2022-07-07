#2i Code Test

Statement of Test Requirement:

“In a language of your choice, using all best practice principles you’re aware of, could you please provide code that iterates in multiples of A until X, then in multiples of A + 1 until 2X, then multiples of A + 2 until 3X. Please state any assumptions you’ve made. Please upload to a public Github repository and share the link.”

Notes:

-The Solution is written in Javascript.
-Assumptions are that parameters entered will be positive, non-zero integers and A is not to be multiplied by zero . This code will operate within Javascript's integer capabilities (I think).

~~~
console.log(multiples(checkA(), checkX()))
function checkA() {
  var A
  do {
    A = parseInt(prompt("Please enter a positive numeric, non-zero value for A"), 10)
  } while (!A || A < 0)
  console.log("You have entered A = " + A)
  return A
}
function checkX() {
  var X
  do {
    X = parseInt(prompt("Please enter a positive numeric, non-zero value for X"), 10)
  } while (!X || X < 0)
  console.log("You have entered X = " + X)
  return X
}
function multiples(A, X) {
  let resultX = []
  let result2X = []
  let result3X = []
  for (i = 1; i <= X; i++) {
    resultX.push(A * i)
  }
  for (j = 1; j <= 2 * X; j++) {
    result2X.push((A + 1) * j)
  }
  for (k = 1; k <= 3 * X; k++) {
    result3X.push((A + 2) * k)
  }
  console.log("Results for entered parameters" + " A = " + A + " and X = " + X)
  return [resultX, result2X, result3X]
}
~~~