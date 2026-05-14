# Test Cases — Evacuator Request Feature

**Application:** Road Assistance Mobile App  
**Feature:** Evacuator Request  
**Type:** Functional, Manual  
**Author:** Svetlana Rakhmaeva  

---

## TC-001 — Successful evacuator request with valid data

**Preconditions:** User is logged in, internet connection is stable  
**Priority:** High  

| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Tap "Order service" button on the main screen | Dropdown list appears with available services |
| 2 | Tap "Evacuator request" in the dropdown list | Form opens with fields: Name, Phone, Email |
| 3 | Enter valid name (e.g. "Anna Ivanova") | Name is entered correctly |
| 4 | Enter valid phone number (e.g. "+7 900 123-45-67") | Phone number is entered correctly |
| 5 | Enter valid email (e.g. "test@mail.ru") | Email is entered correctly |
| 6 | Tap "Order" button | Modal window appears: "We have received your request. Please wait for a call" |

**Expected result:** Request is submitted successfully, modal confirmation is displayed  
**Status:** Pass / Fail

---

## TC-002 — Submit form with empty Name field

**Preconditions:** User is logged in  
**Priority:** High  

| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Tap "Order service" → "Evacuator request" | Form opens |
| 2 | Leave Name field empty | — |
| 3 | Fill in valid Phone and Email | — |
| 4 | Tap "Order" button | Error message is displayed under Name field (e.g. "This field is required") |

**Expected result:** Form is not submitted, validation error is shown  
**Status:** Pass / Fail

---

## TC-003 — Submit form with empty Phone field

**Preconditions:** User is logged in  
**Priority:** High  

| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Tap "Order service" → "Evacuator request" | Form opens |
| 2 | Fill in valid Name and Email | — |
| 3 | Leave Phone field empty | — |
| 4 | Tap "Order" button | Error message is displayed under Phone field |

**Expected result:** Form is not submitted, validation error is shown  
**Status:** Pass / Fail

---

## TC-004 — Submit form with empty Email field

**Preconditions:** User is logged in  
**Priority:** High  

| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Tap "Order service" → "Evacuator request" | Form opens |
| 2 | Fill in valid Name and Phone | — |
| 3 | Leave Email field empty | — |
| 4 | Tap "Order" button | Error message is displayed under Email field |

**Expected result:** Form is not submitted, validation error is shown  
**Status:** Pass / Fail

---

## TC-005 — Submit form with invalid email format

**Preconditions:** User is logged in  
**Priority:** Medium  

| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Tap "Order service" → "Evacuator request" | Form opens |
| 2 | Fill in valid Name and Phone | — |
| 3 | Enter invalid email (e.g. "testmail.ru" or "test@" or "test") | — |
| 4 | Tap "Order" button | Error message: "Enter a valid email address" |

**Expected result:** Form is not submitted, email validation error is shown  
**Status:** Pass / Fail

---

## TC-006 — Submit form with invalid phone number format

**Preconditions:** User is logged in  
**Priority:** Medium  

| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Tap "Order service" → "Evacuator request" | Form opens |
| 2 | Fill in valid Name and Email | — |
| 3 | Enter invalid phone (e.g. "abc", "123", "++79001234567") | — |
| 4 | Tap "Order" button | Error message: "Enter a valid phone number" |

**Expected result:** Form is not submitted, phone validation error is shown  
**Status:** Pass / Fail

---

## TC-007 — Submit form with no internet connection

**Preconditions:** User is logged in, internet connection is disabled  
**Priority:** High  

| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Disable internet connection on device | — |
| 2 | Tap "Order service" → "Evacuator request" | Form opens (or error screen appears) |
| 3 | Fill in all fields with valid data | — |
| 4 | Tap "Order" button | Error message: "No internet connection. Please try again later" |

**Expected result:** User is informed about connection issue, request is not sent  
**Status:** Pass / Fail

---

## TC-008 — Close dropdown without selecting a service

**Preconditions:** User is logged in  
**Priority:** Low  

| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Tap "Order service" button | Dropdown list appears |
| 2 | Tap outside the dropdown or press Back | Dropdown closes |

**Expected result:** Dropdown closes, user returns to main screen, no errors  
**Status:** Pass / Fail

---

## TC-009 — Submit form with Name containing special characters

**Preconditions:** User is logged in  
**Priority:** Low  

| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Tap "Order service" → "Evacuator request" | Form opens |
| 2 | Enter name with special characters (e.g. "Anna!!!", "<script>") | — |
| 3 | Fill in valid Phone and Email | — |
| 4 | Tap "Order" button | Error message or special characters are stripped |

**Expected result:** Application handles special characters safely without crashing  
**Status:** Pass / Fail

---

## TC-010 — Verify modal window closes correctly after confirmation

**Preconditions:** User is logged in, internet connection is stable  
**Priority:** Medium  

| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Complete successful evacuator request (see TC-001) | Modal window is displayed |
| 2 | Tap "Close" or "OK" button on modal | Modal closes |
| 3 | Observe current screen | User returns to main screen |

**Expected result:** Modal closes correctly, app returns to main screen without errors  
**Status:** Pass / Fail
