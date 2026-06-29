# [Sample / Case Name]

**Date:** YYYY-MM-DD
**Analyst:** Luca Leuenberger
**Type:** Malware analysis | Disk forensics | Memory forensics | Network forensics
**Status:** Draft | Complete

---

## 1. Summary

One short paragraph: what this is, how it behaves, and the single most important takeaway.
Write this section *last*, once you know the story.

## 2. Sample / evidence metadata

| Field | Value |
|-------|-------|
| File name | |
| File type | |
| Size | |
| SHA-256 | |
| Source | _e.g. MalwareBazaar, NIST CFReDS, Digital Corpora, own capture_ |
| Acquired / first seen | |

## 3. Static analysis

File structure (PE/ELF headers, sections, imports/exports), notable strings, signs of
packing or obfuscation, embedded resources, and capabilities (`capa`). Everything you can
determine **without executing** the sample.

## 4. Dynamic / behavioral analysis

> Environment: isolated VM, host-only/no network, snapshot reverted before the run.

What it does at runtime: processes spawned, files dropped, registry/persistence changes,
network callbacks, anti-analysis/evasion behavior. Add screenshots where they help.

## 5. Indicators of compromise (defanged)

- **Network:** `hxxp://bad[.]example[.]com`, `185[.]100[.]87[.]xx`
- **Host:** file paths, mutexes, registry keys, scheduled tasks, service names
- **Hashes:** dropped or related files (SHA-256)

## 6. MITRE ATT&CK mapping

| Tactic | Technique | ID | Evidence |
|--------|-----------|----|----------|
| Persistence | Scheduled Task/Job | T1053.005 | |
| | | | |

## 7. Detection

A YARA rule, Sigma rule, or hunting query that would catch this behavior. Detection logic
only — no offensive code.

## 8. Conclusion

Your assessment: family/attribution if known, severity, and what you learned from the case.

## 9. References

Links to public reports, sandbox results, and related samples.
