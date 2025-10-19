---
layout: technique
title: SharePoint Synchronization
mitre_id: T1213.002
tactics:
  - Collection
platforms:
  - M365
tags:
  - SharePoint
  - OneDrive
  - Data Exfiltration
---

## Overview

SharePoint sync is an inbuilt feature which if abused by a Threat Actor allows the contents of a SharePoint site to be downloaded to their local device.

---

## Sync Methods

There are two native options available when synching files from SharePoint sites:

- The Sync Button from within a SharePoint Document Library.
- Add a SharePoint Shortcut to OneDrive.

Both options essentially enable the same functionality allowing users to access SharePoint content from within File Explorer. Adding a SharePoint Shortcut to OneDrive is the promoted option to sync SharePoint content; as it allows for content to be accessed on all devices, whereas, a sync is related to a single device.

---

## References

- [Microsoft: SharePoint Sync](https://learn.microsoft.com/en-us/sharepoint/sharepoint-sync)
- [The DFIR Journal: SharePoint Sync](https://thedfirjournal.com/posts/sharepoint-sync/)