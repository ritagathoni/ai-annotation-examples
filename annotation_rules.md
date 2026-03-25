# Annotation Rules

1. Normalize all `name` and `company` values as strings.

2. Map contact information into a nested `contact` object.
   - If email is missing, set `contact.email` to `null`.

3. Convert currency values to numeric format.
   - Remove currency symbols such as `$`
   - Remove commas from numeric values
   - Store final values as numbers

4. Normalize percentage fields to numeric format.
   - Remove the `%` symbol where present
   - Store valid discount values as numbers
   - If a discount value cannot be parsed, set it to `null` and log an error

5. Normalize boolean-like values.
   - Convert values such as `Yes`, `No`, `TRUE`, and `FALSE` into standardized output values
   - Map urgent records to `meta.priority` as `urgent` or `normal`

6. Apply business rules during transformation.
   - If `discount_requested > 20`, set `approval_required = true`
   - Otherwise set `approval_required = false`

7. Preserve nested JSON structure for related fields.
   - Store email under `contact`
   - Store value, discount, and approval fields under `deal`
   - Store priority under `meta`

8. Handle missing and invalid values consistently.
   - Missing values should be set to `null`
   - Invalid but present values should be preserved where possible and tagged using the error taxonomy

9. Log validation issues using the defined taxonomy.
   - Use `errors` for critical issues that affect validity
   - Use `warnings` for non-critical normalization or formatting adjustments

10. Every record must include both `errors` and `warnings` arrays, even if they are empty.

11. Ensure all output records remain schema-compliant and ready for downstream validation.
