# nmem - A Simple Memory Usage Monitoring Tool

`nmem` is a lightweight Bash script designed to provide a quick overview of system memory usage. While similar in functionality to the GNU `free` command, `nmem` is not intended as a direct replacement. Instead, it's a simplified tool offering basic insights into memory status on Linux systems. Its scope is limited to providing essential memory metrics in a human-readable format, with optional real-time monitoring.

## Project Scope

- **Purpose**: `nmem` aims to give users a straightforward way to check memory usage without the complexity of the full `free` utility. It is perfect for those who want a quick glance at memory status, whether for personal monitoring or lightweight system management.
- **Not a `free` Alternative**: This script is not meant to replace the `free` command from the GNU Core Utilities. It lacks many of the advanced features and platform integrations of `free`.
- **No Distribution Platform**: `nmem` will not be available through package managers or distributions. It is provided as a standalone script for users to install manually if they find it useful.

## Features

- Displays basic memory metrics: Total, Used, Free, Buffers, and Cached.
- Supports various units: Bytes, Kilobytes, Megabytes, Gigabytes, and human-readable format.
- Real-time monitoring with the `--watch` flag, refreshing memory stats every second.
- Lightweight and does not require any external dependencies beyond a POSIX-compliant shell.

## Installation

Since `nmem` is a standalone script and not available via package managers, you can manually install it by following these steps:

1. **Download the Script**: Download `nmem` to your machine.
   ```bash
   wget https://github.com/MohamedElashri/nmem/raw/main/nmem -O nmem
   ```
2. **Make the Script Executable**:
   ```bash
   chmod +x nmem
   ```
3. **Move `nmem` to a Directory in Your PATH**:
   To make `nmem` available system-wide, move it to a directory that is part of your system's `PATH`. Commonly used directories include `/usr/local/bin` or `$HOME/bin`.
   ```bash
   sudo mv nmem /usr/local/bin/
   ```
   Alternatively, if you prefer a local installation, ensure `$HOME/bin` is in your `PATH` and move `nmem` there:
   ```bash
   mv nmem $HOME/bin/
   ```

4. **Verify Installation**:
   ```bash
   nmem --help
   ```

## Usage

### Basic Usage

Simply run `nmem` to get a snapshot of the memory usage in human-readable format:

```bash
nmem
```

This will show something like the following 

```bash
+----------+------------+------------+------------+------------+------------+------------+-------------+
|   Metric  |    Total   |    Used    |    Free    |  Buffers   |   Cached   |   Shared   | Available  |
+----------+------------+------------+------------+------------+------------+------------+-------------+
| Memory    |      28 GB |      10 GB |       1 GB |       1 GB |      14 GB |     800 MB |      15 GB |
+----------+------------+------------+------------+------------+------------+------------+-------------+
| Swap     |      19 GB |       0 KB |      19 GB |            |            |            |           | |
+----------+------------+------------+------------+------------+------------+------------+-------------+
```

### Available Options

- **Units**:
  - `-b` : Show output in bytes
  - `-k` : Show output in kilobytes
  - `-m` : Show output in megabytes
  - `-g` : Show output in gigabytes
  - Default is human-readable format.

- **Real-Time Monitoring**:
  - `--watch` : Continuously update memory usage every second.

### Examples

- Show memory usage in megabytes:
  ```bash
  nmem -m
  ```
- Watch memory usage in gigabytes:
  ```bash
  nmem -g --watch
  ```

## Limitations

- **Scope**: `nmem` provides a basic view of system memory. It does not offer the full range of metrics and options that `free` provides.
- **Linux Only**: The script is designed for Linux systems with the `/proc/meminfo` file. It may not work on non-Linux systems.
- **No Package Management**: This tool will not be included in any package managers. It is intended for manual installation only.

## Contributing

Contributions are welcome! However, please note that the scope of this tool is intentionally limited to providing a simple overview of memory usage. If you have ideas for small improvements or bug fixes, feel free to open a pull request.

To contribute:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes.
4. Commit your changes (`git commit -m 'Add new feature'`).
5. Push to the branch (`git push origin feature-branch`).
6. Open a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](./LICENSE) file for details.



## Acknowledgments

`nmem` is inspired by the simplicity and utility of the `free` command. This project aims to provide a basic alternative for users needing a minimalistic memory monitoring solution.
