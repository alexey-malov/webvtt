[![Build Status](https://travis-ci.org/alexa/webvtt.svg?branch=master)](https://travis-ci.org/alexa/webvtt)

# libwebvtt
A C/C++ library for interpreting and authoring conformant [WebVTT](https://www.w3.org/TR/webvtt1/) content. WebVTT is a
caption and subtitle format designed for use with HTML5 audio and video elements. This project is a fork of 
[caitp/webvtt](https://github.com/caitp/webvtt).

## Build Instructions:

[CMake](https://cmake.org/) is used for running the builds and tests. When using CMake, it's recommended that builds 
take place outside of the main project source, such as in a `build` directory.


### Building and Running the `parsevtt` Sample Program

```bash
# assuming the current working directory is the project directory
cd build

# configure the project with CMake
cmake ..

# compile the test executable
make

# Run the sample executable with a WebVTT file as input,
# using the -f argument to point to the file location.
src/parsevtt/parsevtt -f ../test/webvtt_example.vtt
```

Once built, the static library and include files are available at these locations:

#### For C
* Static library: `build/src/webvtt/libwebvtt.a`
* Include: `include/webvtt`

#### For C++
* Static library: `build/src/webvttxx/libwebvttxx.a`
* Include: `include/webvttxx`


## Running Tests:

All tests are written using [Google Test](https://github.com/google/googletest).

```bash
# assuming the current working directory is the project directory
cd build

# configure the project with CMake
cmake ..

# compile the test executable
make all test

# run the test executable
test/unit/unittests
```

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/alexa/webvtt/tags). 


## License

This project is licensed under the 2-Clause BSD License - see the [LICENSE](LICENSE) file for details.


## Acknowledgments

This project was originally the work of these individuals: Ralph Giles, Caitlin Potter, Rick Eyre, Edwin Lim, Dale Karp, 
Michael Afidchao, Shayan Ahmad, Jordan Raffoul, David Humphrey, Vince Lee, Mandeep Garg, Anh Tran, 
Thevakaran Virutthasalam, Mike Shutov, Michael Stiver-Balla, Kyle Barnhart, and David Perit. Many thanks to these people
for their efforts!
