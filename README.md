# gpioIrq
Example of using sysfs for edge detection interrupts on the Omega's GPIOs.

## Compilation

In order to run this program on the Omega2, it must first be compiled for the MIPS architecture.

The available options:

* Since this program does not use any external libraries, it can be compiled directly on the Omega. See the Onion Documentation for [Compiling C programs on the Omega](https://docs.onion.io/omega2-docs/c-compiler-on-omega.html)
* It can also be cross-compiled using the LEDE build system, see the Onion Documentation for [Cross-Compilation for the Omega](https://docs.onion.io/omega2-docs/cross-compiling.html) for more details

Both methods will work, it is up to the user.

## Usage

The executable is meant to be run with an argument that identifies the GPIO pin which is to be monitored for a change in the voltage level (an edge):

```
./gpioIrq <GPIO-Number>
```

To test this program, run it and try using a jumper wire to connect the selected GPIO to `GND` and then `3.3V`. Monitor the output of the program and observe what happens.
