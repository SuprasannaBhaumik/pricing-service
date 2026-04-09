# Pricing Service (REST API)

This service provides pricing data mapped to movies.

---

## 📦 Setup

```bash
npm init -y
npm install json-server
```

---

## 📁 File Structure

```
pricing-service/
├── package.json
└── prices-list.json
```

---

## 📄 prices-list.json (Sample)

```json
{
  "prices": [
    {
      "id": 1,
      "referenceEntityId": 1,
      "entityPrice": {
        "amount": 10,
        "currency": "USD"
      },
      "serviceCharges": {
        "stream": { "amount": 2, "currency": "USD" },
        "support": { "amount": 1, "currency": "USD" }
      }
    }
  ]
}
```

---

## ▶️ Run Service

```bash
npx json-server --watch prices-list.json --port 4040
```

---

## 🌐 Endpoint

```
GET http://localhost:4040/prices
GET http://localhost:4040/prices?referenceEntityId=1
```

---

## ✅ Purpose

This service provides pricing details used by the **Pricing subgraph**.
