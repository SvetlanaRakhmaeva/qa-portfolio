# Admin Panel — QA Documentation

**Application:** Road Assistance Mobile App (Admin Panel)  
**Author:** Svetlana Rakhmaeva  
**Type:** Manual Testing

---

## Overview

The admin panel is an internal web interface for support operators. It is integrated with the mobile app: evacuation orders submitted by users arrive in the panel in real time, and operators communicate with users through a built-in support chat.

```
User (mobile app)
      |
      |-- Submits evacuation order --> Orders list in admin panel
      |                                      |
      |                               Operator forwards
      |                               to evacuation department
      |
      |-- Writes to support chat  --> Operator chat in admin panel
```

---

## Repository Structure

```
admin-panel/
├── test-cases/
│   ├── TC_ADMIN_evacuation_orders.md   # 7 test cases
│   └── TC_ADMIN_support_chat.md        # 8 test cases
└── bug-reports/
    └── BUG_ADMIN_panel.md              # 4 bug reports
```

---

## Coverage

| Module                    | Test Cases | Bug Reports |
|---------------------------|:----------:|:-----------:|
| Evacuation Order Management | 7        | 2           |
| Support Chat              | 8          | 2           |
| **Total**                 | **15**     | **4**       |

---

## Test Environment

| Parameter     | Value |
|---------------|-------|
| Browsers      | Chrome 124, Firefox 125 |
| OS            | Windows 10 |
| Environment   | Production |
| Testing types | Functional, Integration, Negative |
