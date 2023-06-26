# go-brainfuck

This is a Brainfuck interpreter written in Go. Brainfuck is an esoteric programming language known for its minimalistic and Turing-complete design. The interpreter provides functionality to run Brainfuck code and produce output.

## Usage

The Brainfuck interpreter provides a `Run` function that takes two parameters: the Brainfuck code as a string and the input as a byte array. It returns the output generated by the code as a byte array.

Here's an example of how to use the interpreter:

```go
package main

import (
	"fmt"
	"github.com/lookharm/go-brainfuck"
)

func main() {
	code := "++++++++[>++++[>++>+++>+++>+<<<<-]>+>+>->>+[<]<-]>>.>---.+++++++..+++.>>.<-.<.+++.------.--------." // Example Brainfuck code
	input := []byte{} // Example input

	output := path.Run(code, input)

	fmt.Println("Output:", string(output)) // Hello, World!\n
}
```

## Supported Operations

The interpreter supports the following Brainfuck operations:

| Character | Description                               |
|-----------|-------------------------------------------|
| `>`       | Increment the data pointer                 |
| `<`       | Decrement the data pointer                 |
| `+`       | Increment the byte at the data pointer     |
| `-`       | Decrement the byte at the data pointer     |
| `.`       | Output the byte at the data pointer        |
| `,`       | Input a byte and store it at the data pointer |
| `[`       | Jump forward to the corresponding `]` if the byte at the data pointer is zero |
| `]`       | Jump back to the corresponding `[` if the byte at the data pointer is non-zero |

Any other characters in the code will be ignored.

## License

This code is licensed under the [MIT License](https://opensource.org/licenses/MIT). Feel free to use and modify it according to your needs.

## Acknowledgements

The Brainfuck interpreter was developed by Woradorn L.