# Bug Reports — Admin Panel

**Application:** Road Assistance Mobile App (Admin Panel)  
**Author:** Svetlana Rakhmaeva  
**Environment:** Chrome 124 / Firefox 125, Windows 10, Production

---

## BUG-ADMIN-001 — Order status does not update without page reload

**Module:** Evacuation Order Management  
**Severity:** Major  
**Priority:** High  
**Status:** Open

**Preconditions:** Two operators are working simultaneously. One operator changes an order status to "Sent to evacuation".

**Steps to Reproduce:**

| Step | Action |
|------|--------|
| 1 | Open the evacuation orders list |
| 2 | Have a colleague (or open a second tab) change the order status to "Sent to evacuation" |
| 3 | Return to the orders list without reloading the page |
| 4 | Find that same order in the list |

**Expected Result:** The list updates automatically in real time (WebSocket / polling) — the status "Sent to evacuation" is visible without manual refresh.

**Actual Result:** The order status in the list remains "New". The operator does not see the change and may re-send an already processed order.

**Impact:** Critical when multiple operators work simultaneously — high risk of duplicate order processing.

---

## BUG-ADMIN-002 — "Send to evacuation department" button is active for already transferred orders

**Module:** Evacuation Order Management  
**Severity:** Major  
**Priority:** High  
**Status:** Open

**Preconditions:** An order with status "Sent to evacuation" exists in the system.

**Steps to Reproduce:**

| Step | Action |
|------|--------|
| 1 | Find an order with status "Sent to evacuation" |
| 2 | Open the order card |
| 3 | Check the state of the "Send to evacuation department" button |
| 4 | Click the button |

**Expected Result:** The button is disabled or hidden — re-sending the order is not possible.

**Actual Result:** The button is active. Clicking it sends the order to the evacuation department a second time.

**Impact:** Duplicate orders in the evacuation department, causing confusion during processing.

---

## BUG-ADMIN-003 — Draft message is lost when switching between conversations

**Module:** Support Chat  
**Severity:** Minor  
**Priority:** Medium  
**Status:** Open  
**Browser:** Firefox 125

**Preconditions:** Operator has multiple conversations open.

**Steps to Reproduce:**

| Step | Action |
|------|--------|
| 1 | Open a conversation with user A |
| 2 | Type a reply in the input field — do not send |
| 3 | Switch to a conversation with user B |
| 4 | Return to the conversation with user A |

**Expected Result:** The typed text is preserved as a draft and displayed in the input field upon return.

**Actual Result:** The input field is empty — the typed text is lost.

---

## BUG-ADMIN-004 — Unread message counter does not reset after reading

**Module:** Support Chat  
**Severity:** Minor  
**Priority:** Medium  
**Status:** Open

**Preconditions:** Operator has received a new message (counter = 1).

**Steps to Reproduce:**

| Step | Action |
|------|--------|
| 1 | Wait for a new incoming message (counter shows 1) |
| 2 | Open the conversation and read the message |
| 3 | Return to the conversation list |

**Expected Result:** The unread message counter resets to 0 after the conversation is opened.

**Actual Result:** The counter remains at "1" — it does not reset automatically.
