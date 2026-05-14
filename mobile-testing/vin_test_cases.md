# Test Cases — VIN Number Legal Check Feature

**Application:** Road Assistance Mobile App  
**Feature:** Vehicle Legal Check by VIN Number (integration with Avtoteka)  
**Type:** Functional, Manual  
**Author:** Svetlana Rakhmaeva  

---

## TC-011 — Successful report request with valid VIN number

**Preconditions:** User is logged in, user is on the main screen, internet connection is stable  
**Priority:** High  

| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Tap "Vehicle legal check" button on the main screen | VIN input screen opens |
| 2 | Enter valid VIN number (e.g. "XTA210990Y2793389", 17 characters) | VIN is entered correctly |
| 3 | Tap "Get report" button | Request is submitted |
| 4 | Navigate to "Vehicle legal check" section | New request is displayed in the list |
| 5 | Wait up to 5 minutes | Report is received and displayed in the list |
| 6 | Tap on the created request | PDF report opens successfully |

**Expected result:** Report is generated within 5 minutes and opens as PDF  
**Status:** Pass / Fail

---

## TC-012 — Submit form with empty VIN field

**Preconditions:** User is logged in, user is on the main screen  
**Priority:** High  

| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Tap "Vehicle legal check" button | VIN input screen opens |
| 2 | Leave VIN field empty | — |
| 3 | Tap "Get report" button | Error message is displayed: "Please enter VIN number" |

**Expected result:** Form is not submitted, validation error is shown  
**Status:** Pass / Fail

---

## TC-013 — Enter VIN number with less than 17 characters

**Preconditions:** User is logged in  
**Priority:** High  

| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Tap "Vehicle legal check" button | VIN input screen opens |
| 2 | Enter VIN with less than 17 characters (e.g. "XTA21099") | — |
| 3 | Tap "Get report" button | Error message: "VIN number must be 17 characters" |

**Expected result:** Form is not submitted, length validation error is shown  
**Status:** Pass / Fail

---

## TC-014 — Enter VIN number with more than 17 characters

**Preconditions:** User is logged in  
**Priority:** Medium  

| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Tap "Vehicle legal check" button | VIN input screen opens |
| 2 | Enter VIN with more than 17 characters (e.g. "XTA210990Y27933891234") | Field does not accept characters beyond 17, OR error is shown after tapping "Get report" |
| 3 | Tap "Get report" button | Error message: "VIN number must be 17 characters" |

**Expected result:** Input is restricted to 17 characters or validation error is shown  
**Status:** Pass / Fail

---

## TC-015 — Enter VIN number with invalid characters (letters I, O, Q)

**Preconditions:** User is logged in  
**Priority:** Medium  

| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Tap "Vehicle legal check" button | VIN input screen opens |
| 2 | Enter VIN containing letters I, O or Q (e.g. "XTA21O990Y279338") | — |
| 3 | Tap "Get report" button | Error message: "VIN number contains invalid characters" |

**Expected result:** Validation error is shown (I, O, Q are not allowed in VIN standard)  
**Status:** Pass / Fail

---

## TC-016 — Enter VIN number with special characters

**Preconditions:** User is logged in  
**Priority:** Medium  

| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Tap "Vehicle legal check" button | VIN input screen opens |
| 2 | Enter VIN with special characters (e.g. "XTA2109!0Y279338@") | — |
| 3 | Tap "Get report" button | Error message: "VIN number contains invalid characters" |

**Expected result:** Form is not submitted, validation error is shown  
**Status:** Pass / Fail

---

## TC-017 — Request report with no internet connection

**Preconditions:** User is logged in, internet connection is disabled  
**Priority:** High  

| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Disable internet connection on device | — |
| 2 | Tap "Vehicle legal check" button | Screen opens or error message appears |
| 3 | Enter valid VIN number | — |
| 4 | Tap "Get report" button | Error message: "No internet connection. Please try again later" |

**Expected result:** User is informed about connection issue, request is not sent  
**Status:** Pass / Fail

---

## TC-018 — Report is not received within 5 minutes

**Preconditions:** User is logged in, request has been submitted  
**Priority:** Medium  

| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Submit valid VIN request (see TC-011) | Request appears in the list |
| 2 | Wait more than 5 minutes | — |
| 3 | Observe request status in the list | Error status is shown OR user receives a notification with explanation |

**Expected result:** User is informed if report cannot be generated in time  
**Status:** Pass / Fail

---

## TC-019 — Verify PDF report opens and displays correctly

**Preconditions:** User is logged in, report has been received  
**Priority:** High  

| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Navigate to "Vehicle legal check" section | List of requests is displayed |
| 2 | Tap on a completed request | PDF report opens |
| 3 | Scroll through the PDF | Report content is readable, no blank pages or broken layout |

**Expected result:** PDF opens correctly and displays full report content  
**Status:** Pass / Fail

---

## TC-020 — Submit multiple VIN requests

**Preconditions:** User is logged in  
**Priority:** Low  

| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Submit first valid VIN request | Request appears in the list |
| 2 | Submit second valid VIN request with a different VIN | Second request appears in the list |
| 3 | Observe the list | Both requests are displayed separately with correct VIN numbers |

**Expected result:** Multiple requests are handled correctly and displayed in the list  
**Status:** Pass / Fail
