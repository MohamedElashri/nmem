# Memory Info Formatter

This script formats and displays system memory information from `/proc/meminfo` in a neatly organized, two-column layout. It reads the memory data, converts values to human-readable formats (KB, MB, GB, TB, PB), and applies color coding to make it easier to interpret.

## Features
- Displays system memory information in two columns.
- Converts memory values to a human-readable format.
- Uses color coding to differentiate between KB, MB, GB, TB, and PB.

## Prerequisites
- A Unix-like operating system (e.g., Linux).
- Access to the `/proc/meminfo` file.
- Bash shell.

## Usage

1. Save the script as `meminfo_no_headers.sh`.
2. Make the script executable:
    ```bash
    chmod +x meminfo_no_headers.sh
    ```
3. Run the script:
    ```bash
    ./meminfo_no_headers.sh
    ```
The script will display memory information in a formatted, two-column layout directly in the terminal.
