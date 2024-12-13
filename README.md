# Balmes_OOP_FinalProj
# CHUBS Food Ordering Application

CHUBS is a simple console-based Java application for food ordering. The application allows users to sign up, log in, add items to their cart, view their cart, delete items from the cart, and claim discounts using coupons. The application is designed to demonstrate object-oriented programming concepts such as inheritance, encapsulation, and interfaces.

---

## Features

1. **User Authentication**
   - Allows users to sign up with a username and password.
   - Supports user login with authentication checks.

2. **Cart Operations**
   - Add food items to the cart.
   - View the cart with details of items, quantities, prices, and total cost.
   - Remove items from the cart by specifying the item number.

3. **Discounts**
   - Users can claim a 15% discount by entering a randomly generated verification code.

4. **Food Menu**
   - Offers a selection of food items with fixed prices.
   - Allows users to specify quantities when adding items to the cart.

5. **Shipping Fee**
   - A fixed shipping fee of 50 is applied to the total order.

6. **Clear Console Utility**
   - Ensures a clean display by clearing the console when transitioning between menus (where supported).

---

## Classes and Interfaces

### **`OrderOperations` (Interface)**
Defines the contract for cart-related operations:
- `addToCart(Item newItem)`
- `displayCart()`
- `deleteCartItem(int itemNumber)`

### **`Item` (Class)**
Represents a single food item in the cart:
- Attributes: `itemName`, `itemPrice`, `qty`, and `next` (for linked-list implementation).
- Methods: Getters for all attributes and a setter for the `next` pointer.

### **`User` (Class)**
Represents a basic user with authentication:
- Attributes: `username`, `password`.
- Methods: `authenticate(String username, String password)` for verifying credentials.

### **`CustomerUser` (Class)**
Extends `User` and implements `OrderOperations`:
- Additional Attributes: `fullName`, `contactNumber`, `fullAddress`, `cart`, `discount`, `couponClaimed`, `prepareTotal`, and `shippingFee`.
- Methods:
  - Cart Operations: `addToCart`, `displayCart`, and `deleteCartItem`.
  - Discount Operation: `claimCoupon()`.

### **`ChubsApp` (Class)**
The main driver class:
- Handles user registration and login.
- Contains the main menu and food menu logic.
- Utility method: `clearConsole()`.

---

## Food Menu
The application provides the following food options:

| Option | Food Item            | Price  |
|--------|----------------------|--------|
| 1      | Lumpiang Shanghai    | P120   |
| 2      | Chicken Wings        | P150   |
| 3      | Calamares            | P180   |
| 4      | Nachos               | P160   |

---

## How to Use

1. **Sign Up**
   - Enter your full name, contact number, address, username, and password to register.

2. **Log In**
   - Use your username and password to log into the application.

3. **Main Menu**
   - Navigate through the following options:
     - `(1)` View and select food items to add to your cart.
     - `(2)` View your cart (even if it is empty).
     - `(3)` Claim a coupon to get a 15% discount.
     - `(4)` Exit the application.

4. **Food Menu**
   - Select a food item and specify the quantity to add to your cart.

5. **View Cart**
   - Displays the items in your cart, including quantities, total prices, shipping fees, and applied discounts.

6. **Claim a Coupon**
   - Generate a random verification code and enter it correctly to claim a 15% discount.

7. **Delete Items from Cart**
   - Remove items from the cart by specifying their item number.

---

## How to Run the Program

1. Compile the program using `javac`:
   ```bash
   javac ChubsApp.java
   ```

2. Run the program using `java`:
   ```bash
   java ChubsApp
   ```

---

## Example Walkthrough

1. **Sign Up**
   - Input your details (e.g., "John Doe", "09123456789", "123 Main St", "john", "password").

2. **Log In**
   - Enter the username "john" and password "password".

3. **Add Items to Cart**
   - Select Lumpiang Shanghai, specify quantity as 2. Repeat for other items.

4. **View Cart**
   - See the details of items added, total cost, and shipping fee.

5. **Claim Coupon**
   - Enter the generated verification code correctly to apply the discount.

6. **Delete Item**
   - Remove an item from the cart by specifying its number.

---

## Future Enhancements

1. Add a graphical user interface (GUI) for a better user experience.
   - This feature aligns with **SDG 9: Industry, Innovation, and Infrastructure**, as it improves the technological experience for users.

2. Store user data and orders in a database.
   - Contributes to **SDG 8: Decent Work and Economic Growth** by providing a scalable solution for managing business data, fostering growth opportunities.

3. Add payment gateway integration.
   - Supports **SDG 1: No Poverty** and **SDG 8: Decent Work and Economic Growth** by enabling smoother transactions and encouraging entrepreneurship.

4. Enhance error handling and input validation.
   - Aligns with **SDG 4: Quality Education** by promoting best practices in software design and ensuring accessible learning resources.

5. Provide more flexible coupon and discount options.
   - Encourages **SDG 12: Responsible Consumption and Production** by incentivizing users to make better purchase decisions.

## Implemented Sustainable Development Goals (SDGs)

The application also incorporates several SDGs directly in its current implementation:

1. **SDG 8: Decent Work and Economic Growth**
   - The app supports entrepreneurship by providing a platform for users to simulate an e-commerce system.

2. **SDG 12: Responsible Consumption and Production**
   - The coupon feature incentivizes users to plan their purchases effectively and reduce waste.

3. **SDG 9: Industry, Innovation, and Infrastructure**
   - By utilizing programming best practices and enabling users to manage orders, the app contributes to the technological landscape and innovation in small-scale solutions.


---

## License
This project is open-source and available for personal and educational use.

---

### Author
Developed by.

