QA Validation Checklist

1. Check required fields
- name
- company
- contact.email
- deal.value

2. Validate numeric fields
- deal.value must be a number
- discount_requested must be numeric

3. Business rules
- discount >20% requires approval
- missing email triggers error E_MISSING_EMAIL

4. Error taxonomy
E_MISSING_EMAIL
E_INVALID_BOOLEAN
E_DUPLICATE_ENTITY

5. Warnings
W_DEFAULT_VALUE_USED
