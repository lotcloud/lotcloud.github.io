---
layout: technique
title: Mailbox Synchronization
mitre_id: T1114.002
tactics:
  - Collection
platforms:
  - M365
tags:
  - Exchange
  - Outlook
  - Data Exfiltration
---

## Overview

The Outlook desktop application includes a productivity feature known as mailbox synchronization. By default, when a user signs in to the Outlook desktop application, a copy of their mailbox is downloaded to the local device to support offline access. A Threat Actor may leverage this feature to obtain a local copy of a mailbox. Even when containment measures have been applied the Threat Actor will retain all items synchronized. 

---

## How Synchronization Works

When a user signs in to the Outlook desktop application, synchronization occurs by downloading the contents of the mailbox to a file known as an Offline Outlook Data File (OST). Once the download is complete, a Threat Actor can navigate to the OST files location, which would contain a full local copy of the mailbox's contents. 

**OST file location:** 
- Windows: `C:\Users\<username>\AppData\Local\Microsoft\Outlook\`

## How to Identify Synchronization

Mailbox synchronization will generate MailItemsAccessed operations in the Unified Audit Log. Synchronization events can be identified by reviewing the Unified Audit Logs of the impacted user for MailItemsAccessed Operations where the mail access type is recorded as sync and the event is attributed to the unauthorized activity.  

As per Microsoft's guidance, all items within a synced folder should be considered impacted:  
> Assume that all mail items in the synched folder are compromised.

Example Unified Audit Log Entry: 
```
CreationTime:2025-11-01T13:03:36
Operation: MailItemsAccessed
ClientIP: 181.210...
SessionId: a7f8c2e1...
UserID: executive@company.onmicrosoft.com
ClientProcessName: OUTLOOK.EXE
MailboxOwnerUPN: Mailbox Owner UPN
MailAccessType: Sync
ParentFolder:{"Id":"AAMkAGZm...","Name":"Inbox","Path":"Not Available"}
```


## References

- [MITRE ATT&CK T1114.002](https://attack.mitre.org/techniques/T1114/002/)
- [Use MailItemsAccessed to investigate compromised accounts](https://learn.microsoft.com/en-us/purview/audit-log-investigate-accounts#auditing-sync-access)
