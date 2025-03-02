---
title: "Create a Simple Shell Script for Backup (2025/03/02)"
description: ""
---

#### [Visit (https://github.com/takehika0129/no18-simple-shell-script)](https://github.com/takehika0129/no18-simple-shell-script)


# **Concept**
This shell script simplifies a backup process by creating timestamped archives and maintaining a “latest” file.


# **Features**
- **📂 Directory Backup Automation**: Compresses a specified folder into a .tar.gz archive.
- **📅 Timestamped Backups**: Ensures each backup has a unique filename with the current date.
- **💾 Latest Version Retention**: Overwrites a backup-latest.tar.gz file to always keep the most recent backup accessible.
- **⚡ Error Handling**: Uses set -eu and trap to catch errors and prevent silent failures.
- **🛠️ Easy Setup**: Simple configuration by defining SOURCE_DIR and BACKUP_DIR.


# **Future Improvements**
- **Logging & Notification System**: Adding a logging mechanism or email notifications would help users stay informed about backup success or failure.
- **Storage Control**: For example, keeping only the last 7 days ensures a balance between data retention and storage efficiency.


---
[Back to All Prototypes](../index.md)
