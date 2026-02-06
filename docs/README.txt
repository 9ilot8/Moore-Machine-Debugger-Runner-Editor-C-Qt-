MOORE MACHINE DEBUGGER, RUNNER, AND EDITOR
FIT BUT - ICP Project

OVERVIEW
This repository implements a finite state machine system focused on Moore machines.
It includes:
- a C++ backend for FSM construction, validation, execution, and JSON persistence,
- a Qt GUI editor for interactive FSM creation and inspection,
- tests and example programs.

DISCLAIMER
This repository is public for academic reference and presentation purposes.
Using this code (or parts of it) as your own coursework may violate academic rules.

PROJECT STRUCTURE
- src/core/      Core FSM implementation and interface
- src/gui/       Qt GUI editor (Automata_Editor)
- tests/         Current test framework and test suites
- tests-old/     Legacy tests kept for reference
- examples/      Example programs using the backend
- assets/        Generated assets (for example DOT files)
- docs/          Documentation files
- lib/           Third-party libraries bundled with the project

REQUIREMENTS
- Modern C++ compiler
- Qt development libraries
  - Qt 5 for root Makefile workflow
  - Qt 6 for src/gui CMake workflow
- make
- cmake (for GUI build)

BUILD AND RUN (MAKEFILE WORKFLOW)
Run from repository root:

1) Build backend executable
   make

2) Build backend + examples + tests
   make build_all

3) Build and run tests
   make test

4) Build examples
   make examples

5) Run interface example
   ./build/examples/fsm_interface_example

Main binaries/targets:
- core_backend
- fsm_test_runner
- build/examples/*

BUILD GUI (CMAKE WORKFLOW)
The GUI project is in src/gui:

cd src/gui
cmake -S . -B build
cmake --build build
./build/Automata_Editor

TESTING
The current test entry point is:
- tests/fsm_test_runner.cpp

Run tests with:
- make test

More test framework details:
- tests/TEST_GUIDE.md

AUTHOR
Adam Taha
