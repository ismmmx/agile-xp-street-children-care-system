# Software Testing

Four manual test cases were designed and executed by four team members, one for each of four modules. Test data is illustrative sample data. The full test-case tables are in Section 5 of the [project report](../project-report/Street-Children-Care-System-Project-Report.pdf).

## Summary

| ID | Module | Designed and executed by | Priority | Result |
|---|---|---|---|---|
| TC_1 | Child Placement & Tracking | Ishmam Mubtasim | High | Pass |
| TC_2 | Foundation Profile | Sanjida Affrin Bristi | High | Pass |
| TC_3 | New Child Registration | Tanmay Roy Rony | High | Pass |
| TC_4 | Orphanage Profile Details | Afroza Akter Neha | High | **Fail** |

## TC_1 — Administrator assigns an unassigned child to a registered orphanage

- **Precondition:** Administrator is logged in and an unassigned child profile exists.
- **Dependencies:** Network connection and active database service.
- **Steps:** Open Child Placement from the side menu → click "+ New Placement" → select the child from the unassigned list → select the target organization → submit.
- **Expected:** Child status changes from "Pending" to "Placed" and appears under the assigned organization.
- **Actual:** As expected. **Status: Pass**

## TC_2 — Foundation Coordinator updates foundation profile with valid data

- **Precondition:** Logged in as Foundation Coordinator, on the Foundation Profile page.
- **Dependencies:** Active SQL Server database connection.
- **Steps:** Enter foundation name, contact email and person, phone number and website URL → click "Save Changes".
- **Expected:** Input is validated, the record is updated in SQL Server, and a success notification is shown.
- **Actual:** Profile details updated and notification displayed. **Status: Pass**

## TC_3 — Staff registers a new street child with complete valid details

- **Precondition:** Staff user is logged in, on the New Child Registration page.
- **Dependencies:** Active SQL Server database connection.
- **Steps:** Enter full name, estimated age, gender and found location, physical and health condition → click SUBMIT.
- **Expected:** Input is validated, the record is saved to SQL Server, and a success notification is shown.
- **Actual:** Record saved and success message displayed. **Status: Pass**

## TC_4 — Non-numeric data in the Max Capacity field

- **Precondition:** Orphanage Coordinator is on the Profile Details page.
- **Dependencies:** Input validation logic in the C# Windows Forms front end.
- **Steps:** Enter a valid orphanage name → enter non-numeric text in *Max Capacity* → click SUBMIT.
- **Expected:** Submission is blocked with the error "Max Capacity must be a positive integer."
- **Actual:** The form was submitted without validation and created a corrupted entry in the database. **Status: Fail**

### Known issue

TC_4 revealed missing numeric validation on the orphanage *Max Capacity* field. The corrective fix and re-test result are to be recorded here once completed.

| Item | Status |
|---|---|
| Fix implemented | Not recorded |
| Re-test result | Not recorded |
