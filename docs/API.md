# Bundus DNA Platform - API Documentation

## Base URL

```
https://api.bundus-dna.com/v1
```

## Authentication

All requests require a valid JWT token in the Authorization header:

```
Authorization: Bearer <your_jwt_token>
```

---

## Core Endpoints

### DNA Upload

#### POST `/dna/upload`

Upload DNA sequence files (VCF format).

**Request:**
```json
{
  "file": "<binary VCF data>",
  "file_format": "vcf",
  "sample_id": "sample_001"
}
```

**Response:**
```json
{
  "success": true,
  "upload_id": "upload_abc123",
  "status": "processing",
  "timestamp": "2026-06-05T04:00:00Z"
}
```

**Status Codes:**
- `202 Accepted` - File accepted for processing
- `400 Bad Request` - Invalid file format
- `413 Payload Too Large` - File exceeds size limit (2GB)

---

### DNA Analysis

#### GET `/dna/analysis/{upload_id}`

Retrieve analysis results for uploaded DNA.

**Response:**
```json
{
  "upload_id": "upload_abc123",
  "status": "completed",
  "analysis_results": {
    "total_variants": 4500000,
    "chromosomes_analyzed": 23,
    "ancestry": {
      "european": 0.85,
      "african": 0.10,
      "asian": 0.05
    }
  }
}
```

---

### Variants

#### GET `/variants`

List genetic variants.

**Query Parameters:**
```
?chromosome=1&start=1000&end=10000&impact=high
```

**Response:**
```json
{
  "data": [
    {
      "rsid": "rs123",
      "chromosome": "1",
      "position": 5000,
      "reference": "A",
      "alternate": "G",
      "genotype": "AG",
      "consequence": "missense_variant",
      "impact": "moderate"
    }
  ],
  "total": 1500,
  "page": 1,
  "per_page": 50
}
```

---

### Ancestry

#### GET `/ancestry`

Get ancestry composition.

**Response:**
```json
{
  "primary_ancestry": "European",
  "percentages": {
    "european": 0.852,
    "african": 0.098,
    "asian": 0.032,
    "oceanian": 0.018
  },
  "haplogroups": {
    "maternal": "H1c",
    "paternal": "R1b"
  }
}
```

---

### Traits

#### GET `/traits`

List available genetic traits.

**Query Parameters:**
```
?category=health&limit=20
```

**Response:**
```json
{
  "data": [
    {
      "trait_id": "longevity",
      "name": "Longevity",
      "category": "health",
      "description": "Genetic markers associated with lifespan",
      "genes": ["FOXO3", "APOE"],
      "variants": 15
    }
  ],
  "total": 45
}
```

#### GET `/traits/{trait_id}`

Get trait analysis.

**Response:**
```json
{
  "trait_id": "longevity",
  "name": "Longevity",
  "score": 8.2,
  "interpretation": "Your genetic markers suggest above-average longevity potential.",
  "contributing_genes": [
    {
      "gene": "FOXO3",
      "variants": ["rs2802292"],
      "effect": "positive",
      "odds_ratio": 1.24
    }
  ]
}
```

---

### User Profile

#### GET `/profile`

Get user profile.

**Response:**
```json
{
  "user_id": "user_123",
  "email": "user@example.com",
  "created_at": "2026-01-15T10:00:00Z",
  "uploads": 3,
  "analyses": 3,
  "subscription": "premium"
}
```

---

## Pagination

List endpoints support pagination:

```
GET /variants?page=2&per_page=50
```

**Response Headers:**
```
X-Total-Count: 1500
X-Page: 2
X-Per-Page: 50
X-Total-Pages: 30
```

---

## Error Handling

### Error Response Format

```json
{
  "error": {
    "code": "INVALID_REQUEST",
    "message": "Required field 'file' is missing",
    "timestamp": "2026-06-05T04:00:00Z"
  }
}
```

### Common Error Codes

- `INVALID_REQUEST` (400) - Malformed request
- `UNAUTHORIZED` (401) - Missing or invalid authentication
- `FORBIDDEN` (403) - Permission denied
- `NOT_FOUND` (404) - Resource not found
- `CONFLICT` (409) - Resource already exists
- `RATE_LIMITED` (429) - Too many requests
- `INTERNAL_ERROR` (500) - Server error

---

## Rate Limiting

- **Free Tier**: 100 requests/hour
- **Premium Tier**: 1000 requests/hour
- **Enterprise**: Unlimited

**Headers:**
```
X-RateLimit-Limit: 1000
X-RateLimit-Remaining: 950
X-RateLimit-Reset: 1686225600
```

---

**Last Updated**: June 5, 2026
**Version**: 1.0
