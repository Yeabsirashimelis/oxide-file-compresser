# File Compression

A fast and simple command-line file compression tool written in Rust using gzip compression.

## Features

- 🚀 Fast gzip compression using the `flate2` library
- 📊 Real-time compression statistics (original size, compressed size, elapsed time)
- 🎯 Simple command-line interface
- 💾 Automatic `.gz` extension handling

## Installation

### Prerequisites

- [Rust](https://www.rust-lang.org/tools/install) (1.56 or later)

### Build from source

```bash
git clone <repository-url>
cd file-compression
cargo build --release
```

The compiled binary will be available at `target/release/file-compression`.

## Usage

```bash
file-compression <source> <target>
```

### Arguments

- `<source>` - Path to the input file to compress
- `<target>` - Desired output file name (`.gz` extension will be added automatically)

### Examples

Compress a text file:
```bash
file-compression input.txt output
# Creates: output.gz
```

Compress any file type:
```bash
file-compression data.json compressed
# Creates: compressed.gz
```

The tool will display:
- Output file path
- Compression time
- Source file size
- Compressed file size

## How It Works

The tool uses the DEFLATE compression algorithm (via gzip) to reduce file sizes. It reads the input file in buffered chunks for efficient memory usage and writes the compressed output to a new `.gz` file.

## Development

### Project Structure

```
src/
├── main.rs          # Entry point
├── lib.rs           # Library exports
├── args.rs          # Command-line argument parsing
├── compression.rs   # Compression logic
└── file_ops.rs      # File I/O operations
```

### Run tests

```bash
cargo test
```

### Run with cargo

```bash
cargo run -- <source> <target>
```

## License

This project is open source and available under the MIT License.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## Author
Yeabsira Shimelis

Built with 🦀 Rust