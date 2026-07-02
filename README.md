# Category_checker — Allegro REST API Integration

This repository serves as public documentation for **Category_checker**
(Allegro REST API application, Client ID: `053d21b152ac4b2e9f67fab5fd2facf7`),
a suite of internal tools used for sales operations automation.

All tools share a single registered Allegro application and are maintained
by the same operator. Requests are identified by the User-Agent header:


Category_checker/1.0.0 (+https://github.com/antekkalafior/Allegro_API_Overwiew)


---

## What this application does

### 1. Price & Margin Management Platform
Internal web application (FastAPI + React) that queries the Allegro REST API to:
- retrieve product category trees and commission rates for margin calculation
- monitor offer prices across multiple seller accounts
- compare pricing against reference sources (Empik, competitor data)

### 2. Shipping Rate Synchronization
Automated tooling that:
- fetches existing delivery price lists (cenniki dostaw) from Allegro API
- creates and updates shipping rate tables based on external data sources (CSV/XLSX)
- bulk-patches seller offers to assign the correct rate table per SKU group
- supports multiple seller accounts with per-account token management

### 3. Offer Data Export
Batch downloader that accepts a list of Allegro offer IDs, resolves which
seller account owns each offer, and exports full offer data (JSON + CSV)
for reporting and analysis.

### 4. Category & Commission Queries
Scripts for resolving Allegro product categories from EAN codes and product
names, used for catalogue enrichment and commission estimation.

---

## Operator contact

For questions regarding this application's activity, contact the repository owner
via GitHub: [antekkalafior](https://github.com/antekkalafior)

---

## Technical details

- Language: Python 3.11+
- Auth: OAuth 2.0 Device Flow with automatic token refresh
- Deployment: Docker, self-hosted Ubuntu server
- All API access is read/write scoped to the operator's own seller accounts
