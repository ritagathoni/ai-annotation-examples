# QA Validation Checklist

## 1. Required Field Validation
Ensure all mandatory fields are present:

- name  
- company  
- contact.email  
- deal.value  

Flag missing fields using:
- E_MISSING_EMAIL  

---

## 2. Data Type Validation
Validate correct data types:

- deal.value must be numeric  
- discount_requested must be numeric  
- boolean fields must be true/false  

Flag invalid values using:
- E_INVALID_BOOLEAN  

---

## 3. Business Rule Validation
Apply domain-specific rules:

- discount > 20% requires approval  
- missing email triggers E_MISSING_EMAIL  

---

## 4. Duplicate and Consistency Checks
- Detect duplicate entities or records  
- Ensure consistent field values across entries  

Flag issues using:
- E_DUPLICATE_ENTITY  

---

## 5. Warning Handling
Non-critical issues should be flagged as warnings:

- W_DEFAULT_VALUE_USED  

---

# Financial Document QA Checks

## 6. Line Item Validation
- Verify each `line_total = quantity × unit_price`  
- Flag mismatches as errors  

---

## 7. Subtotal Validation
- Verify `subtotal = sum(line_items.line_total)`  

---

## 8. Grand Total Validation
- Verify `grand_total = subtotal + tax`  

---

## 9. Required Financial Fields
Ensure presence of:

- vendor  
- invoice_number  
- invoice_date  
- currency  
- line_items  
- subtotal  
- grand_total  

---

## 10. Financial Data Type Validation
- quantity must be integer  
- prices and totals must be numeric  
- paid must be boolean  

---

## 11. Validation Outcomes
Each record should produce:

- errors → critical issues that fail validation  
- warnings → non-critical issues  

Example:
- Missing required field → error  
- Default value used → warning  
