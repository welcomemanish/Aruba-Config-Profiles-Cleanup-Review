# Aruba CPCR — Config Profiles Cleanup Review

A browser-based tool for HPE Aruba network engineers to analyze `tech-support.log` files and identify unused or unreferenced configuration profiles — helping to streamline and clean up controller configurations.

> **No installation required.** Everything runs locally in your browser. No data is uploaded to any server.

---

## Overview

When managing HPE Aruba Mobility Controllers over time, configuration profiles tend to accumulate — many of which may no longer be referenced anywhere in the running configuration. The **Config Profiles Cleanup Review (CPCR)** tool automates the process of identifying these orphaned profiles, giving network teams a clear, actionable report.

The tool parses the `show running-config` section from a tech-support log file, scans for over **100 profile types** (AAA, RF, WLAN, IDS, AP, UCC, and more), and checks whether each profile name appears to be actively referenced.

---

## Features

- **Drag & drop file upload** — supports `.log` and `.txt` tech-support files
- **Auto-analysis** — parsing begins immediately on file load, no extra clicks needed
- **Comprehensive keyword coverage** — 100+ profile types including AAA, RF, WLAN, AP, IDS, UCC, crypto, VRRP, and more
- **Smart matching** — skips built-in `default` profiles; marks a profile as `YES` (in use) if its name appears ≥ 2 times in the config
- **VRRP detection** — matches VRRP instance numbers against `Virtual Router` entries
- **Stats summary** — total profiles, in-use count, unused count, and usage rate %
- **Search & filter** — real-time search by keyword or profile name; filter by YES / NO / ALL
- **Sortable columns** — click any column header to sort
- **Export CSV** — download the current filtered view as a CSV file
- **Three themes** — Dark, Gray, and Light (preference saved in browser)
- **Fully offline** — all processing happens in-browser, no server required

---

## Usage

1. **Download** `Aruba CPCR - By Manish Sharma.html`
2. **Open** the file in any modern web browser (Chrome, Edge, Firefox, Safari)
3. **Upload** your `tech-support.log` file by dragging it onto the drop zone or clicking to browse
4. Analysis starts **automatically** — results appear within seconds
5. Use the **search box**, **filter buttons**, and **column sort** to explore results
6. Click **Export CSV** to save the report

---

## How It Works

The parser:

1. Locates the `show running-config` section within the tech-support log
2. Scans each line against a predefined list of HPE Aruba profile keywords
3. Extracts the profile name (the token immediately following the keyword)
4. Skips any profile named `default`
5. Counts how many times the extracted profile name appears anywhere in the running config
6. If the count is **≥ 2**, the profile is marked **YES** (in use); otherwise **NO** (potentially unused)
7. Separately matches VRRP instance numbers against `Virtual Router` lines

> **Note:** A `NO` result means the profile name was not found referenced elsewhere in the config. It does **not** automatically mean the profile is safe to delete — always verify before making changes in production.

---

## Supported Profile Types (Sample)

| Category | Examples |
|---|---|
| AAA | `aaa profile`, `aaa server-group`, `aaa authentication dot1x`, `aaa authentication-server radius` |
| RF | `rf arm-profile`, `rf dot11a-radio-profile`, `rf ht-radio-profile`, `rf spectrum-profile` |
| WLAN | `wlan ssid-profile`, `wlan virtual-ap`, `wlan hotspot *`, `wlan he-ssid-profile` |
| AP | `ap-group`, `ap system-profile`, `ap wired-port-profile`, `ap regulatory-domain-profile` |
| IDS | `ids profile`, `ids dos-profile`, `ids signature-profile`, `ids general-profile` |
| UCC | `ucc`, `lc-cluster group-profile` |
| Network | `ip access-list session`, `netdestination`, `user-role`, `vlan-name`, `crypto isakmp policy` |
| VRRP | `vrrp <n>` matched against `Virtual Router <n>` |

---

## Browser Compatibility

| Browser | Support |
|---|---|
| Chrome 90+ | ✅ Full |
| Edge 90+ | ✅ Full |
| Firefox 88+ | ✅ Full |
| Safari 14+ | ✅ Full |

---

## Disclaimer

This tool is provided for informational purposes only. HPE/Aruba Support provides information on the usage status of configuration profiles. The tool output should be reviewed carefully by a qualified network engineer before any configuration changes are made in a production environment.

---

## Author

**Manish Sharma**  
[github.com/welcomemanish](https://github.com/welcomemanish)

---

## License

This project is licensed under the **BSD 2-Clause License** — see the [LICENSE](LICENSE) file for details.
