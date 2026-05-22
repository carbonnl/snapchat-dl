<div align="center">
  <h1>👻 Snapchat Public Stories Downloader</h1>
</div>

<div align="center">

Download public Snapchat stories directly from the command line.

[![PyPI Version](https://img.shields.io/pypi/v/snapchat-dl.svg)](https://pypi.org/project/snapchat-dl/)
[![Python Versions](https://img.shields.io/pypi/pyversions/snapchat-dl)](https://pypi.org/project/snapchat-dl/)
[![Wheel](https://img.shields.io/pypi/wheel/snapchat-dl)](https://pypi.org/project/snapchat-dl/)
[![CI](https://img.shields.io/github/actions/workflow/status/skyme5/snapchat-dl/continuous-integration-pip.yml)](https://github.com/skyme5/snapchat-dl/actions)
[![Code Coverage](https://img.shields.io/codecov/c/github/skyme5/snapchat-dl)](https://codecov.io/gh/skyme5/snapchat-dl)
[![Downloads](https://static.pepy.tech/badge/snapchat-dl)](https://pepy.tech/project/snapchat-dl)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Code Style](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)

</div>

---

## Features

- Download public Snapchat stories
- Monitor accounts for new uploads
- Batch download multiple usernames
- Save story metadata as JSON
- Parallel downloads for improved speed
- Clipboard story link detection
- Lightweight and easy-to-use CLI

---

## Installation

### Install from PyPI

```bash
pip install snapchat-dl
```

### Install from GitHub

```bash
pip install git+https://github.com/skyme5/snapchat-dl.git
```

> Linux/macOS users may want to add `--user` to avoid requiring `sudo`.

---

## Quick Start

Download stories from a username:

```bash
snapchat-dl username
```

Download stories from multiple users:

```bash
snapchat-dl user1 user2 user3
```

Monitor for new stories continuously:

```bash
snapchat-dl -u username
```

Save metadata as JSON:

```bash
snapchat-dl -d username
```

---

## Usage

```text
usage: snapchat-dl [-h] [-c | -u] [-i BATCH_FILENAME]
                   [-P DIRECTORY_PREFIX] [-s] [-d]
                   [-l MAX_NUM_STORY] [-j MAX_WORKERS]
                   [-t INTERVAL] [--sleep-interval INTERVAL]
                   [-q]
                   [username [username ...]]
```

### Arguments

| Argument | Description |
|---|---|
| `username` | One or more usernames to download stories from |
| `-h, --help` | Show help message |
| `-c, --scan-clipboard` | Scan clipboard for Snapchat story links |
| `-u, --check-for-update` | Periodically check for new stories |
| `-i, --batch-file` | Read usernames from a file |
| `-P, --directory-prefix` | Set download directory |
| `-s, --scan-from-prefix` | Scan usernames from directory names |
| `-d, --dump-json` | Save metadata as JSON |
| `-l, --limit-story` | Limit number of stories downloaded |
| `-j, --max-concurrent-downloads` | Set concurrent download count |
| `-t, --update-interval` | Interval for checking new stories |
| `--sleep-interval` | Delay between downloads |
| `-q, --quiet` | Suppress console output except errors |

---

## Examples

### Download stories from a single account

```bash
snapchat-dl nasa
```

### Download using a batch file

```bash
snapchat-dl -i usernames.txt
```

### Limit downloads

```bash
snapchat-dl -l 5 username
```

### Set custom output directory

```bash
snapchat-dl -P ./downloads username
```

---

## Output Structure

```text
downloads/
└── username/
    ├── Images/
    │   ├── image1.jpg
    │   └── image2.jpg
    │
    └── Videos/
        ├── video1.mp4
        └── video2.mp4
```

---

## License

This project is licensed under the MIT License.

---

## Disclaimer

This project is intended for educational and archival purposes only.  
Please respect Snapchat’s Terms of Service and content ownership rights.
