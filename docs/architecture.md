# Architecture Overview

Metrics Flow:
Node → Kubelet → Scraper → Metrics Server → API Layer → Storage → Dashboard

## Design Decisions:
- Lightweight scraper for low overhead
- Aggregated cluster-level metrics storage
- API-first design for observability tools
