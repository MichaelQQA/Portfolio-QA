**Title**

Cart crashes 

**Description**

Cart page crashes when the user types a 3-digit number into the quantity field and then clicks anywhere outside the input.
The UI does not show any maximum quantity limit or validation message, so the user gets no guidance and the page fails instead of handling the input safely.

**Priority**

P2 – Major

**Environment**

*Device: PC
*OS: Windows 11
*Browser: Chrome

**Steps to Reproduce**

*Open the website: https://shield-germany.de
*Open any product page (click any product).
*Add the product to the cart.
*In the side cart menu, click “ZUM WARENKORB”.
*In the product quantity field, type a 3-digit value (e.g., 999).
*Click anywhere outside the quantity input (an empty area on the page).

**Actual Result**

The page/cart crashes (UI stops working / page breaks). No information is displayed about the maximum allowed quantity, and no validation message is shown.

**Expected Result**

The cart should validate the quantity (show the max limit or block/auto-limit invalid values) and must not crash.

[bug](../../Assets/Bug-Clips/bug-clip-02.mp4)
