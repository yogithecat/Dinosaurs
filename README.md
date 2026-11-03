# Dinosaurs 🦖

Final project repository for **Team Dinosaurs**: a dbt analytics project built on retail data.

## Team

| Name | GitHub | Role |
|------|--------|------|
| TBD | @yogithecat | Repo owner |
| Riaan Joshi | @riaanjoshi | Setup lead |
| Khushi Patel | TBD | Team member |
| Rian | TBD | Team member |

## Use case

We will model retail transaction data (orders, products, customers, stores) into clean, tested analytics tables that answer business questions such as:

- Which products, categories, and stores drive the most revenue and margin?
- How do sales trend over time (daily / weekly / seasonal)?
- Who are our repeat customers, and what is their lifetime value?

Outputs: staging models for each source, fact/dimension marts (e.g. `fct_orders`, `dim_customers`, `dim_products`), dbt tests, and documentation.

## Project structure

```
Dinosaurs/
├── README.md
├── dbt_project.yml        # dbt project config
├── models/
│   ├── staging/           # 1:1 cleaned source models
│   ├── intermediate/      # business-logic joins
│   └── marts/             # final fact/dimension models
├── seeds/
├── tests/
├── macros/
└── analyses/
```

## dbt setup plan

1. Choose the warehouse/adapter and install dbt (`pip install dbt-core dbt-<adapter>`).
2. Each teammate creates their own `~/.dbt/profiles.yml` locally using the profile name `dinosaurs`. **Never commit credentials.**
3. Run `dbt debug` to verify the connection.
4. Build staging models from the raw retail sources, then add tests.

## Workflow

- Work happens on feature branches; changes reach `main` through pull requests with at least one approving review.
- Work is tracked on the GitHub Projects board (Backlog → Ready → In progress → In review → Done).
- Never commit secrets, `profiles.yml`, `.env` files, or the `target/`, `dbt_packages/`, and `logs/` folders.
