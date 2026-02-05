# Changelog

All notable changes to this project will be documented in this file.

## [5.1.0] - 2026-02-05

### Added
- Security hardening with centralized job control
- Rate limiting with exponential backoff
- Improved error handling and logging
- Verbose mode for debugging (`--verbose` flag)
- Comprehensive input validation

### Changed
- Removed dangerous bash constructs (eval, command substitution in prompts)
- Improved variable quoting throughout
- Enhanced timeout management for all phases
- Optimized parallel execution logic

### Fixed
- Resume functionality stability
- Memory leak issues in long-running scans
- Race conditions in concurrent operations

## [5.0.0] - 2025-12-01

### Added
- 14-phase reconnaissance pipeline
- Resume capability with checkpoint system
- Tor network support
- Multi-target scanning
- Automated report generation

### Features
- Phase 1: Subdomain Enumeration
- Phase 2: DNS Resolution
- Phase 3: Port Scanning
- Phase 4: HTTP Probing
- Phase 5: Web Crawling
- Phase 6: Nuclei Scanning
- Phase 7: Vulnerability Pattern Matching
- Phase 8: DNS Reconnaissance
- Phase 9: Screenshots
- Phase 10: Technology Detection
- Phase 11: Parameter Discovery
- Phase 12: Enhanced Parameter Fuzzing
- Phase 13: CORS Testing
- Phase 14: Quick Security Checks

### Tools Integrated
- subfinder, amass, assetfinder, findomain
- dnsx, massdns, puredns
- naabu, nmap
- httpx
- waybackurls, katana, hakrawler
- nuclei
- gowitness
- arjun, x8
- dalfox, sqlmap
- And 30+ more security tools

---

## Version History

- **v5.1**: Current release with security hardening
- **v5.0**: Initial comprehensive 14-phase pipeline
- **v4.x**: Legacy versions (deprecated)
