# WiFiJammer

![Wifi Jammer](https://img.shields.io/badge/WiFi-Jammer-blue)

**Disconnect Nearby Access Points and Stations with WiFiJammer**

WiFiJammer is a powerful tool designed to disrupt and analyze Wi-Fi networks by forging and transmitting deauthentication frames. Built on top of Scapy, this tool utilizes channel hopping and frame forging from a single interface, providing a comprehensive solution for testing and understanding Wi-Fi security. Compatible with Python 3.

## Installation

1. Install Scapy:

   ```bash
   $ pip3 install scapy==2.4.3
   ```

2. Clone the repository and check the manual:

   ```bash
   $ git clone https://github.com/mabdulrehmankhan/wifi-jammer.git
   $ cd wifi-jammer/
   $ python3 wifi-jammer.py --help
   ```

## Usage

```bash
python3 [scriptname] [argument...]
python3 wifi-jammer.py --help
```

### Arguments

| Args              | Description                                        | Default |
| ----------------- | -------------------------------------------------- | ------- |
| -h, --help        | Throwback this help manual                        | False   |
| -i, --interface   | Monitor Mode Interface for scanning & deauthentication | None    |
| -c, --channel     | Channel to put monitor interface on               | All     |
| -a, --accesspoints| Comma-separated list of access points to target    | All     |
| -s, --stations    | Comma-separated list of stations to target         | All     |
| -f, --filters     | Comma-separated list of Mac addresses to skip target | None  |
| -p, --packets     | Number of deauthentication packets to send per turn | 25    |
| -d, --delay       | Delay between transmission of packets             | 0.1s   |
| -r, --reset       | Refresh the target list after reaching a specific number, e.g., --reset 5 | None |
| --code            | Deauthentication Code to send with packets        | 7      |
| --world           | Scan for channels from 1-14, default is 1-11      | False  |
| --aggressive      | Run in Aggressive Mode. Send continuous frames to Broadcast | False  |
| --no-broadcast    | Don't send deauthentication packets to broadcast address | False |
| --verbose         | Print device manufacturing details                | False  |

### Example

Disconnecting Access Points from their stations on channel 6:

```bash
$ python3 wifi-jammer.py --interface wlan1mon --channel 6 --aggressive
```

## Disclaimer

This tool is intended for testing purposes only and should be used where there is allowance for de-authentication tests. Users must obtain prior consent for testing against the target. The author will not be held responsible for any misuse.

## Author

- LinkedIn: [mabdulrehmankhan]([https://twitter.com/hash3liZer](https://www.linkedin.com/in/muhammadabdulrehmankhanofficial/)https://www.linkedin.com/in/muhammadabdulrehmankhanofficial)
- Email: abdulrehman.sameed@gmail.com
