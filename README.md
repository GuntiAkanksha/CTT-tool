## Overview

This document outlines the key responsibilities and checks to be performed before starting with CTT tool.

---ctt.env

Update the paths, paysys & currency in ctt.env file 

Update paysys & currency details in sh file

---

## 📄 Nocks Sheet
🧩 What is a Nock?

It Mocks HTTP requests (external APIs). Intercepts HTTP calls and returns predefined responses without actually hitting the real API.

Ensure that all required nocks mentioned in the design document are getting called.


---

## 📄  API Chaining Sheet

### 🔸 Mocks

#### Checks:
1. Ensure **all mocks** mentioned in the design document are present in the mocks folder(test/cttTestSuite/payments_workspace/py/mocks)
   - (outbound.json/inbound.json..)
2. Confirm that each mock contains the **exact required data**.  
   - If not, create a **new mock** by copying an existing one and modify the necessary fields.
   - Pass the new mock name in the design document.
3. Review all mocks mentioned in the design document and **remove any unnecessary mocks**.
4. If you need to **dynamically pass values** to a mock:
   - Use the **Mock Input** column to pass values using the format:  
     ```
     #COMBO.X
     ```
   - pass the `X` parameter as column the **Generated Combinations** sheet & provide the param path in TestConfig file.

---

### 🔸 Patterns

#### Checks:
1. Ensure all **template files** are present in the `templates` folder.
2. Validate that the **template content** matches the expected structure and data.
3. If no existing template matches the required format, **create a new template file** with the appropriate structure.
4. When you want to pass input dynamically to template use 'Input' column.

---

## 📄  Generated Combinations Sheet

#### Checks:
1. Verify that **all assertions** in Genrated Combinations are correctly mapped with template names present in API Chaining sheet.

---

## 📄  Test Config

#### Checks:
1. Ensure that all paths for parameters used in **Generated Combinations** are properly defined here.
   - Each value passed in the generated combinations should have a corresponding path entry in this configuration.

---

## 🧱 Note
- Maintain consistent naming conventions across mocks, templates, and config sheets.
- An extra unncessary space can cause some isssues.
- When you are working on CTs outside node_modules -  Use replace.js(test/componentTest/replace.js) to replace CMNCT to respective PAYSYS & replace HKD to respective CRNCY.

---

## 🚧 Work in Progress
This README is a **living document** , feel free to update.
