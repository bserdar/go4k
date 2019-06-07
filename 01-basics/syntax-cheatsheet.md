# Syntax Cheat-Sheet

Declare a function, no input/output:

```
func myFunction() {
}
```

Declare a function with inputs, one output:

```
func myFunction(input1 int,input2 int) int {
  ...
  return output
}
```

Declare a function with multiple inputs/outputs:

```
func myFunction(input1 int,input2 int) (int,int) {
  ...
  return output1, output2
}
```

Declare a variable

```
var myVariable int
```

Assign a value to a variable

```
myVariable = 1
```

Conditionals:

```
if myVariable == 1 {
  // Here, myVariable is 1
} else {
  // Here, myVariable is not 1
}
```


```
if myVariable > 2 {
}
```


Loops:

```
var index int

for index=0; index < 5; index++ {
  // This block will execute 10 times
  // At each iteration, index will be different
  //  0, 1, 2, 3, 4
  // When index == 5, the loop will terminate
  // and execution continue
}
```
