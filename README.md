# Metro Ticket Generating System

A ServiceNow application for booking metro tickets online. The passenger fills a short form on the Service Portal, the fare is calculated automatically, a QR code ticket is shown, and every booking is saved for station staff to verify.

**Platform:** ServiceNow – Personal Developer Instance (Global scope)

## Features

- **Book A Metro Ticket** catalog item on the Service Portal with 8 fields
- Automatic fare calculation (single and return journey, 1–4 passengers)
- "Enter payment mode" field appears only when Mode of Payment = Others (UI policy)
- QR code ticket shown in a popup (custom widget `metro_qr_widget` + QR Code API)
- Flow Designer flow saves each booking to the **Metro Ticket Booking** table (MTB numbers) and creates a verification task for the Station Managers group
- Default ACLs keep the tables safe from normal users

## Fares (from Ameerpet)

| Route | Single (per passenger) | Return (per passenger) |
|---|---|---|
| Ameerpet – Madhapur | ₹30 | ₹60 |
| Ameerpet – LB Nagar | ₹50 | ₹100 |
| Ameerpet – Kukatpally | ₹30 | ₹60 |
| Ameerpet – Jubilee Hills | ₹20 | ₹40 |

## Repository contents

All project documents are provided as PDF files in the main folder, along with the two ServiceNow XML exports. Screenshots are kept in a separate folder.

| File / Folder | What is inside |
|---|---|
| `Define_Problem_Statements.pdf` | Customer problem statements |
| `Empathy_Map_Canvas.pdf` | Empathy map of a daily metro commuter |
| `Brainstorming_Idea_Generation_Prioritization.pdf` | Brainstorming, idea grouping and prioritisation |
| `Customer_Journey_Map.pdf` | Customer journey map |
| `Solution_Requirements.pdf` | Functional and non-functional requirements |
| `Data_Flow_Diagrams_and_User_Stories.pdf` | Data flow diagram and user stories |
| `Technology_Stack.pdf` | Technical architecture and technology stack |
| `Problem_Solution_Fit.pdf` | Problem–solution fit canvas |
| `Proposed_Solution.pdf` | Proposed solution |
| `Solution_Architecture.pdf` | Solution architecture |
| `Project_Planning.pdf` | Sprint planning, burndown chart |
| `Planning_Logic.pdf` | Planning logic and velocity |
| `Functional_and_Performance_Testing.pdf` | Functional and performance test cases |
| `Artificial_Intelligence_Performance_Test.pdf` | AI performance test template |
| `Machine_Learning_Performance_Test.pdf` | ML performance test template |
| `Power_BI_Performance_Test.pdf` | Power BI performance test template |
| `Tableau_Performance_Test.pdf` | Tableau performance test template |
| `Salesforce_Performance_Test.pdf` | Salesforce performance test template |
| `User_Acceptance_Testing.pdf` | User acceptance test cases and bug tracking |
| `UAT_Report.pdf` | UAT execution and report |
| `FSD_Project_Documentation.pdf` | Project documentation |
| `Final_Project_Report.pdf` | Final project report |
| `Metro_Ticket_Generating_System.xml` | Exported update set of the application – can be imported into any ServiceNow instance |
| `Metro_Station_Details_Data.xml` | The 5 station records |
| `Screenshots/` | Screenshots of the build and the working output |

## How to import the application

1. Log in to a ServiceNow instance as admin.
2. Go to **System Update Sets → Retrieved Update Sets**.
3. Click **Import Update Set from XML** and choose `Metro_Ticket_Generating_System.xml`.
4. Open the retrieved update set → **Preview Update Set** → **Commit Update Set**.
5. Import the station data: open `u_metro_station_details.list`, right-click a column heading → **Import XML**, and choose `Metro_Station_Details_Data.xml`.
6. Open `/sp`, search **Book A Metro Ticket** and place a test booking.
