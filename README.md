# Redis Vulnerability Scanner


## Overview

Redis Vulnerability Scanner is a powerful and efficient script designed to scan Redis instances across multiple IP addresses and ports to identify potential vulnerabilities.

## Features

- Scans multiple IP addresses and ports concurrently.
- Identifies vulnerable Redis instances.
- Optionally fetches keyvalue pairs from the database and displays proof of concept (PoC) data from vulnerable instances.
- Provides detailed output including counts of vulnerable, non-vulnerable, and unreachable IPs.
- Offers options to display only vulnerable IPs or only the IP addresses of vulnerable instances.

## Installation

1. **Clone the repository:**
    ```sh
    git clone https://github.com/zipponnova/redis-vulnerability-scanner.git
    cd redis-vulnerability-scanner
    ```

2. **Install dependencies:**
    ```sh
    pip3 install redis termcolor
    ```

## Usage

### Command-Line Options

- `--ips`: List of IP addresses to scan (space/comma separated).
- `--ips-file`: File containing IP addresses (line/space/comma separated).
- `--ports`: List of ports to scan.
- `--max-workers`: Maximum number of worker threads (default is 10).
- `--poc`: Fetch proof of concept data from Redis.
- `--only-vulnerable`: Print only vulnerable IPs and their details.
- `--only-ips`: Print only IP addresses of vulnerable instances.

### Examples

#### Scan IPs from a file and print only vulnerable IP addresses

```sh
python3 redis-vulnerability-scanner.py --ips-file ips.txt --ports 6379 --only-ips
```

