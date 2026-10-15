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

| Folder | What is inside |
|---|---|
| `1_Ideation_Phase` | Problem statements, empathy map, brainstorming |
| `2_Requirement_Analysis` | Customer journey map, solution requirements, data flow diagrams and user stories, technology stack |
| `3_Project_Design` | Problem–solution fit, proposed solution, solution architecture |
| `4_Project_Planning` | Project planning (sprints) and planning logic |
| `5_Testing` | Functional and performance testing, performance test templates, user acceptance testing, UAT report |
| `6_Project_Documentation` | FSD project documentation and the final project report |
| `7_ServiceNow_Update_Set` | Exported XML of the application – can be imported into any ServiceNow instance |
| `8_Screenshots` | Screenshots of the build and the working output |

## How to import the application

1. Log in to a ServiceNow instance as admin.
2. Go to **System Update Sets → Retrieved Update Sets**.
3. Click **Import Update Set from XML** and choose the file in `7_ServiceNow_Update_Set`.
4. Open the retrieved update set → **Preview Update Set** → **Commit Update Set**.
5. Open `/sp`, search **Book A Metro Ticket** and place a test booking.
