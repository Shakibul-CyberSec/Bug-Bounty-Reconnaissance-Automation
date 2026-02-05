# Bug Bounty Recon Pipeline

Ultra-fast, security-hardened reconnaissance automation for bug bounty hunters and penetration testers. A comprehensive 14-phase pipeline built for speed and reliability.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)](https://github.com/Shakibul-CyberSec/Bug-bounty-recon-pipeline/releases)
[![Bash](https://img.shields.io/badge/bash-5.0%2B-green.svg)](https://www.gnu.org/software/bash/)

## 🚀 Features

- **14-Phase Pipeline**: Complete reconnaissance from subdomain enumeration to vulnerability scanning
- **Security Hardened**: Production-ready bash script with proper error handling and input sanitization
- **Resume Capability**: Checkpoint system allows resuming interrupted scans
- **Performance Optimized**: Parallel execution with configurable concurrency
- **Rate Limiting**: Smart exponential backoff to prevent API overload
- **Tor Support**: Optional anonymization through Tor network
- **50+ Tools Integrated**: Best-in-class security tools working together

## 📋 Requirements

- Linux/Unix system (tested on Ubuntu 24.04)
- Root/sudo access for installation
- Minimum 2GB RAM
- 10GB free disk space

## 🛠️ Installation

```bash
# Clone the repository
git clone https://github.com/Shakibul-CyberSec/Bug-bounty-recon-pipeline.git
cd Bug-bounty-recon-pipeline

# Make scripts executable
chmod +x install.sh recon.sh

# Run the installer
sudo ./install.sh
```

The installer will:
- Install all required tools (50+ security tools)
- Set up default wordlists and resolvers
- Configure Tor proxy (optional)
- Download Nuclei templates

## 🎯 Usage

### Basic Scan
```bash
./recon.sh target.com
```

### With Verbose Output
```bash
./recon.sh target.com --verbose
```

### Multiple Targets
```bash
# Create a targets file (one domain per line)
./recon.sh targets.txt
```

### Resume Interrupted Scan
```bash
./recon.sh
# Select the incomplete scan when prompted
```

## 📊 Reconnaissance Phases

| Phase | Name | Tools Used |
|-------|------|------------|
| 01 | Subdomain Enumeration | subfinder, amass, assetfinder, findomain |
| 02 | DNS Resolution | dnsx, massdns, puredns |
| 03 | Port Scanning | naabu, nmap |
| 04 | HTTP Probing | httpx |
| 05 | Web Crawling | waybackurls, katana, hakrawler |
| 06 | Content Discovery | feroxbuster, meg |
| 07 | Vulnerability Scanning | nuclei |
| 08 | Advanced DNS Recon | dig, zone transfers |
| 09 | Screenshots | gowitness |
| 10 | Technology Detection | webanalyze, wappalyzer |
| 11 | Parameter Discovery | arjun, x8 |
| 12 | Parameter Fuzzing | dalfox, sqlmap, gxss |
| 13 | CORS Testing | corstest |
| 14 | Quick Security Checks | subdomain takeover, s3 buckets, git exposure |

## 📂 Output Structure

```
recon_output_YYYYMMDD_HHMMSS/
├── target.com/
│   ├── subdomains/
│   │   ├── all_subdomains.txt
│   │   ├── live_subdomains.txt
│   │   └── resolved_subdomains.txt
│   ├── ports/
│   │   ├── open_ports.txt
│   │   └── nmap_scan.txt
│   ├── http/
│   │   ├── live_urls.txt
│   │   └── http_responses.txt
│   ├── vulnerabilities/
│   │   ├── nuclei_results.txt
│   │   └── custom_checks.txt
│   ├── screenshots/
│   │   └── *.png
│   └── report.html
└── recon.log
```

## ⚙️ Configuration

The script uses sensible defaults but can be customized by editing `recon.sh`:

```bash
MAX_CONCURRENT_JOBS=5        # Parallel jobs
NAABU_RATE=2000             # Port scan rate
HTTPX_THREADS=100           # HTTP probe threads
NUCLEI_RATE_LIMIT=150       # Nuclei scan rate
```

## 🔒 Security Features

- No use of `eval` or dangerous bash constructs
- Proper variable quoting throughout
- Input validation and sanitization
- Centralized job control with timeout management
- Exponential backoff for rate limiting
- Secure temporary file handling

## 📚 Documentation

- [Setup Guide](SETUP.md) - Detailed installation and configuration
- [Usage Examples](EXAMPLES.md) - Real-world usage scenarios
- [FAQ](docs/FAQ.md) - Frequently asked questions
- [Security Policy](SECURITY.md) - Security guidelines and reporting
- [Contributing](CONTRIBUTING.md) - How to contribute
- [Credits](CREDITS.md) - Acknowledgments and attributions

## 🐛 Troubleshooting

See [SETUP.md](SETUP.md) for detailed troubleshooting guide.

Quick fixes:
- **Tool not found**: Reload shell with `source ~/.bashrc`
- **Permission denied**: Run `chmod +x recon.sh install.sh`
- **Out of memory**: Reduce `MAX_CONCURRENT_JOBS` in script

## 🤝 Contributing

Contributions are welcome! Please read [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

This project was developed with assistance from:

- **AI Development Partners**: Claude (Anthropic), DeepSeek, and ChatGPT for code development, optimization, and documentation
- **Open Source Community**: All the amazing security tools that make this pipeline possible
- **Security Researchers**: The bug bounty and infosec community

See [CREDITS.md](CREDITS.md) for detailed acknowledgments.

## 👤 Author

**Shakibul** ([@Shakibul_Cybersec](https://twitter.com/Shakibul_Cybersec))

## ⭐ Show Your Support

Give a ⭐️ if this project helped you!

## ⚠️ Legal Disclaimer

This tool is for authorized security testing only. Always obtain proper permission before scanning any target. Unauthorized scanning is illegal. The authors are not responsible for misuse of this tool.

---

**Happy Hunting! 🚀**
