# Tarkov Loot Advisor

Tarkov Loot Advisor is a web application that helps Escape from Tarkov players compare item sale options. The planned MVP lets a player search for an item and see an explainable recommendation based on available Tarkov.dev market and trader data.

Recommendations are estimates, not guaranteed sale prices. They should show the prices and fee assumptions used, when the data was observed, and whether relevant data is missing or stale.

## MVP scope

The first milestone focuses on:

- Importing item and price data from the [Tarkov.dev API](https://tarkov.dev/).
- Storing item and timestamped price data in PostgreSQL, with Flyway-managed schema migrations.
- Searching items by name.
- Comparing available sale options and returning estimated proceeds with calculation inputs and data freshness.
- Providing a separate Angular user interface for search and recommendation details.

Screenshot recognition is planned to allow users to upload a screenshot of a container of loot (ex. Backpack, rig, etc.) and quickly determine where the optimal selling location for each item is. 

## Technology

- **Backend:** Java 25, Spring Boot, Spring Web MVC, Spring Data JPA, and Bean Validation.
- **Database:** PostgreSQL.
- **Migrations:** Flyway.
- **Frontend:** Angular (planned as a separate application under `frontend/`).
- **Build:** Maven Wrapper.
- **External data:** Tarkov.dev API.