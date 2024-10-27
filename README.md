# mkp224o on Google Colab

A Google Colab notebook to generate vanity `.onion` addresses for Tor v3 hidden services using `mkp224o`. This notebook allows users to harness Google Colab’s computational power to generate custom `.onion` addresses without needing a high-performance local machine.

## Features

- Generates version 3 `.onion` addresses with specified prefixes.
- Utilizes Google Colab for CPU-intensive operations.
- Suitable for those without local computational resources.

## Installation and Setup on Google Colab

To set up and run the `mkp224o` tool on Google Colab, follow these steps within the Colab notebook:

1. **Clone the `mkp224o` Repository**:
   ```python
   !git clone https://github.com/cathugger/mkp224o.git
   cd mkp224o/
   ```

2. **Install Required Packages**:
   ```python
   !sudo apt install gcc libsodium-dev make autoconf git
   ```

3. **Build the `mkp224o` Tool**:
   ```python
   !./autogen.sh
   !./configure
   !make
   ```

4. **Run `mkp224o` with Custom Prefix**:
   Replace `^eneskeremaydin` with your desired prefix, and adjust the `-n` value to set the number of addresses to generate:
   ```python
   !./mkp224o ^eneskeremaydin -y -n 100
   ```

## Files

- **`vanity .onion v3 address generator (mkp224o).ipynb`**: The Jupyter Notebook designed for Google Colab, automating the setup and generation of vanity `.onion` addresses.

## Requirements

- A Google account to access Google Colab.
- Basic knowledge of Jupyter Notebooks and command-line commands.

## Disclaimer

This tool is intended for educational or personal use. Generating complex vanity `.onion` addresses may take significant time, depending on the prefix complexity.
