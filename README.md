# Senkanthal's Thirukkural API

A free, public REST API to explore the ancient Tamil classic **Thirukkural** – including its Paals (books), Athikaarams (chapters), and individual Kurals (couplets).

- **Base URL:** [thirukkural.senkanthal.org](https://thirukkural.senkanthal.org)
- **Mirror:** [kural.senkanthal.org](https://kural.senkanthal.org)
- **Format:** All responses are in JSON.
- **Version:** 1.0.0

---

## Features

- List and fetch details for all **Paals** (Books)
- List and fetch details for all **Athikaarams** (Chapters)
- List and fetch details for all **Kurals** (Couplets)
- Get all Kurals in a Paal or Athikaaram
- Fetch a random Kural, or a random Kural from a specific Paal or Athikaaram

---

## Note on Kural Formatting

In the API responses, the Kural text uses the dollar sign (`$`) to indicate a line break between the first and second lines of the couplet.

---

## Endpoints

### API Root

```
GET /
```
API documentation is available via Swagger UI

---

### Paal (Book) Endpoints

- **List all Paals:**  
  `GET /paal`

- **Get Paal by ID:**  
  `GET /paal/{id}`  
  - `id`: 1–3

- **All Kurals in a Paal:**  
  `GET /paal/{id}/all`

- **Random Kural from a Paal:**  
  `GET /paal/{id}/random`

---

### Athikaaram (Chapter) Endpoints

- **List all Athikaarams:**  
  `GET /athikaaram`

- **Get Athikaaram by ID:**  
  `GET /athikaaram/{id}`  
  - `id`: 1–133

- **All Kurals in an Athikaaram:**  
  `GET /athikaaram/{id}/all`

- **Random Kural from an Athikaaram:**  
  `GET /athikaaram/{id}/random`

---

### Kural (Couplet) Endpoints

- **List all Kurals:**  
  `GET /kural`

- **Get Kural by ID:**  
  `GET /kural/{id}`  
  - `id`: 1–1330

- **Get a random Kural:**  
  `GET /random`

---

## Example Usage

**Get a specific Kural:**
```http
GET https://thirukkural.senkanthal.org/kural/1
```

**Get all Kurals in the first Paal:**
```http
GET https://thirukkural.senkanthal.org/paal/1/all
```

**Get a random Kural:**
```http
GET https://thirukkural.senkanthal.org/random
```

---

## License

[MIT](LICENSE) License.  
All data is free to use. Attribution appreciated but not required.

---

## About Thirukkural

The [**Thirukkural**](https://www.projectmadurai.org/pm_etexts/utf8/pmuni0001.html) is a classic Tamil text consisting of 1330 couplets, offering timeless wisdom on ethics, wealth, and love.

---

## Contact

For feedback or questions, email: [contact@senkanthal.org](mailto:contact@senkanthal.org)

---

Let US know if you want code samples or more details!

© 2025 Senkanthal.org. All rights reserved.
