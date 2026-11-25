# After-Sales Service Platform

Repair ticket platform for an electronics manufacturer and its service centres.

Customers open repair tickets online, service centres follow each product from deposit to delivery, and managers measure workload, delays, recurring failures and satisfaction.

> **Structure only.** The source code is private. Source files here are intentionally empty so you can see how the project is organized. Commands describe the private codebase.
>
> Company names, logos and data were removed. All data in the screenshots is fictional.

![Dashboard](docs/screenshots/staff-dashboard.png)

## Features

- Ticket flow: waiting, deposited, in repair, repaired, ready, delivered
- Warranty status and repair history by product
- Delay highlighting in lists
- Automatic documents and messages
- Satisfaction surveys

## Applications

| Application | Role |
| --- | --- |
| [API server](server/README.md) | Express API |
| [Management application](frontend-management/README.md) | Staff interface for administrators and service centres |
| [Customer website](frontend-customer/README.md) | Public website |

## Architecture

```mermaid
flowchart LR
  C[Customer website] --> S[API server]
  G[Management application] --> S
  S --> DB[(MySQL)]
  S --> PDF[PDF slips]
  S --> MSG[SMS and email]
```

## Engineering highlights

- Paginated, searchable selectors for large reference lists
- Role-aware routing and server authorization
- Migration scripts that moved free text to relational references
- Graceful shutdown

## Screenshots

| Dashboard | Open tickets |
| --- | --- |
| ![Dashboard](docs/screenshots/staff-dashboard.png) | ![Open tickets](docs/screenshots/staff-tickets.png) |
| **Ticket details** | **New ticket** |
| ![Ticket details](docs/screenshots/staff-ticket-details.png) | ![New ticket](docs/screenshots/staff-open-ticket.png) |
| **Delivered products** | **Satisfaction** |
| ![Delivered products](docs/screenshots/staff-delivered.png) | ![Satisfaction](docs/screenshots/staff-satisfaction.png) |
| **Products** | **Service centres** |
| ![Products](docs/screenshots/staff-products.png) | ![Service centres](docs/screenshots/staff-service-centres.png) |
| **Customer website** | **Customer ticket** |
| ![Customer website](docs/screenshots/client-home.png) | ![Customer ticket](docs/screenshots/client-open-ticket.png) |

Screenshots show the real front ends connected to a mock API with fictional data, because the server needs MySQL. Company branding was replaced.

## Repository layout

```text
server/                                 Express API
frontend-management/                    Staff interface for administrators and service centres
frontend-customer/                      Public website
docs/screenshots/
```

Each application has its own README with responsibilities, dependencies, structure and commands.

## Usage

Published for portfolio and presentation purposes. No license is granted for reuse.
