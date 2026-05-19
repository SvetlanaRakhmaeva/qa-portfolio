# Test Cases — Evacuation Order Management

**Application:** Road Assistance Mobile App (Admin Panel)  
**Feature:** Evacuation Order Management  
**Type:** Functional, Manual  
**Author:** Svetlana Rakhmaeva

---

## TC-ADMIN-EVA-001 — New order appears in the list

**Preconditions:** Operator is logged in with the "Support" role. A user has submitted an evacuation request in the mobile app.  
**Priority:** High

| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Navigate to the "Evacuation Orders" section | The section opens, the order list is displayed |
| 2 | Check whether the new order has appeared in the list | The order is displayed with status "New" and includes: user name, phone number, address, and creation time. New orders are visually highlighted |

---

## TC-ADMIN-EVA-002 — View full order details

**Preconditions:** At least one order exists in the list.  
**Priority:** High

| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Click on an order in the list | The order card opens |
| 2 | Review the card content | Full details are shown: full name, phone number, address, user comment, geolocation on map |
| 3 | Check available action buttons | Buttons are present: "Take in progress", "Send to evacuation department", "Reject" |

---

## TC-ADMIN-EVA-003 — Send order to evacuation department

**Preconditions:** The order has status "New" or "In progress".  
**Priority:** Critical

| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Open the order card | The card opens |
| 2 | Click "Send to evacuation department" | A confirmation dialog appears |
| 3 | Confirm the action | Order status changes to "Sent to evacuation" |
| 4 | Review the updated order card | The card shows: operator name and timestamp of the transfer. The "Send" button is now disabled |

---

## TC-ADMIN-EVA-004 — Attempt to re-send an already transferred order

**Preconditions:** The order has status "Sent to evacuation".  
**Priority:** High

| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Open the order card with status "Sent to evacuation" | The card opens |
| 2 | Check the state of the "Send to evacuation department" button | The button is disabled or hidden |
| 3 | Attempt to click the button | Re-sending is not possible |

---

## TC-ADMIN-EVA-005 — Filter orders by status

**Preconditions:** Orders with different statuses exist in the system.  
**Priority:** Medium

| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Apply the filter "New" | Only orders with status "New" are displayed |
| 2 | Apply the filter "In progress" | Only orders with status "In progress" are displayed |
| 3 | Apply the filter "Sent to evacuation" | Only transferred orders are displayed |
| 4 | Reset all filters | All orders are displayed; the counter is updated |

---

## TC-ADMIN-EVA-006 — Display geolocation on the map

**Preconditions:** The user shared their geolocation when submitting the order.  
**Priority:** Medium

| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Open an order card that includes geolocation | A map marker is shown at the user's location; the map is zoomable |
| 2 | Open an order card without geolocation | A text address is displayed with the message "Geolocation unavailable" |

---

## TC-ADMIN-EVA-007 — Handle order submission with no internet connection

**Preconditions:** The operator has the order card open.  
**Priority:** High

| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Open the order card | The card opens |
| 2 | Disable internet on the device | — |
| 3 | Click "Send to evacuation department" | A network error message is displayed. The order status has not changed |
| 4 | Restore internet connection and retry | Data is preserved; the action completes successfully |
