# Moore Machine Debugger, Runner, and Editor
FIT BUT - ICP Project

## Overview
This repository contains a finite state machine (FSM) project focused on Moore machines.  
It includes:
- a core C++ backend for FSM creation, validation, execution, and serialization,
- a Qt-based graphical editor for building and inspecting machines,
- tests and example programs.

## Disclaimer
This repository is published for academic presentation and reference only.  
Submitting this code (or parts of it) as your own course work may violate academic rules.

## Project Layout
- `src/core/` - core FSM implementation and API layer
- `src/gui/` - Qt GUI editor (`Automata_Editor`)
- `tests/` - current test framework and test suites
- `tests-old/` - legacy tests kept for reference
- `examples/` - example usage programs
- `assets/` - generated files (for example DOT output)
- `docs/` - project documentation
- `lib/` - bundled third-party headers/libraries

## Requirements
- C++ compiler with modern standard support
- Qt development libraries:
  - Qt 5 for the root `Makefile` workflow
  - Qt 6 for the `src/gui/CMakeLists.txt` workflow
- `make`
- `cmake` (for GUI build in `src/gui`)

## Build and Run (Makefile Workflow)
From repository root:

```bash
# Build backend executable
make

# Build everything (backend, examples, tests)
make build_all

# Build and run FSM tests
make test

# Build and run examples
make examples
./build/examples/fsm_interface_example
```

Main targets:
- `core_backend` - backend executable
- `fsm_test_runner` - test runner used by `make test`
- `build/examples/*` - example binaries

## Build GUI (CMake Workflow)
The GUI has its own CMake project under `src/gui`:

```bash
cd src/gui
cmake -S . -B build
cmake --build build
./build/Automata_Editor
```

## Testing
Current tests are organized around the custom framework in `tests/`, with `tests/fsm_test_runner.cpp` as entry point.

```bash
make test
```

For framework details, see:
- `tests/TEST_GUIDE.md`

## Author
Adam Taha
