# 🚀 GraphQL API – Postman Collections

A set of **GraphQL API** requests built with Postman, covering two public APIs.

---

## 📁 Collections

### 🧬 Rick & Morty Character API
> `https://rickandmortyapi.com/graphql`

| Request | Description |
|---|---|
| Fetch Page 1 Characters | Fetches the first page of characters with pagination info |
| Fetch Single Character | Fetches a single character by ID with origin and location details |
| Fetch Characters with Status | Filters and returns characters based on their status (e.g. Dead, Alive) |
| Fetch Multiple Characters by IDs | Retrieves multiple characters in one query using an array of IDs |
| Get Characters by Status and Species | Filters characters by both status and species combined |

---

### 🌍 Countries GraphQL API
> `https://countries.trevorblades.com/`

| Request | Description |
|---|---|
| Fetch All Countries | Returns name, code, capital, and currency for every country |
| Fetch Specific Country | Gets languages and continent info for a country by its code |
| Fetch All Continents | Lists all continents with their name and code |
| Fetch Countries in Asia | Filters and returns countries belonging to the Asian continent |
| Fetch All Languages | Returns all languages with code, name, native name, and RTL flag |
| Get Countries by Codes | Fetches multiple specific countries in one request using country codes |

---
## Project Structure

graphql-api-practice/
│
├─ collections/
│ ├─ GraphqlCharacterAPI_postman_collection.json
│ └─ GraphQLCountry_postman_collection.json
│
├─ environments/
│ └─ development.postman_environment.json
│
|__ newman/
|  └─ reports.html
|
└─ README.md

## 🛠️ Setup and Running via Postman GUI

1. Install [Postman](https://www.postman.com/downloads/)  
2. Import collections from `collections/` folder  
3. Import environment from `environments/development.postman_environment.json`  
4. Select a collection → select a request → hit **Send**

---

## 🚀 Running via Newman (CLI)

### Step 1 — Install Node.js
Download and install Node.js from the official site:
👉 https://nodejs.org/en/download

Verify installation:
```bash
node -v
npm -v
```

### Step 2 — Install Newman
```bash
npm install -g newman
```

Verify installation:
```bash
newman --version
```

### Step 3 - Install HTML Reporter

```bash
npm install -g newman-reporter-htmlextra
```

### Run the collection

```bash

newman run collections\GraphqlCharacterAPI.postman_collection.json -e environments\development.postman_environment.json -r htmlextra
newman run collections\GraphQlCountry.postman_collection.json -e environments\development.postman_environment.json -r htmlextra
---


## 🔗 API References

- [Rick and Morty API](https://rickandmortyapi.com/documentation)
- [Countries GraphQL API](https://github.com/trevorblades/countries)
