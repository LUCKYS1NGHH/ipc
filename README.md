# ipc — IP Checker

A minimal command-line tool to fetch your public IP address and display geolocation details about it.

## What it does

- Fetches your current public IP via [httpbin.org](https://httpbin.org/ip)
- Looks up IP details (hostname, city, region, country, coordinates, ISP/org) via [ipinfo.io](https://ipinfo.io)
- Prints everything neatly to the terminal

## Requirements

- Python 3.x
- [`requests`](https://pypi.org/project/requests/) library

```bash
pip install requests
```

## Usage

```bash
ipc
```

### Example output

```
Welcome to the IP Looker!
Your Public IP Address: 203.0.113.42
IP Address:   203.0.113.42
Hostname:     example.hostdomain.net
City:         Tokyo
Region:       Tokyo
Country:      JP
Location:     35.6895,139.6917
Organization: AS12345 Some ISP Ltd.
```

## Notes

- No API key required for basic usage (ipinfo.io free tier: 50k requests/month)
- Does not support lookup of arbitrary IPs — it only checks your own public IP
- Output is printed to stdout; the function also returns a dict if you want to use it programmatically
