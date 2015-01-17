# LTOWrapper

Wrap calls to GCC toolchain to enable Link Time Optimization (LTO) duration compilation.

## Why LTOWrapper?

Some Makefiles have hard-coded `ar` and `ranlib` configuration, while GCC requires `gcc-ar` and `gcc-ranlib` to make LTO work.

LTOWrapper can redirect calls to `ar` to `gcc-ar` so that LTO works even with hard-coded Makefiles.

## Usage

LTOWrapper works on Linux. Make sure that `ar` `nm` `ranlib` `gcc` `g++` are installed on your system.

Then type `./activate`.

It will start a new shell (by default, bash). When you type something like `ar` in the new shell, `gcc-ar` will be actually invoked. 

When you finished, type `exit`.

## Support for Clang/BSD/OS X?

I am not sure how to do that. If you managed to get it work, please contribute to this project by sending a pull request at GitHub.

Use it as your own risk if you want to use LTOWrapper on any other platform than Linux with GCC toolchain.

## License

This program is licensed under MIT license. Refer to the file `COPYING` for more details.
