# Spin - An Efficient Logic Model Checker

[![License](https://img.shields.io/badge/License-BSD%203--Clause-blue.svg)](LICENSE)

## Overview

Spin is a widely-used formal verification tool for the analysis of concurrent systems. It can verify the correctness of distributed software models in a rigorous and automated fashion. The tool was originally developed by Gerard J. Holzmann at Bell Labs and is now maintained as an open-source project.

## Key Features

- **Efficient Model Checking**: Verifies correctness properties of concurrent system models
- **Promela Language**: Uses Process Meta Language (Promela) for system specification
- **Verification Modes**: Supports exhaustive verification, partial order reduction, bitstate hashing, and more
- **Property Specification**: Verifies safety, liveness, and temporal logic properties
- **Multi-Core Support**: Parallel verification algorithms for multi-core systems
- **Counterexample Generation**: Produces error traces when properties are violated
- **Interactive Simulation**: Allows step-by-step execution of models

## Getting Started

### Installation

#### From Source

```bash
git clone https://github.com/nimble-code/Spin.git
cd Spin/Src
make
sudo make install
```

#### Pre-built Binaries

Pre-built binaries for various platforms are available in the `Bin` directory.

### Basic Usage

1. Write a model in Promela:

```promela
/* hello.pml */
init {
    printf("Hello, world!\n")
}
```

2. Run a simulation:

```bash
spin hello.pml
```

3. Verify properties:

```bash
spin -a hello.pml    # Generate verifier
gcc -o pan pan.c     # Compile verifier
./pan                # Run verification
```

## Documentation

- [Online Manual](http://spinroot.com/spin/Man/)
- [Tutorials](http://spinroot.com/spin/Man/1_Exercises.html)
- [Examples](Examples/)

## Advanced Features

- **Swarm Verification**: Cloud-based verification for large state spaces
- **Bitstate Hashing**: Memory-efficient verification using Bloom filters
- **Partial Order Reduction**: Reduces state explosion by eliminating redundant interleavings
- **Breadth-First Search**: For finding shortest counterexamples
- **Bounded Context Switching**: Limits context switches for focused verification

## License

This project is licensed under the BSD 3-Clause License - see the [LICENSE](LICENSE) file for details.

## Citation

If you use Spin in your research, please cite:

```
@book{holzmann2004spin,
  title={The Spin Model Checker: Primer and Reference Manual},
  author={Holzmann, Gerard J},
  year={2004},
  publisher={Addison-Wesley Professional}
}
```

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.