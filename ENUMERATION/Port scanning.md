To perform a comprehensive port and service enumeration using Nmap, you need a command that scans all ports, detects service versions, runs default reconnaissance scripts, and performs OS detection.

Here is the ultimate, go-to Nmap command for deep information gathering:

Bash

```bash
nmap -p- -sV -sC -O --reason -T4 <target-ip>
```

### ## Breakdown of the Flags

- `-p-`: Scans all 65,535 TCP ports (by default, Nmap only scans the top 1,000 most common ports).
    
- `-sV`: Probes open ports to determine service/version information.
    
- `-sC`: Runs a suite of default NSE (Nmap Scripting Engine) scripts categorized for safe discovery and vulnerability checking.
    
- `-O`: Enables OS (Operating System) detection.
    
- `--reason`: Explains _why_ Nmap classified a port in a certain state (e.g., `syn-ack` received), which is crucial for troubleshooting firewalls.
    
- `-T4`: Speeds up the scan (Aggressive timing template). _Use `-T3` if stability on the target network is a concern._

```

```

![[image.png]]