# Test Cases — Support Chat

**Application:** Road Assistance Mobile App (Admin Panel)  
**Feature:** Support Chat with Users  
**Type:** Functional, Manual  
**Author:** Svetlana Rakhmaeva

---

## TC-ADMIN-CHAT-001 — Receive a new message from a user

**Preconditions:** Operator is logged in. A user has sent a message via the in-app support chat.  
**Priority:** Critical

| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Navigate to the "Support Chat" section | The section opens |
| 2 | Check the conversation list | A new conversation appears marked as "New": user name, message preview, and timestamp are visible. The unread counter has increased |

---

## TC-ADMIN-CHAT-002 — Operator replies to a user message

**Preconditions:** A conversation is open with at least one incoming message.  
**Priority:** Critical

| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Open the conversation with the user | The conversation opens; the incoming message is visible |
| 2 | Type a reply in the input field | Text is entered correctly |
| 3 | Click "Send" or press Enter | The message is displayed in the chat on the operator's side |
| 4 | Verify delivery in the mobile app | The user received the reply; the message status shows "Delivered" |

---

## TC-ADMIN-CHAT-003 — Send an empty message

**Preconditions:** A conversation is open.  
**Priority:** Medium

| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Leave the input field empty | The "Send" button is inactive |
| 2 | Click "Send" or press Enter | The message is not sent; no notification is triggered for the user |

---

## TC-ADMIN-CHAT-004 — View message history

**Preconditions:** The user has a conversation history of more than 20 messages.  
**Priority:** Medium

| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Open the conversation | Message history is displayed in chronological order |
| 2 | Scroll up | Older messages load progressively (lazy loading) |
| 3 | Check the visual distinction between messages | Operator and user messages are visually different |

---

## TC-ADMIN-CHAT-005 — Search conversation by user name

**Preconditions:** Multiple conversations exist in the system.  
**Priority:** Medium

| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Enter a full user name in the search field | The correct conversation is found |
| 2 | Enter a partial name | All matching conversations are displayed |
| 3 | Enter a name that does not exist | Message "Nothing found" is displayed |

---

## TC-ADMIN-CHAT-006 — Close a support conversation

**Preconditions:** A conversation is open with status "In progress".  
**Priority:** Medium

| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Click "Close conversation" | Status changes to "Resolved"; the conversation moves to the archive |
| 2 | Attempt to send a message in the closed conversation | A warning is displayed or the input field is disabled |

---

## TC-ADMIN-CHAT-007 — Handle multiple simultaneous conversations

**Preconditions:** Several users have written to support at the same time.  
**Priority:** High

| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Open conversation with user A, type a message (do not send) | Text is entered |
| 2 | Switch to conversation with user B | Context of conversation A is preserved |
| 3 | Return to conversation with user A | The draft message is still in the input field. New incoming messages in the background are indicated by a counter |

---

## TC-ADMIN-CHAT-008 — Receive notification about a new message from another section

**Preconditions:** Operator is in the "Orders" section. A user sends a message in the chat.  
**Priority:** High

| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Stay in the "Orders" section (not in chat) | — |
| 2 | Wait for a new incoming message | A notification appears (toast or badge on the chat icon); the unread counter increases |
| 3 | Click the notification | The correct conversation opens |
