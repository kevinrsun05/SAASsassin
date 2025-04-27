# 🌟 SAASsassin - A Open-Source SaaS Hosting Project

**By:** Alex Zheng, Audrey Wong, Nathan Zhang, Kevin Sun

## About the Project
Software-as-a-Service (SaaS) subscriptions drain thousands of dollars every year from companies, startups, and student groups. Tools like Slack, GitHub, Notion, and Zoom started as ways to make software easier to use — but over time, they became costly rental services that limit control, privacy, and financial flexibility.

This project solves this problem by self-hosting powerful, open-source alternatives to common SaaS tools on our own server.
By doing this, we help startups, student groups, and individuals save thousands of dollars while maintaining full ownership and control over their data and software.

We built a complete free alternative "workspace" that covers everything from real-time communication to version control, project management, cloud storage, document editing, and video conferencing — without a single recurring SaaS fee.

## How to install the Project
To install the project, you must first download the VM file. Before jumping to this, please read the following disclaimer:
- A. This is a 55GB .vma.zst file that is the entire VM and it's datapool. You should only be downloading this if you have a hypervisor readily avaliable to test it on.
- B. Current configuration of the backup is 12 CPUs, 24GB of RAM, and a 300GB disk. If you do not have these free resources on your hypervisor, then it may fail to properly spin up. If you contact Alex he can customize a configuration for you.
- C. Due to limited bandwidth and to avoid attacks, the download is protected by a password. Please reach out to Alex (alexzheng2004@gmail.com) for the username and password if you need to download this file.

Download the file:
```scp -P 5300 user@tinycv.art:/home/user/vzdump-qemu-copy.vma.zst```

Upload the file to your Hypervisor:
```scp [yourUSER]@[yourHypervisorIP]:/var/lib/vz/dump/vzdump-qemu-copy.vma.zst```
- /var/lib/vz/dump/vzdump-qemu-copy.vma.zst is the default backup location on Proxmox, may be different from hypervisor to hypervisor.
- Replace [yourUser] and [yourHypervisorIP] with your username (root works best!) and your hypervisor IP respectively. Or, scp the file directly to your hypervisor!

Restore the VM from the backup:
```qmrestore /var/lib/vz/dump/vzdump-qemu-copy.vma.zst [VMID-number] \--storage [storage-name]```
- replace [VMID-number] with the id number you would like to assign to the VM
- replace [storage-name] where the disks will live. This is local-lvm for me.

## 🔥 Hosted Applications and Details

- Note: a lot of these still require an admins approval, so you may or may not be able to create an account. Definitely check out the Mattermost application for starters.

### 1. Gitea - Source Code Hosting & Collaboration
*Paid SaaS equivalent:* GitHub / GitLab.com

*URL:* http://tinycv.art:3000/

### 2. Mattermost - Real-Time Chat & Collaboration
*Paid SaaS equivalent:* Slack

*URL:* http://tinycv.art:8065/signup_user_complete/?id=qdeh3f3m4pd1xeizz6rhisgkxy

### 3. Taiga - Project & Issue Tracking
*Paid SaaS equivalent:* Jira Cloud / Asana

*URL:* http://tinycv.art:9000/

### 4. Jitsi Meet - Video Conferencing
*Paid SaaS equivalent:* Zoom / Google Meet

*URL:* https://tinycv.art:7443

### 5. NocoDB - Spreadsheet Database
*Paid SaaS equivalent:* Airtable

*URL:* http://tinycv.art:8085

### 6. Docuseal
*Paid SaaS equivalent:* Docusign

*URL:* http://tinycv.art:3010/

### 7. NextCloud - File Sync, Sharing & Document Collaboration
*Paid SaaS equivalent:* Google Drive / Dropbox / Microsoft 365

*URL:* http://tinycv.art:8180/login

### 8. AppFlowy - Workspace & Documentation
*Paid SaaS equivalent:* Notion

*URL:* http://tinycv.art:3010/

### 9. Jenkins - CI/CD Automation
*Paid SaaS equivalent:* GitHub Actions / CircleCI

*URL:* http://tinycv.art:8080/

### 10. Penpot - UI/UX Design & Prototyping
*Paid SaaS equivalent:* Figma

*URL:* http://tinycv.art:9005

### 11. Cal.com
*Paid SaaS equivalent:* Calendly

*URL:* http://tinycv.art:3020/

### 12. Wekan - Kanban Task Management
*Paid SaaS equivalent:* Trello

*URL:* http://tinycv.art:3200



