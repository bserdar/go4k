# Basics 

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

