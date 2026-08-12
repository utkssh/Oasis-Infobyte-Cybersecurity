# Task 1 – Basic Network Scanning with Nmap

## Objective

Perform a basic TCP port scan using Nmap and identify reachable services on an authorized host.

## Tool Used

- Nmap 7.99.1
- Windows command prompt / Zenmap environment

## Target

The scan was performed against an authorized host used for the internship exercise:

`192.168.34.238`

## Command Used

```text
nmap -oN "%USERPROFILE%\Downloads\scan_result.txt" 192.168.34.238
```

The first attempt to save the output inside the Nmap installation directory was denied by Windows permissions. I then saved the output in the Downloads folder instead.

## Scan Result

The host was detected as up. Nmap reported 995 closed TCP ports and identified these open ports:

| Port | State | Service |
|---|---|---|
| 135/tcp | open | msrpc |
| 139/tcp | open | netbios-ssn |
| 445/tcp | open | microsoft-ds |
| 1521/tcp | open | oracle |
| 5500/tcp | open | hotline |

The scan completed in approximately 0.89 seconds.

## What I Learned

This task helped me understand the basics of network reconnaissance and service discovery. I learned how Nmap identifies open and closed TCP ports and associates commonly known ports with services.

I also learned how to save Nmap output to a text file for documentation and later analysis.

## Evidence

This folder contains:

- `Task_1_Nmap_Report.pdf` – detailed task report
- `scan_result.txt` – saved Nmap output
- `screenshots/nmap_scan_evidence.jpg` – screenshot evidence from the practical scan

## Note

The scan was performed for educational/internship purposes on an authorized host/network.
