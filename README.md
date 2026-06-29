# DFIR & Malware Analysis Lab

A personal lab notebook documenting my work in **digital forensics** and **malware
analysis**: investigation writeups, methodology, and the tooling I build along the way.

> **Important:** This repository contains **analysis and reports only**. No live malware
> samples are stored here. Samples are referenced by SHA-256 hash and obtained from
> legitimate research sources. All indicators of compromise (IOCs) in writeups are defanged
> (e.g. `hxxp://`, `evil[.]com`) so nothing is accidentally clickable or executable.

## Index

| Date | Case | Type | Key tools | Writeup |
|------|------|------|-----------|---------|
| YYYY-MM-DD | _e.g. Scheduled-task persistence on a Windows image_ | Disk forensics | Autopsy, EZ Tools, RegRipper | [link](writeups/) |
| YYYY-MM-DD | _e.g. Static triage of an unknown PE_ | Malware (static) | DIE, PEStudio, capa | [link](writeups/) |

## Lab setup

All **dynamic** analysis runs in an isolated virtual machine: host-only / no internet,
with a clean snapshot taken before every run and reverted after. Static analysis and
forensic imaging never touch my main system.

- Analysis VMs: REMnux (Linux) and a Windows VM (e.g. FLARE-VM)
- Network containment: host-only adapter; INetSim / FakeNet-NG to simulate services
- Snapshot → run → observe → revert, every single time

## Toolbox

- **Forensics:** Autopsy, The Sleuth Kit, Volatility 3, Eric Zimmerman's Tools, RegRipper, plaso/log2timeline, Wireshark, FTK Imager
- **Malware (static):** Detect It Easy, PEStudio, CFF Explorer, FLARE `capa` & `FLOSS`, `strings`, YARA
- **Malware (dynamic):** Process Monitor, System Informer, Wireshark, INetSim, CAPE/Cuckoo sandbox

## Responsible use

Everything here is for **defensive research and education**. Samples are handled only in a
contained environment and never redistributed. Forensic images come from sanctioned,
publicly available datasets — no real-world PII or confidential case data.

## About

Maintained by **Luca Leuenberger** — application developer (Informatiker EFZ) with a focus
on application security and digital forensics.
