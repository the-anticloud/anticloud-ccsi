# How to Update — CCSI

**Project:** `CCSI`
**Category:** CARBON_CAPTURE
**Domain:** carbon capture, utilization, and storage
**Date:** 2026-10-07

---

## Update Procedure

### Checking for Updates
```bash
CCSI --version
CCSI check-update
```

### Applying Updates
```bash
pip install --upgrade CCSI
```

### Rolling Back
```bash
pip install CCSI==<previous-version>
```

### Update Policy
- **Security updates:** Applied immediately
- **Feature updates:** Monthly release cycle
- **Breaking changes:** 6-month deprecation notice

## Verification

All 16 checks PASS. Evidence: `ISOLATED_LAB_RESULTS/03_Result_Register.md`.
