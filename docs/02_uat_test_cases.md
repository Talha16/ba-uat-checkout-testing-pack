# UAT Test Cases – Checkout Flow

## Legend
- Priority: High / Medium / Low
- Result: Pass / Fail / Blocked

---

## TC-001: Proceed to Checkout (Cart Has Items)
**Priority:** High  
**Preconditions:** Cart contains at least 1 item  
**Steps:**
1. Navigate to cart page
2. Click “Proceed to Checkout”
**Expected Result:**
- User is directed to checkout entry step (sign-in/guest choice)

---

## TC-002: Prevent Checkout (Empty Cart)
**Priority:** High  
**Preconditions:** Cart is empty  
**Steps:**
1. Navigate to cart page
2. Click “Proceed to Checkout”
**Expected Result:**
- System displays message indicating cart is empty
- User cannot proceed to checkout

---

## TC-003: Guest Checkout Option Available
**Priority:** High  
**Preconditions:** Cart contains at least 1 item  
**Steps:**
1. Start checkout
2. Select “Continue as Guest”
**Expected Result:**
- User is taken to Shipping Address step without account creation

---

## TC-004: Shipping Address Required Field Validation
**Priority:** High  
**Preconditions:** User is on Shipping Address step  
**Steps:**
1. Leave required fields blank (e.g., city, postal code)
2. Click “Continue”
**Expected Result:**
- Field-level error messages appear
- User cannot proceed until corrected

---

## TC-005: Shipping Method Displayed After Valid Address
**Priority:** High  
**Preconditions:** Valid shipping address entered  
**Steps:**
1. Continue to Shipping Method step
**Expected Result:**
- Shipping options display with cost and delivery estimate

---

## TC-006: Payment Validation – Invalid Card Format
**Priority:** High  
**Preconditions:** User is on Payment step  
**Steps:**
1. Enter invalid card number format
2. Attempt to continue/place order
**Expected Result:**
- Validation error message displayed
- User remains on Payment step

---

## TC-007: Payment Authorization Failure Handling (Conceptual)
**Priority:** High  
**Preconditions:** Payment authorization returns “Declined”  
**Steps:**
1. Attempt to place order
**Expected Result:**
- User sees a generic retry message (no technical codes)
- Order is not confirmed

---

## TC-008: Order Review Displays Correct Summary
**Priority:** Medium  
**Preconditions:** Shipping and payment details provided  
**Steps:**
1. Navigate to Order Review
**Expected Result:**
- Items, shipping method, taxes, and total are visible
- User can return to edit details

---

## TC-009: Order Confirmation Displays Order ID
**Priority:** High  
**Preconditions:** Payment succeeds  
**Steps:**
1. Place order
**Expected Result:**
- Confirmation page shows success message and order ID
