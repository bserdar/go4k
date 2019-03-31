# Basics 

You can run all the examples here on the Go playground:
https://play.golang.org/

Go programs start running at the "main" function in the "main"
package. This is a minimal go program:

```
package main

func main() {
}
```

A function, like "main" above, is a piece of code you can run using
its name. The following program prints out a number using the function
Println. Println is in a package called "fmt", and you have to impport
"fmt" to use the Println function:

```
package main

import "fmt"

func main() {
  fmt.Println(1)
}
```

You can call Println many times, with different things to print out.

```
package main

import "fmt"

func main() {
  fmt.Println(1+2)
  fmt.Println(1-2)
  fmt.Println(2*3)
  fmt.Println(10/5)
}
```

All the numbers in these programs are integers. An integer is a whole
number that can be positive or negative. You can use arithmetic
operators with integers. The result of an arithmetic operation on
integers is another integer. Because of this, if you divide two
integers, the result is an integer with decimals removed.


```
package main

import "fmt"

func main() {
  fmt.Println(10/3)
  fmt.Println(11/4)
}
```


You can create more functions yourself:

```
package main

import "fmt"

// Declare a function called "print1" that prints 1
func print1() {
  fmt.Println(1)
}

// Declare a function called "print2" that prints 2
func print2() {
  fmt.Println(2)
}

func main() {
  // Call print1. Program jumps to where print1
  // is declared, executes the statements, and
  //when print1 is complete, it comes back here
  // and continues with the next line
  print1()

  // Same thing with print2
  print2()
}
```

You can call functions from other functions:

```
package main

import "fmt"

func print1() {
  fmt.Println(1)
}

func print2() {
  fmt.Println(2)
}

func print1and2() {
  print1()
  print2()
}

func main() {
  print1and2()
}
```

You can send information to functions.

```
package main

import "fmt"

func print(number int) {
  fmt.Println(number)
}

func main() {
  print(1)
  print(2)
  print(3)
}
```

Above, the function "print" is called three times from main, once with
1, then with 2, then with 3. When "print" is running, the name
"number" has the value it is given at where it is called. The fist
time, number is 1. Second time it is called, number is 2. Third time
it is called, number is 3. Once "print" completes, the name "number"
is meaningless.

You can write a function that adds one to a number:

```
package main

import "fmt"

func add1(number int) {
  fmt.Println(number+1)
}

func main() {
  add1(1)
  add1(100)
}
```

Functions can get more than one input:

```
package main

import "fmt"

func add(number1 int, number2 int) {
  fmt.Println(number1+number2)
}


func main() {
  add(1,2)
  add(4,5)
  add(100,-200)
}
```

Here, "number1" and "number2" are the "arguments to the function add".


Functions can produce output.

```
package main

import "fmt"

func add(number1 int,number2 int) int {
   return number1+number2
}

func main() {
  fmt.Println(add(1,2))
  fmt.Println(add(10,-5))
}
```

Here, "number1" and "number2" goes into the function "add". "add"
computes the sum of the two numbers, and "returns" the result, which
is an "int". Then we print that result using "Println".

The above program runs like this:

 * main() starts running.
 * The first line is fmt.Println(add(1,2)). That means, it has to
   evaluate the function add(1,2) first, and send the result of that
   to fmt.Println.
 * "add" is called, with 1 and 2 as inputs
 * "add" is running with number1=1 and number2=2
 * "add" computes number1+number2, which is 3
 * "add" returns 3, we're back in main()
 * fmt.Println(3) is running
 * fmt.Println(3) runs, prints 3
 * Next line: fmt.Println(add(10,-5))
 * add(10,-5) needs to be evaluated first
 * "add" is called, with number1=10, number2=-5
 * "add" computes number1+number2, which is 5
 * "add" returns 5, we're back in main()
 * fmt.Println(5) is running
 * fmt.Println(5) runs, prints 5
 * main() returns, program ends
 