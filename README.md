# Network Port Scanner (Tkinter GUI)

A simple **TCP port scanner with a minimal Tkinter GUI**. Enter a target (IP/hostname) and a port range, then run a multi-threaded scan to discover **open TCP ports**. Results can be saved to a `.txt` file.

> File: `portscanergui.py`

## Features
- GUI built with **Tkinter**
- Scan a target **IP address or hostname**
- Scan a configurable port range (0–65535)
- Multi-threaded scanning (internal default: **500 workers**)
- Progress bar + elapsed time
- Displays open ports and common service names (basic mapping)
- Save results to a text file

## Requirements
- Python 3.x
- Tkinter (usually included with Python on Windows/macOS; on some Linux distros you may need to install it)

No third-party packages are required.

## How to Run

### 1) Clone the repo
```bash
git clone https://github.com/gamana29/Network-Port-Scanner.git
cd Network-Port-Scanner
```

### 2) Run the GUI
```bash
python portscanergui.py
```
(If your system uses `python3`:)
```bash
python3 portscanergui.py
```

## Usage
1. **Target (IP / Hostname)**: Example: `127.0.0.1`, `scanme.nmap.org`, or a LAN IP like `192.168.1.1`
2. **Start Port**: Example: `1`
3. **End Port**: Example: `1024`
4. Click **Start Scan**
5. Optional: click **Save Results** to export open ports to a `.txt` file

## Notes / Safety
- Scan only hosts you own or have explicit permission to test.
- The scanner uses TCP connect scanning (`socket.connect_ex`) and a per-connection timeout (internal default: `0.5s`).

## Customization
Inside `portscanergui.py`, you can adjust:
- `COMMON_PORTS` mapping to display additional service names
- Internal defaults used by the scanner:
  - `timeout = 0.5`
  - `max_threads = 500`

## License
Add a license file (e.g., MIT) if you want to specify how others may use this code.
