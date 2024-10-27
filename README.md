
# Network Scanner

This is a simple Python script that performs network scanning by sending ARP requests to a specified IP or IP range on Linux systems. It is useful for identifying active devices on a network and retrieving their IP and MAC addresses.

## Features
- Send ARP requests to discover active devices within a given IP range.
- Display the IP and MAC address of each detected device on the network.

## Prerequisites
- Python 3.x
- Linux-based operating system
- `scapy` library (for handling ARP requests)

## Installation

Clone the repository to your local machine:

```bash
git clone https://github.com/yourusername/network_scanner.git
cd network_scanner
```

Install the required library:

```bash
pip install scapy
```

## Usage

Run the script with superuser privileges to scan a target IP or IP range.

```bash
sudo python3 network_scanner.py -t <target_ip_or_range>
```

### Arguments:
- `-t` or `--target`: The target IP or IP range you want to scan (e.g., `192.168.1.1` or `192.168.1.1/24`).

### Example:

```bash
sudo python3 network_scanner.py -t 192.168.1.1/24
```

### Output:
- The script will display a table of IP addresses and corresponding MAC addresses for each active device on the specified network.

```
IP              MAC Address
-----------------------------------------
192.168.1.1     00:11:22:33:44:55
192.168.1.2     00:66:77:88:99:AA
...
```

## Notes:
- The script currently supports only Linux systems with `scapy` installed.
- Scanning requires network privileges, so ensure you are running the script with `sudo` or as root.
- Ensure that the IP range is correctly formatted for accurate results.

## Troubleshooting:
- If the scan does not return any results, check if the target IP range is correct and that the devices are on the same subnet.
- Make sure `scapy` is installed, as it is essential for handling ARP requests.

## License
This project is licensed under the MIT License.

## About

This script is part of the course [Learn Python & Ethical Hacking from Scratch](https://www.udemy.com/course/learn-python-and-ethical-hacking-from-scratch/) on Udemy. The course covers Python scripting and its application in ethical hacking, network security, and more.