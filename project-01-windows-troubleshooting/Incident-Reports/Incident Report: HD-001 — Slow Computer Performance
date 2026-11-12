# Incident Report: HD-001 — Slow Computer Performance

**Ticket ID:** HD-001  
**Date:** November 12, 2026  
**Category:** Desktop Support / Performance  
**Priority:** Medium  
**Status:** Resolved (Simulated Lab Exercise)

## 1. User's Reported Issue

A simulated employee reported that their computer was running slowly, applications were taking a long time to open, and the computer occasionally froze.

The issue was affecting their ability to complete everyday work.

## 2. Environment

- Host machine: MacBook Pro M5
- Virtualization software: UTM 5.0.8
- Guest operating system: Windows 11 ARM64
- Allocated memory: 4 GB
- Environment: Local virtual machine

## 3. Troubleshooting Steps

**Step 1 — Initial resource investigation**

Opened Windows Task Manager and reviewed CPU, memory, disk, and running processes.

Initial observations:
- CPU utilization: 12%
- Memory utilization: 2.6 / 4 GB (65%)
- Disk utilization: 5%
- Highest resource-consuming process identified: wsappx

**Step 2 — Investigated background activity**

- Observed that wsappx resource usage decreased over time.
- Checked Windows Update and found updates downloading or installing.
- Checked Microsoft Store and found no active app updates.

**Step 3 — Investigated startup applications**

Reviewed Task Manager's Startup apps section.

- Identified Microsoft Edge as a high-impact startup application.
- Confirmed Edge was enabled at startup.
- Inspected Microsoft Edge system settings.
- Found Startup boost enabled.
- Found background applications permitted to run after Edge was closed.

**Step 4 — Applied troubleshooting changes**

- Disabled Microsoft Edge in Windows Startup apps.
- Disabled Microsoft Edge Startup boost.
- Disabled background extensions and applications running after Edge was closed.
- Restarted Windows to apply the changes.

## 4. Findings and Root Cause

The investigation identified unnecessary Microsoft Edge startup and background activity as a potential contributor to resource consumption.

Windows Update was also active during the investigation and may have contributed to temporary background resource usage.

The exact cause of the original reported slowdown could not be conclusively isolated because multiple background conditions were present.

## 5. Resolution

Disabled Microsoft Edge automatic startup and background activity.

After restarting the virtual machine, memory utilization decreased from 3.0 GB to 2.1 GB.

This represented a reduction of approximately 900 MB (30% relative to the initial measurement).

Microsoft Edge no longer launched automatically after sign-in.

## 6. Verification

Following the changes and restart:

- Memory utilization: 2.1 / 4 GB (52.5%)
- CPU utilization: 0% at the time of observation
- Disk utilization: 0% at the time of observation
- Microsoft Edge automatic startup: Disabled
- Observed performance: Noticeably faster

The user-reported performance improvement was confirmed through the post-change test.

## 7. Lessons Learned

- Used Task Manager to investigate system resource utilization.
- Learned how to identify high-impact startup applications.
- Investigated Windows background processes and update activity.
- Practiced controlled troubleshooting through before-and-after comparisons.
- Learned the importance of distinguishing a suspected cause from a confirmed root cause.
- Recognized that multiple background processes can influence system performance.

## 8. Tools Used

- Windows 11 Task Manager
- Windows Update
- Microsoft Edge system settings
- UTM virtualization software

## 9. Evidence

Supporting screenshots:
- Initial Task Manager resource utilization
- Startup applications and impact ratings
- Microsoft Edge system settings
- Post-restart Task Manager resource utilization

---

**Project:** IT Help Desk Home Lab  
**Exercise:** HD-001 — Windows Performance Troubleshooting  
**Result:** Completed
