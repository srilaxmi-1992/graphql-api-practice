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

## 🛠️ Setup

1. Install [Postman](https://www.postman.com/downloads/)
2. Import `GraphqlCharacterAPI_postman_collection.json` and `GraphQLCountry_postman_collection.json`
3. Select a request and hit **Send** — no authentication needed

---

## 🛠️ Setup & Run via Newman (CLI)

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

### Step 3 — Run Collections

**Run Rick & Morty Character API collection:**
```bash
newman run GraphqlCharacterAPI_postman_collection.json
```

**Run Countries GraphQL API collection:**
```bash
newman run GraphQLCountry_postman_collection.json
```

**Run with detailed HTML report (install reporter first):**
```bash
npm install -g newman-reporter-htmlextra

newman run GraphqlCharacterAPI_postman_collection.json -r htmlextra
newman run GraphQLCountry_postman_collection.json -r htmlextra
```

**Run with verbose output:**
```bash
newman run GraphqlCharacterAPI_postman_collection.json --verbose
```

---



## 🔗 API References

- [Rick and Morty API](https://rickandmortyapi.com/documentation)
- [Countries GraphQL API](https://github.com/trevorblades/countries)
