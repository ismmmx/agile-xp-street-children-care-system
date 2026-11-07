# Requirements Summary

This is a summary. The complete specification, user story table and requirements traceability matrix are in the [project report](../project-report/Street-Children-Care-System-Project-Report.pdf).

## Actors

Administrator · Staff · Orphanage Coordinator · Foundation Coordinator · Vaccination Staff  
External actors in the use case model: SMS Gateway (mobile OTP) and Email Service (confirmation email).

## Scopes

| # | Scope | Main actors |
|---|---|---|
| 1 | User authentication and access management | All roles |
| 2 | Account enrollment and provisioning | Administrator |
| 3 | Self-profile and credential management | All roles |
| 4 | Street child registration | Staff |
| 5 | Child case management and tracking | Staff, Administrator |
| 6 | Orphanage partner management | Administrator |
| 7 | Orphanage care coordination | Orphanage Coordinator |
| 8 | Foundation partner management | Administrator |
| 9 | Foundation support coordination | Foundation Coordinator |
| 10 | Health and immunization record | Vaccination Staff |
| 11 | Health drive scheduling and monitoring | Vaccination Staff |

## Functional requirements (structure)

The traceability matrix groups requirements by role: **1.0** System Administrator (enrollment, login, dashboard, user management, organization management, child placement, reports), **2.0** Staff, **3.0** Orphanage Coordinator, **4.0** Foundation Coordinator, **5.0** Vaccination Staff. Each role has login, a dashboard with side menu, profile, password change and role-specific management functions.

## Non-functional requirements

| Category | Requirement |
|---|---|
| Security and access control | Only authenticated users access data according to role; password change requires old password and double entry of the new one; password recovery uses mobile OTP and email confirmation. |
| Data integrity and reliability | Centralized SQL Server back end to prevent duplicate and lost records; confirmation window before deleting records. |
| Usability | C# Windows Forms desktop interface; tables show status updates instantly; success notifications after major data entry. |
| Performance and efficiency | Fast child-record search; dashboards load after login and show only role-relevant data. |

## Task log

[`implemented-features.md`](implemented-features.md) lists each user-story task (T-1 to T-53) as tracked on the Trello board.
