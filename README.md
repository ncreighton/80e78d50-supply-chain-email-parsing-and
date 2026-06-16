# Supply Chain Email Parsing and Data Extraction API

> Tired of manually copy-pasting supplier emails into spreadsheets? Each typo costs you time and money—our API turns messy email data into structured JSON in milliseconds.

The Supply Chain Email Parsing and Data Extraction API eliminates the need for tedious data entry by automatically extracting purchase order numbers, quantities, dates, and line items from inbound supplier emails. It's purpose-built for logistics teams, letting you focus on moving goods—not wrangling spreadsheets.

## What's Included

- Extract purchase orders, invoices, and shipping notifications from plain text and HTML emails
- Supports custom field mapping to match your existing ERP or inventory system
- Handles multiple email formats (PDF attachments, tables, free text) without manual rules
- Batch processing with real-time callback URLs for instant downstream automation
- Simple RESTful API with clear documentation and one-click integration

## Who Is This For

- Logistics managers drowning in daily email floods from dozens of suppliers
- Procurement teams who need to reconcile purchase orders without manual data entry
- Supply chain analysts building dashboards or reports using structured data
- E-commerce operations that rely on timely inventory updates from vendor communications

## How It Works

Sign up for an API key, then send the raw email body or attachment via a single POST request. The API returns a structured JSON object with all parsed fields. You can integrate directly into your existing workflow using our cURL examples or SDK snippets—no complex setup required.

## Frequently Asked Questions

**What email formats does the API support?**
We handle plain text, HTML, and common attachment types (PDF, Excel, CSV). The parser detects table structures and key-value pairs automatically.

**Is my data secure when sent to the API?**
All transmissions are encrypted via HTTPS. We do not store your email data longer than necessary for processing, and you can request immediate deletion from our logs.

**Can I customize which fields are extracted?**
Yes. You provide a schema of fields (e.g., order number, ship date) and the API maps them to the email content using context-aware parsing.

**How fast is the processing?**
Typical response time is under 500ms for standard emails. Batch processing supports up to 100 emails per request with parallel parsing.

**Do I need coding experience to use this?**
Basic API knowledge (REST, JSON) is helpful. We provide tutorials for non-developers using Zapier, Make, and low-code platforms.

## What You Get

- Instant digital download
- Complete REST API with full documentation
- Free updates for life — pay once, own forever
- Setup guide and usage instructions

**Stop manually extracting data from supplier emails—get your API key for $32.49 and start automating today.**

## Features

- Full REST API

## Quick Start

```bash
# 1. Install dependencies
pip install -r requirements.txt

# 2. Configure environment
cp .env.example .env
# Edit .env with your settings

# 3. Run locally
uvicorn main:app --reload --port 8000

# 4. View interactive docs
open http://localhost:8000/docs
```

## Docker Deployment

```bash
# Build and run
docker compose up -d

# Check health
curl http://localhost:8000/health
```

## Authentication

Get a token first:
```bash
curl -X POST "http://localhost:8000/auth/token?username=admin&password=admin123"
```

Use the token in subsequent requests:
```bash
curl -H "Authorization: Bearer YOUR_TOKEN" http://localhost:8000/items
```

## API Endpoints

| Method | Path | Description |
|--------|------|-------------|
| GET | `/health` | System health |
| POST | `/auth/token` | Get JWT token |
| GET | `/items` | List all items |
| POST | `/items` | Create item |
| GET | `/items/{id}` | Get item |
| PATCH | `/items/{id}` | Update item |
| DELETE | `/items/{id}` | Delete item |
| GET | `/stats` | API statistics |

Full interactive docs: `http://localhost:8000/docs`

## Rate Limits

| Endpoint | Limit |
|----------|-------|
| `/auth/token` | 10/minute |
| `GET /items` | 60/minute |
| `POST /items` | 30/minute |
| `DELETE /items` | 20/minute |

## Running Tests

```bash
pip install pytest httpx
pytest tests/ -v
```

## Production Notes

- Change `SECRET_KEY` in `.env` before deploying
- Replace in-memory `_db` with a real database
- Add proper user management to `auth.py`
- Configure `ALLOWED_ORIGINS` for CORS
- Use Nginx/Traefik as reverse proxy

## License

MIT


---

## Free vs Pro

| Feature | Free | Pro |
|---------|:----:|:---:|
| 100 requests/day | Yes | Yes |
| Standard endpoints | Yes | Yes |
| JSON responses | Yes | Yes |
| Unlimited requests | - | Yes |
| Premium endpoints | - | Yes |
| Batch processing | - | Yes |
| Webhook notifications | - | Yes |
| SLA guarantee | - | Yes |
| Priority support | - | Yes |

### Upgrade to Pro

Get the full version with all premium features, priority support, and lifetime updates.

**[Get Pro Version](https://buy.stripe.com/aFa6oH7r18Isf440VecZg3i)**

- [Buy Now (Stripe)](https://buy.stripe.com/aFa6oH7r18Isf440VecZg3i)

