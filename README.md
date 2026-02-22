# ZashironSentinel

ZashironSentinel is a Windows-focused antivirus and endpoint protection engine designed to detect, quarantine, and monitor malicious activity in real time. It is built for developers and power users who want transparent, configurable protection with a focus on system-level visibility and performance.

## Features

- Real-time file system monitoring with on-access scanning and event logging.
- On-demand quick and deep scans for selected drives, folders, or custom paths.
- Signature-based detection using a local hash/signature database with user-managed entries.
- Heuristic and behavior-based checks for suspicious process and script activity.
- Quarantine system that safely isolates, restores, or permanently deletes detected threats.
- Whitelist/ignore rules for trusted files, folders, and processes to reduce false positives.
- Detailed logs for detections, scan sessions, and system events, suitable for later analysis.
- Configurable scheduled scans and background tasks.

## Architecture Overview

- **Core**  
  Implements scanning, detection logic, quarantine management, and persistence of signatures and configuration. 

- **Signature Database**  
  Local store (e.g., SQLite/JSON/custom) for known-bad hashes, patterns, and rules, with update and export/import support.

- **Service / Daemon**  
  Optional background service to monitor the file system and processes, independent of the UI.

- **User Interface**  
  Desktop UI (e.g., PySide/Kivy/Win32/.NET) providing dashboards, scan controls, logs, and settings.

## Getting Started

### Prerequisites

- Windows 11 or later (64-bit).
- Python 3.x / .NET / native toolchain (update to your actual stack).
- Recommended: Administrator rights to enable low-level monitoring and access system directories.

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/Zashiron/Zashiron-Sentinel.git
   cd ZashironSentinel
   ```

2. (If Python) Create and activate a virtual environment:
    ```bash
    bash
    python -m venv venv
    venv\Scripts\activate
    ```

3. Install dependencies:
    ```
    pip install -r requirements.txt
    ```
