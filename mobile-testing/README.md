# Mobile Testing — QA Documentation

**Application:** Road Assistance Mobile App  
**Author:** Svetlana Rakhmaeva  
**Type:** Functional, Manual  
**Platforms:** iOS, Android

---

## Overview

Mobile application for drivers with the following features: evacuator request, vehicle legal check by VIN number (integration with Avtoteka), alcohol calculator, accident scheme builder, and document generation.

---

## Repository Structure

```
mobile-testing/
├── evacuator_test_cases.md       # 10 test cases
└── vin_check_test_cases.md       # 10 test cases
```

---

## Coverage

| Feature | File | Test Cases |
|---------|------|:----------:|
| Evacuator Request | evacuator_test_cases.md | 10 |
| Vehicle Legal Check (VIN) | vin_check_test_cases.md | 10 |
| **Total** | | **20** |

---

## Test Environment

| Parameter | Value |
|-----------|-------|
| Platforms | iOS, Android |
| Testing type | Functional, Manual |
| Test case IDs | TC-001 — TC-020 |
| Integrations covered | Avtoteka (VIN report generation) |
