# Test Plan — Road Assistance Mobile App

**Application:** Road Assistance Mobile App  
**Platforms:** iOS, Android  
**Author:** Svetlana Rakhmaeva  
**Type:** Manual Testing

---

## 1. Introduction

This test plan covers manual testing of the Road Assistance mobile application. Testing is performed independently within a single sprint.

**Features in scope:**

- Vehicle Legal Check by VIN
- Alcohol Calculator
- Evacuator Request
- Document Generator
- Accident Scheme Builder

---

## 2. Objectives

- Verify that each feature works according to the requirements
- Find bugs before users encounter them
- Ensure forms validate input correctly and handle invalid data
- Verify consistent behavior across iOS and Android platforms

---

## 3. Testing Types

| Type | Purpose |
|------|---------|
| Functional | Verify features work according to requirements |
| UI/UX | Ensure the interface matches the design mockups |
| Negative | Verify behavior with invalid or edge-case input |
| Regression | Ensure that fixes do not break existing functionality |
| Smoke | Quickly verify a new build before full test cycle |
| Exploratory | Free-form testing without scripts to find unexpected issues |

---

## 4. Test Environment

| Parameter | Value |
|-----------|-------|
| iOS devices | iPhone 12, iPhone 14 — iOS 15+ |
| Android devices | Samsung Galaxy S21, Xiaomi Redmi Note 11 — Android 11+ |
| Network | Wi-Fi and 4G |
| Tools | Jira, Zephyr, Postman, Charles Proxy |

Primary testing is performed on real devices. Emulators are used as a supplementary tool.

---

## 5. Module Priorities

| Module | Priority | Reason |
|--------|----------|--------|
| Evacuator Request | High | Critical feature, depends on external service |
| Vehicle Legal Check (VIN) | High | External API integration, multiple failure points |
| Document Generator | Medium | Important but less frequently used |
| Alcohol Calculator | Medium | Standalone feature, lower risk |
| Accident Scheme Builder | Low | Complex but non-critical functionality |

---

## 6. Entry Criteria

- Build is delivered and installed on test devices
- Test cases are written and reviewed
- Test environment is up and running
- Blocking bugs from the previous cycle are fixed

---

## 7. Exit Criteria

- All high priority test cases are executed
- No open critical or blocking bugs
- Medium and low priority bugs are logged in Jira and scheduled
- Smoke test after the last fix is passed

---

## 8. Risks

| Risk | Mitigation |
|------|------------|
| Requirements change during the sprint | Update test cases after each grooming session |
| Build is delivered late | Use the time to write documentation |
| Test device unavailable | Use an emulator as a temporary replacement |
| External service unavailable in test environment | Coordinate with the developer to set up a mock |

---

## 9. Test Artifacts

- Checklists — `checklist.md`
- Test cases — `evacuator_test_cases.md`, `vin_check_test_cases.md`
- Bug reports — logged in Jira
- Test summary report — provided at the end of the sprint
