# 🛰️ Agri-Sentry-core: Spatial Intelligence Engine

A production-grade, climate-resilient agricultural intelligence backend designed to bridge the $6B parametric insurance trust gap in the Terai belt, West Bengal. 

---

## ⚙️ The Agri-Sentry Data Pipeline
Our architecture transforms raw satellite telemetry into actionable financial intelligence:

1. **Ingestion:** Automated fetch of Sentinel-1 SAR imagery from Google Earth Engine.
2. **Purification:** Removing noise, buffering polygons, and fixing CRS geometry.
3. **Storage:** Secure storage in an RLS-enabled PostGIS vault.
4. **Analysis:** Multi-temporal anomaly detection (SAR backscatter analysis) to verify flood events.

---

## 🛠️ Engineering Mission
Agri-Sentry-core solves the "Basis Risk" problem in parametric insurance by converting noisy, cloud-covered SAR satellite data into clean, verifiable flood-event triggers.

## 🏗️ System Architecture
The system is built as a modular pipeline where data moves from raw telemetry to actionable intelligence:

| Phase | Component | Technical Focus |
|-------|-----------|-----------------|
| **01** | [Spectral Vectorization](./day01-first-satellite-analysis) | NumPy-optimized NDVI calculations (61x faster than iterators). |
| **02** | [Spatial Math Engine](./day02-coordinate-systems) | WGS84 to UTM Zone 45N conversion for precision area calculation. |
| **03** | [Secure Spatial Vault](./day03-geopandas%2Bpostgis) | PostGIS database with Row-Level Security & GiST Indexing. |
| **04** | [GEE Handshake](./day04-satellite-handshake-for-SAR) | Sentinel-1 SAR (VV Polarization) historical anomaly detection. |

---

## ⚙️ Core Technical Capabilities
* **Cloud-Native Ingestion:** API-driven handshake with Google Earth Engine to process >7 years of historical backscatter data.
* **Database Hardening:** Idempotent schema design with 3-meter inner-core buffering to eliminate edge-case noise in farm boundary sampling.
* **Compute Efficiency:** Vectorized raster processing pipelines built to handle large-scale temporal data without memory overhead.

---

## 🛠️ Technology Stack
* **Earth Observation:** Sentinel-1 (SAR GRD), Sentinel-2, Google Earth Engine API
* **Spatial & Database:** PostGIS, PostgreSQL, GeoPandas, Rasterio, Shapely
* **Language & Math:** Python, NumPy (Vectorization)

---

## 🛡️ Methodology
Agri-Sentry-core follows a **Human-in-the-Loop (HITL)** engineering framework. State-of-the-art AI models act as "Computational Sub-Contractors" for architectural hardening and pipeline optimization, while every SQL constraint, security protocol, and spatial algorithm is manually audited and validated by the Lead Engineer.
