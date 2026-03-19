# AInstall – AOgy Download OS CLI Edition

AInstall is an advanced command-line installer and downloader, combining multi-threaded downloads, VirusTotal file scanning, YouTube downloads, Termux package installation, and configurable DNS protection. Think of it as a **CLI all-in-one download & install tool**.

---

## ⚡ Features

- **File download**
  - Multi-threaded download with progress bar
  - SHA256 hash calculation
  - Resume support if network drops
  - Real-time download speed (MB/s)
  
- **VirusTotal integration**
  - Scan downloaded files for malware
  - Cache scan results for faster future checks
  - ⚠ Requires your personal VirusTotal API key

- **YouTube download**
  - Detect YouTube links automatically
  - List available formats
  - Select desired video/audio format
  - Download directly via `yt-dlp` backend

- **History tracking**
  - JSON-based download history
  - Query by domain or date

- **Configurable**
  - YAML configuration (`Ainstall-Config/Ainstall.yml`)
  - Set threads, proxy, DNS, and more
  - Enable/disable log, alias, history

- **Termux package installation**
  - Install packages via `-tp` flag
  - Example: `ainstall -tp git`

- **DNS protection**
  - Custom DNS settings
  - Avoid local resolver leaks

- **Alias support**
  - Save aliases for frequent installs
  - Configurable via YAML

---

## 🛠 Installation

1. Make sure Java is installed:

```bash
java -version
```
Place AInstall.java in your working directory.
Compile the project:
Bash
javac AInstall.java
Run the program:
Bash
java AInstall <url>
📌 Usage Examples
Download a file
Bash
java AInstall https://example.com/file.zip
Download from YouTube
Bash
java AInstall https://www.youtube.com/watch?v=VIDEO_ID
It will prompt for the format ID to download.
Install a Termux package
Bash
java AInstall -tp git
Query history
Bash
java AInstall --history
⚠ VirusTotal API Key
To enable VirusTotal scanning:
Open the YAML configuration:
Bash
Ainstall-Config/Ainstall.yml
Add your personal VirusTotal API key:
YAML
VTKey: YOUR_PERSONAL_API_KEY
Note: The developer does not provide an API key, you must add your own.
🔧 Config (Ainstall.yml)
YAML
VTKey: YOUR_API_KEY
Threads: 4
DNS:
  Primary: 8.8.8.8
  Secondary: 1.1.1.1
Log: On
History: On
Alias: On
Threads – number of concurrent download threads
DNS – custom DNS servers
Log, History, Alias – enable/disable features
⚡ Requirements
Java 8+
yt-dlp installed for YouTube downloads
Network access
Optional: VirusTotal API key
🔒 Security Notes
Downloads are SHA256 hashed before scanning.
If VirusTotal detects malware, the file is auvtomatically deleted.
Supports safe DNS configuration to prevent leaks.
# AOgy Public License 2.0

Copyright (c) 2026 AOGY

Permission

Permission is hereby granted to any person obtaining a copy of this software and associated documentation files (the "Software") to:

- Use the Software for personal, research, and educational purposes.
- Study the source code and learn from it.
- Modify the Software.
- Redistribute modified or unmodified copies of the Software.

These permissions are granted free of charge, under the conditions described below.

---

Conditions

1. Credit Preservation
   
   The original credit to "AOGY" must remain visible in:
   
   - the source code
   - documentation
   - redistributed copies of the Software

2. Non-Commercial Use
   
   The Software may NOT be sold, licensed commercially, or included in commercial products without explicit written permission from AOGY.

3. No Malicious Usage
   
   The Software may NOT be used to create or distribute:
   
   - malware
   - ransomware
   - spyware
   - cryptominers
   - exploits targeting user systems
   - software designed to violate privacy or security

4. Fork Transparency
   
   If the Software is modified or forked:
   
   - the modified version must clearly state that it is a modified version
   - the original author AOGY must remain credited

5. No Author Rebranding
   
   No person may claim authorship of the original Software or remove the original author attribution.

---

Disclaimer

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO:

- MERCHANTABILITY
- FITNESS FOR A PARTICULAR PURPOSE
- NON-INFRINGEMENT

IN NO EVENT SHALL THE AUTHOR OR COPYRIGHT HOLDER BE LIABLE FOR ANY CLAIM, DAMAGES, OR OTHER LIABILITY ARISING FROM THE USE OF THE SOFTWARE.

---

Summary (Human-Readable)

You are free to:

- use the software
- learn from the code
- modify it
- share it

But you must:

- keep credit to AOGY
- not sell it
- not use it for malware

---

License Name

AOgy Public License 2.0 (APL-2.0)
