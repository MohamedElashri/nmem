# Swap Usage Summary Script

This script provides a summary of the system's swap usage using various Linux commands (`free`, `swapon`, `/proc/swaps`, `vmstat`, `top`). It gathers and displays total, used, and free swap space on the system in a human-readable format.

## Prerequisites

- This script is compatible only with Linux operating systems.
- The following commands should be available on your system: `free`, `swapon`, `vmstat`, `top`.

## Usage

To use this script, simply run it from the terminal:

```bash
./nswap
```

### Output

The script outputs a table summarizing the system's swap usage:

```
This table provides a summary of system swap usage as reported by different methods.
Method       Total                Used                 Free                
------       ------------------   -----------------    ----------------    
free         19.99 GB             957.75 MB            19.06 GB            
swapon       19.99 GB             957.75 MB            19.06 GB            
proc         19.99 GB             957.75 MB            19.06 GB            
vmstat       19.99 GB             957.75 MB            19.06 GB            
top          19.99 GB             957.80 MB            19.06 GB            
```

### Options

- `-h`, `--help`: Display help information about the script.

```bash
./nswap --help
```

### Example

Run the script to view the swap usage:

```bash
./nswap
```

## Notes

- This script requires execution permission. If it's not executable, run:

```bash
chmod +x nswap
```


