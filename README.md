## Overview
This document outlines the key responsibilities and checks to be performed before starting with CTT tool.

---ctt.env
Update the paths, paysys & currency in ctt.env file 
Update paysys & currency details in sh file

---

## 📄 Nocks Sheet
🧩 What is a Nock
It Mocks HTTP requests (external APIs). Intercepts HTTP calls and returns predefined responses without actually hitting the real API.

Ensure that all required nocks mentioned in the design document are getting called.

### Checklist:
- ✅ Verify that **all required nocks** are mentioned in the nocks sheet of design document.

---

## 🔗 API Chaining Sheet

### 🔸 Mocks

#### Checks:
1. Ensure **all mocks** mentioned in the design document are present in the respective files below:
   - `outbound.json`
   - `inbound.json`
   - `suspense.json`
2. Confirm that each mock contains the **exact required data**.  
   - If not, create a **new mock** by copying an existing one and modify the necessary fields.
   - Pass the new mock name in the design document.
3. Review all mocks mentioned in the design document and **remove any unnecessary mocks**.
4. If you need to **dynamically pass values** to a mock:
   - Use the **Mock Input** column to pass values using the format:  
     ```
     #COMBO.X
     ```
   - Define the corresponding `X` value in the **Generated Combinations** sheet.

---

### 🔸 Patterns

#### Checks:
1. Ensure all required **template files** are present in the `templates` folder.
2. Validate that the **template content** matches the expected structure and data.
3. If no existing template matches the required format, **create a new template file** with the appropriate structure.
4. When you want to pass input to template use 'Input' column.

---

### 🔸 Generated Combinations Sheet

#### Checks:
1. Verify that **all assertions** are correctly defined and aligned with expected outcomes.

---

### 🔸 Test Config

#### Checks:
1. Ensure that all paths for parameters used in **Generated Combinations** are properly defined here.
   - Each value passed in the generated combinations should have a corresponding path entry in this configuration.

---

## 🧱 Notes
- Maintain consistent naming conventions across mocks, templates, and config sheets.
- An extra unncessary space can cause some isssues.

---

## 🚧 Work in Progress
This README is a **living document** , feel free to update.
