# Checklist — Functional Testing

**Application:** Road Assistance Mobile App  
**Author:** Svetlana Rakhmaeva  
**Type:** Functional, Manual  
**Platforms:** iOS, Android

---

## 1. Vehicle Legal Check by VIN Number

- [ ] VIN input field is present on the screen
- [ ] Field accepts exactly 17 characters
- [ ] Field does not accept fewer than 17 characters
- [ ] Field does not accept more than 17 characters
- [ ] Field does not accept letters I, O, Q (not allowed in VIN standard)
- [ ] Field accepts Latin letters and digits
- [ ] Field does not accept special characters
- [ ] Valid VIN returns correct check result
- [ ] Invalid VIN displays an error message
- [ ] Result contains legal information about the vehicle
- [ ] "Check" button is inactive when the field is empty
- [ ] No internet connection: correct error message is displayed

---

## 2. Alcohol Calculator

- [ ] Calculator form is displayed correctly
- [ ] Fields are present: gender, weight, drink type, volume, alcohol percentage
- [ ] Weight field accepts only numeric values
- [ ] Weight field does not accept negative values or zero
- [ ] Drink type selection works correctly (dropdown / buttons)
- [ ] Volume field accepts only numeric values
- [ ] Alcohol percentage field accepts only numeric values
- [ ] Result is displayed after all fields are filled in
- [ ] Result recalculates when input data changes
- [ ] Alcohol elimination time is displayed
- [ ] Empty required fields trigger a validation error
- [ ] Warning is displayed that the result is approximate

---

## 3. Evacuator Request

- [ ] "Order service" button is present on the main screen
- [ ] Dropdown list opens on tap
- [ ] "Evacuator request" option is present in the list
- [ ] Form opens after selecting the service
- [ ] Fields are present: Name, Phone, Email
- [ ] Name field does not accept digits or special characters
- [ ] Phone field accepts correct phone number format
- [ ] Phone field does not accept letters
- [ ] Email field validates correct format (requires @ and domain)
- [ ] "Order" button is inactive when required fields are empty
- [ ] Confirmation modal appears after successful submission
- [ ] Modal closes correctly
- [ ] Form is not re-submitted on repeated button tap

---

## 4. Document Generator

- [ ] "Document generator" section opens correctly
- [ ] List of available document types is displayed
- [ ] Document type selection works correctly
- [ ] All required form fields are present
- [ ] Required fields are validated before generation
- [ ] Empty required fields trigger a validation error
- [ ] Document is generated after all fields are filled in
- [ ] Generated document is available for download or preview
- [ ] Document format is correct (PDF / DOCX)
- [ ] User data is correctly inserted into the document
- [ ] Re-generating with the same data produces an identical result

---

## 5. Accident Scheme Builder

- [ ] "Accident scheme" section opens correctly
- [ ] Scheme building tools are present on the screen
- [ ] Adding road elements (lanes, intersections) works correctly
- [ ] Adding traffic signs works correctly
- [ ] Adding participants (cars, pedestrians) works correctly
- [ ] Elements can be moved on the scheme
- [ ] Elements can be deleted
- [ ] Undo last action works correctly
- [ ] Scheme supports zoom in / zoom out
- [ ] Completed scheme can be saved
- [ ] Completed scheme can be exported (PNG, PDF)
- [ ] Saved scheme opens correctly on re-entry
