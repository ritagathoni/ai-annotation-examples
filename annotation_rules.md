Annotation Rules

1. Normalize company and name fields into strings.

2. Convert currency values to numeric format.

3. Missing values should be set to null.

4. Discount greater than 20% triggers approval_required = true.

5. Log errors using the defined taxonomy.

6. Maintain nested JSON structure for contact and deal information.

7. All records must include errors and warnings arrays even if empty.
