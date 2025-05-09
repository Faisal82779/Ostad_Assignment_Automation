# 🚀 SauceDemo Automation with WebDriverIO

Automated testing project for [SauceDemo](https://www.saucedemo.com/) using WebDriverIO, designed to validate three end-to-end user scenarios.

---

## 🛠️ Technologies Used

- ✅ WebDriverIO  
- ✅ Mocha (Test Framework)  
- ✅ Chai (Assertion Library)  
- ✅ Allure Reporter (For Reporting)

---

## 📁 Test Scenarios

### 🧪 Q1: Locked Out User Validation...👍
- Login with `locked_out_user`
- Validate error message display

---

### 🛒 Q2: Standard User Full Purchase Flow... 👍
- Login with `standard_user`
- Reset app state
- Add 3 products to cart
- Proceed to checkout
- Validate product names and total
- Complete the order
- Confirm success message
- Reset and log out

---

### ⚙️ Q3: Performance Glitch User + Sorting Test...👍
- Login with `performance_glitch_user`
- Reset app state
- Sort products (Z → A)
- Add first item to cart
- Validate product name and total
- Complete purchase
- Reset and log out

---

## 🚀 Getting Started

### 📌 Step 1: Installation

1. Clone the repository:
   ```bash
   git clone <repository_url>
   cd <repository_name>

 *(Replace `<repository_url>` with the actual URL of your GitHub repository and `<repository_name>` with the name of the cloned directory.)*


### 📌 Step 2: Run Individual Tests

Edit the `wdio.conf.js` file and uncomment the scenario you want to run under the `specs:` section:

    specs: [
    
        // Q1,
    
        // Q2,
    
        // Q3,
    
    ],

✅ Use Ctrl + / to uncomment one test file.

Then run the test:

    npm run wdio

### 📌 Step 3: Run All Tests Together

To run all three tests sequentially:

    npm run together

### 📌 Step 4: Generate Allure Report

After test execution, generate the Allure report:

    npm run getReport



## 🛠️ Command Summary

| 🔢 Step | 🧪 Command             | ⚙️ What It Does                                                                 |
|--------:|------------------------|----------------------------------------------------------------------------------|
| 1️⃣     | `npm run wdio`         | Runs the **selected individual test file** (after uncommenting in `wdio.conf.js`). |
| 2️⃣     | `npm run together`     | Executes **all scenarios** (`Q1`, `Q2`, and `Q3`) **in sequence**.               |
| 3️⃣     | `npm run getReport`    | Generates a **detailed Allure test report** after execution.                     |



## 📂 Folder Structure

```
ostad_assessment/
├── .gitignore
├── package-lock.json
├── package.json
├── wdio.conf.js
├── allure-report/
├── allure-results/
├── node_modules/
├── specs/
│   ├── Q1.spec.js
│   ├── Q2.spec.js
│   └── Q3.spec.js
└── test/
    ├── Q1/
    │   ├── loginAction.js
    │   └── loginObject.js
    ├── Q2/
    │   ├── cart/
    │   │   ├── addToCartAction.js
    │   │   └── addToCartObject.js
    │   ├── checkout/
    │   │   ├── checkoutAction.js
    │   │   └── checkoutObject.js
    │   ├── finish_Purchase_and_message/
    │   │   ├── finishAction.js
    │   │   └── finishObject.js
    │   ├── login/
    │   │   ├── loginAction2.js
    │   │   └── loginObject2.js
    │   ├── openManue/
    │   │   ├── openManuAction.js
    │   │   └── openManuObject.js
    │   ├── poroduct_Name_and_Price/
    │   │   ├── namePriceAction.js
    │   │   └── namePriceObject.js
    │   ├── reset_app_and_logout/
    │   │   ├── resetLogutAction.js
    │   │   └── resetLogutObject.js
    │   └── viewCart/
    │       ├── viewCartAction.js
    │       └── viewCartObject.js
    └── Q3/
        ├── cart/
        │   ├── cartAction.js
        │   └── cartObject.js
        ├── CheckOut(fromQ2)/
        │   ├── checkoutAction.js
        ├── Filter/
        │   ├── filterAction.js
        │   └── filterObject.js
        ├── Login/
        │   ├── loginGlitchAction.js
        │   └── loginGlitchObject.js
        ├── Name_Price/
        │   ├── namePriceAction.js
        │   └── namePriceObject.js
        ├── reset_App(fromQ2)/
        │   ├── resetAppAction.js
        ├── ResetApp&Logout(fromQ2)/
        │   ├── resetLogoutAction.js
        ├── SuccessMessage(from Q2)/
        │   ├── finishMessageAction.js
        └── view_Cart/
            ├── viewCartAction.js
            └── viewCartObject.js
```
