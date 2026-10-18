# Travel Naja

**Travel booking platform — requirements and system design**

Travel Naja brings flight booking, hotel reservations, car rentals, and local tour-guide discovery into one proposed travel-planning experience. The design combines third-party booking providers with a locally managed guide service.

This repository documents the platform's scope, requirements, actors, use cases, and data flows. It contains planning and analysis artifacts rather than a complete, runnable booking application.

## Platform scope

| Service | Planned capability |
| --- | --- |
| Flights | Search availability and reserve flights through external booking agencies |
| Hotels | Discover rooms and make reservations through hotel-provider APIs |
| Car rentals | Compare vehicles, rental periods, and pickup/drop-off locations |
| Local guides | Discover approved guides and book tours within capacity limits |

The local-guide service is managed within the proposed platform: guides submit their qualifications and tour offerings, and operations staff review applications before approval.

## Planned user experience

- Register and sign in to a member account.
- Search travel options by destination and schedule.
- Review availability and select a booking.
- Complete payment through an external credit-card payment system.
- View booking history and manage reservations.
- Maintain profile details and travel preferences.
- Receive travel recommendations and browse promotions.
- Use a multilingual interface across desktop and mobile experiences.

These capabilities are specified requirements, not implemented or verified features.

## System design

The platform is designed around three main operational groups:

- **Travelers:** search, book, pay, and manage their travel information.
- **Local guides:** apply to join the platform and maintain tour offerings and availability.
- **Operations staff:** review guide applications, manage promotions, and access reports.

External booking agencies provide flight, hotel, and car-rental information. A bank or payment provider handles payment processing. The documentation also identifies the frontend team as an actor involved in maintaining the user experience.

### Booking flow

1. A signed-in traveler searches for a service.
2. Travel Naja retrieves relevant options from an external provider or its local-guide catalog.
3. The traveler selects an option and proceeds to payment.
4. The proposed system records the reservation and provides confirmation.
5. Booking details become available in the traveler's history.

The report includes detailed narratives for car rental, travel-information search, and local-guide application submission.

## Documentation

| Artifact | Description |
| --- | --- |
| [Initial project document](Phase-0/ITCS371_Phase%200_Group%208.pdf) | Initial project planning material |
| [Requirements and design report](Phase-1/ProjectReport.pdf) | Platform scope, 20 functional requirements, 11 non-functional requirements, actors, and use-case narratives |
| [Use-case diagram](Phase-1/User%20Case%20Diagram/Use%20Case.pdf) | Interactions between the proposed system and its actors |
| [Context diagram — DFD Level 0](Phase-1/Data%20Flow%20Diagram/DFD%20Level_0.pdf) | System boundary and external data exchanges |
| [Data-flow diagram — DFD Level 1](Phase-1/Data%20Flow%20Diagram/DFD%20Level_1.pdf) | More detailed process and data-flow decomposition |

### Diagram previews

<details>
<summary>Use-case diagram</summary>

![Travel Naja use-case diagram](Phase-1/User%20Case%20Diagram/Use%20Case.png)

</details>

<details>
<summary>Context diagram — DFD Level 0</summary>

![Travel Naja context diagram](Phase-1/Data%20Flow%20Diagram/DFD%20Level_0.png)

</details>

<details>
<summary>Data-flow diagram — DFD Level 1</summary>

![Travel Naja Level 1 data-flow diagram](Phase-1/Data%20Flow%20Diagram/DFD%20Level_1.png)

</details>

## Quality objectives

The requirements describe responsive desktop and mobile experiences, accessibility, secure communication, data consistency, availability, monitoring, and scalability.

Performance and concurrency statements in the report are design targets. This repository does not provide benchmark results or a deployed system demonstrating those targets.

## Repository structure

```text
Phase-0/
└── Initial project document
Phase-1/
├── ProjectReport.pdf
├── Data Flow Diagram/
│   ├── DFD Level_0.pdf / .png
│   └── DFD Level_1.pdf / .png
├── User Case Diagram/
│   └── Use Case.pdf / .png
└── README.md
lab-exercise-1/
└── Small standalone Java examples
README.md
```

The Java examples are separate from the Travel Naja platform design and do not implement the booking flows.

## Getting started

Start with the [requirements report](Phase-1/ProjectReport.pdf), then review the use-case diagram and data-flow diagrams. All primary documents can be viewed directly on GitHub or downloaded for closer inspection.

There is no application installation or deployment procedure in the current repository. A production implementation would still require application code, provider integrations, payment configuration, database design, and verification against the documented requirements.

## Contributors

Lingrui Dong · Zishu Wang · Chusong Xu · Shaojun Wen · Jiahui Wu

## License

No license file is present in the inspected repository. Contact the contributors before reusing or redistributing the material.
