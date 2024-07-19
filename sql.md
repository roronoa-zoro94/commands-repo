1. Show first name and last name of patients who does not have allergies. (null)
SELECT
  first_name,
  last_name
FROM patients
WHERE allergies IS NULL;
---------------------------------------------------------------------------------

2. Show first name of patients that start with the letter 'C'
SELECT
  first_name
FROM
  patients
WHERE
  first_name LIKE 'C%'

SELECT first_name
FROM patients
WHERE substring(first_name, 1, 1) = 'C'
----------------------------------------------------------------------------------------------

3. Show first name and last name of patients that weight within the range of 100 to 120 (inclusive)
SELECT
  first_name,
  last_name
FROM patients
WHERE weight BETWEEN 100 AND 120;

-------------------------------------------------------------------------------------------
4. Show first name and last name of patients that weight within the range of 100 to 120 (inclusive)
SELECT
  first_name,
  last_name
FROM patients
WHERE weight BETWEEN 100 AND 120;

SELECT
  first_name,
  last_name
FROM patients
WHERE weight >= 100 AND weight <= 120;
------------------------------------------------------------------------------------------

5. Update the patients table for the allergies column. If the patient's allergies is null then replace it with 'NKA'
UPDATE patients
SET allergies = 'NKA'
WHERE allergies IS NULL;
-------------------------------------------------------------------------------------------

6. Show first name and last name concatinated into one column to show their full name.
SELECT
  CONCAT(first_name, ' ', last_name) AS full_name
FROM patients;

SELECT first_name || ' ' || last_name
FROM patients;
------------------------------------------------------------------------------------------------

7. Show first name, last name, and the full province name of each patient.
Example: 'Ontario' instead of 'ON'
SELECT
  first_name,
  last_name,
  province_name
FROM patients
  JOIN province_names ON province_names.province_id = patients.province_id;
-----------------------------------------------------------------------------------------------

8. 

