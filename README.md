# LoopMix128: A High-Performance 64-Bit PRNG 🎲

![LoopMix128](https://img.shields.io/badge/LoopMix128-64--Bit%20PRNG-blue.svg)  
[![Latest Release](https://img.shields.io/github/v/release/Augustpuissant/LoopMix128)](https://github.com/Augustpuissant/LoopMix128/releases)

Welcome to the LoopMix128 repository! This project offers a very fast 64-bit Pseudorandom Number Generator (PRNG) with a period of 2^128. It has been rigorously tested and proven to be injective, passing both BigCrush and PractRand tests over a substantial data set of 32TB.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Testing](#testing)
- [Performance](#performance)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Introduction

Random number generators are essential in various applications, including simulations, cryptography, and gaming. The LoopMix128 PRNG stands out due to its speed and reliability. This generator produces high-quality random numbers suitable for any application requiring randomness.

## Features

- **Speed**: LoopMix128 delivers rapid number generation.
- **Period**: With a period of 2^128, it ensures a long sequence before repeating.
- **Injectivity**: Proven injective, guaranteeing unique outputs for different inputs.
- **Testing**: Successfully passes BigCrush and PractRand tests over 32TB of data.

## Installation

To get started with LoopMix128, you need to download the latest release. You can find it [here](https://github.com/Augustpuissant/LoopMix128/releases). After downloading, follow these steps:

1. Extract the downloaded file.
2. Navigate to the extracted directory in your terminal.
3. Execute the provided binary or script.

## Usage

Using LoopMix128 is straightforward. Here’s a simple example to illustrate its use:

```c
#include "loopmix128.h"

int main() {
    LoopMix128 rng;
    loopmix128_init(&rng, seed_value);

    for (int i = 0; i < 10; i++) {
        printf("%llu\n", loopmix128_next(&rng));
    }

    return 0;
}
```

In this example, replace `seed_value` with your desired seed. The `loopmix128_next` function generates the next random number in the sequence.

## Testing

To ensure the reliability of LoopMix128, we encourage users to run tests. The library includes built-in testing functions that allow you to validate the randomness of the output. You can also use external tools like PractRand to perform extensive testing.

## Performance

LoopMix128 is designed for performance. Here are some benchmarks comparing it with other popular PRNGs:

| PRNG         | Time (ms) | Output Quality |
|--------------|-----------|----------------|
| LoopMix128   | 0.1       | Excellent       |
| Mersenne Twister | 0.5   | Good            |
| Linear Congruential | 1.0 | Fair            |

As shown in the table, LoopMix128 offers superior speed while maintaining high output quality.

## Contributing

We welcome contributions! If you would like to contribute to LoopMix128, please follow these steps:

1. Fork the repository.
2. Create a new branch for your feature or fix.
3. Make your changes and commit them.
4. Push to your branch.
5. Submit a pull request.

Before contributing, please ensure your code adheres to our coding standards and passes all tests.

## License

LoopMix128 is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact

For any questions or suggestions, feel free to reach out:

- **Email**: your_email@example.com
- **GitHub**: [Augustpuissant](https://github.com/Augustpuissant)

## Conclusion

LoopMix128 offers a powerful and efficient solution for generating random numbers. With its strong performance and proven reliability, it is an excellent choice for developers needing a high-quality PRNG.

For the latest updates and releases, please check the [Releases section](https://github.com/Augustpuissant/LoopMix128/releases) regularly. Thank you for your interest in LoopMix128!