# Awesome-Mapping-GIS-Libraries

# Top Mapping & GIS Libraries Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on Web Map Rendering, Geospatial Analysis & Self-Hosted Tile Infrastructure*  
**Last updated: October 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Mapping & GIS Libraries**. These tools render interactive maps in the browser—handling tile loading, layer styling, projection transformations, and spatial data visualization—so developers can build location-aware applications without implementing map engines from scratch.

**Examples** include Leaflet, OpenLayers, MapLibre GL JS, Mapbox GL JS, Google Maps API, HERE, TomTom, and CesiumJS (the category leaders).

**Open-source emphasis**: This section is heavily expanded with every major active library for self-hosting, avoiding per-map-load SaaS fees, and controlling the rendering layer. The open-source landscape is anchored by **Leaflet** (the lightweight raster standard with a massive plugin ecosystem), **OpenLayers** (the GIS-grade library with broad format and projection support), and **MapLibre GL JS** (the vector-tile fork of Mapbox GL JS after its license change), with **CesiumJS** serving 3D globe and geospatial visualization needs.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

| Product | Description | Pricing | Free Tier Limit |
| :--- | :--- | :--- | :--- |
| **[Mapbox](https://www.mapbox.com/)** | Vector tile maps with Mapbox GL JS, Studio for style editing, and extensive location APIs. | Billed by **tile requests** and MAUs for mobile. Vector and raster tiles counted separately; compositing sources in Studio reduces tile count . | **Free tier included** but exact limits not published on public pricing docs; requires account for current allowances . |
| **[Google Maps Platform](https://developers.google.com/maps)** | Comprehensive maps, routes, and places APIs with global coverage. | **Starter**: $100/month (50,000 calls). **Essentials**: $275/month (100,000 calls). **Pro**: $1,200/month (250,000 calls). Overage at standard pay-as-you-go rates . | **No-cost SKUs** (Maps SDK, Embed) do not count toward subscription limits. $200 monthly credit for new accounts (legacy). |
| **[HERE Technologies](https://www.here.com/)** | Location platform with maps, routing, and traffic APIs. | Freemium **250,000 requests/month** free; pay-as-you-go from **€1 per 1,000 transactions**; enterprise volume pricing available . | **250,000 requests/month** free tier. |
| **[TomTom](https://www.tomtom.com/)** | Maps, traffic, and routing APIs with Orbis Maps. | **Map Display API Vector Tiles**: free 200,000/month. **Raster Tiles**: free 20,000/month. **Places Search**: free 10,000/month. Pay-as-you-go beyond free tiers . | Free tiers vary by API: **200K vector tiles/month**, 20K raster tiles, 10K place searches, 2.5K geocoding requests. No credit card required for evaluation . |
| **[MapTiler](https://www.maptiler.com/)** | Map hosting, geocoding, and self-hosted map server options. | **On-prem Free**: $0 for non-commercial, max 100 MAU. **On-prem Standard**: $2,500/year for single internal app, max 500 MAU. **Custom**: annual contract for larger deployments . | **On-prem Free**: non-commercial only, 100 MAU maximum. No free commercial tier for self-hosted . |
| **[CARTO](https://carto.com/)** | Cloud-native location intelligence platform built on data warehouses. | **Basemaps Commercial**: $500/month or $5,000/year for up to 10M requests. **Commercial Plus**: $1,500/month or $15,000/year for 50M requests . | **Non-commercial**: 5M tile requests/month free. **Commercial**: 1M tile requests/month free (requires attribution, API key) . |
| **[Esri ArcGIS](https://www.esri.com/)** | Enterprise GIS platform with ArcGIS Online and ArcGIS Pro. | **ArcGIS Online Professional Plus**: ~₩20,572,000/year (~$15,000 USD) per user (1-49 tier) . Enterprise agreements custom. | **ArcGIS Free Tier**: limited ArcGIS Online features for personal use. Developer accounts available for testing. |

## Open-Source GitHub Projects

- **[Leaflet](https://github.com/Leaflet/Leaflet)** [![GitHub Stars](https://img.shields.io/github/stars/Leaflet/Leaflet?style=social&color=white)](https://github.com/Leaflet/Leaflet/stargazers)  
  **The lightweight raster standard.** Small API, quick setup, and a mature plugin ecosystem. **Strengths**: fastest rendering for small-to-medium feature counts (up to 10,000 features); simple to learn; works with any raster tile source . **Leaflet 2.0** is in development with breaking changes—migration will be required for some plugins . **Trade-offs**: no native vector-tile styling or WebGL rendering; limited projection support. Best for straightforward raster basemaps, quick prototypes, and applications where the plugin ecosystem matters.

- **[OpenLayers](https://github.com/openlayers/openlayers)** [![GitHub Stars](https://img.shields.io/github/stars/openlayers/openlayers?style=social&color=white)](https://github.com/openlayers/openlayers/stargazers)  
  **The GIS-grade library.** Broad data-source, projection, and rendering support. **v10.10.0** (July 2026) added text support in WebGL vector renderers, improved tile rendering performance, GeoZarr non-spatial dimension selection, and deprecated BingMaps source (Bing Maps for Enterprise retires June 2028) . **Strengths**: handles complex GIS formats, projections, and advanced layer composition; excels at large line and polygon datasets . **Trade-offs**: steeper learning curve than Leaflet; more configuration. Best for GIS professionals, complex spatial data, and applications requiring projection flexibility.

- **[MapLibre GL JS](https://github.com/maplibre/maplibre-gl-js)** [![GitHub Stars](https://img.shields.io/github/stars/maplibre/maplibre-gl-js?style=social&color=white)](https://github.com/maplibre/maplibre-gl-js/stargazers)  
  **The vector-tile standard after Mapbox's license change.** Fork of Mapbox GL JS with a community-governed, BSD-licensed alternative. **v6 is in development** with two major breaking changes: **dropping WebGL1 support** (WebGL2 only) and **transitioning from CommonJS to ESM** . **Strengths**: style-driven vector rendering, runtime basemap styling and localization, pitch/bearing, and WebGL performance for large point datasets . **Trade-offs**: larger configuration surface than Leaflet; WebGL1 removal may affect older browser support. Best for style-driven maps, vector tiles, and applications needing runtime customization.

- **[CesiumJS](https://github.com/CesiumGS/cesium)** [![GitHub Stars](https://img.shields.io/github/stars/CesiumGS/cesium?style=social&color=white)](https://github.com/CesiumGS/cesium/stargazers)  
  **The 3D globe standard.** **v1.146** (October 2026) extracts core math/geometry/time primitives into a separate `@cesium/core` package, improves 3D Tiles 2.0 vector rendering, and reduces load time/memory for implicitly tiled tilesets by 23x/13x on a benchmark dataset . **Strengths**: true 3D geospatial visualization, terrain, and 3D Tiles support. Best for 3D globes, terrain visualization, and applications requiring volumetric geospatial data.

### Additional Strong Open-Source Options

- **deck.gl** — WebGL-powered visualization framework for large-scale geospatial data. Best for high-performance data overlays on top of MapLibre or other basemaps.
- **ol-mapbox-style** — OpenLayers plugin for applying Mapbox style documents to OpenLayers maps. Best for teams wanting Mapbox-style vector rendering within OpenLayers.
- **MapLibre Native** — Native mobile SDKs (iOS, Android) for MapLibre vector maps. Best for mobile applications requiring vector tile rendering.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- **Library choice depends on your hardest requirement**: raster basemap → Leaflet; vector styling/pitch → MapLibre GL JS; GIS formats/projections → OpenLayers; 3D globe → CesiumJS .
- **Performance scales differently**: Leaflet and OpenLayers excel for up to 10,000 features; Mapbox/MapLibre pull ahead at 50,000+ . Benchmark against your actual data volume.
- **SaaS free tiers vary and change**: TomTom's 200K vector tiles/month is generous; HERE's 250K requests/month is broad; CARTO's commercial free tier is 1M tiles with attribution requirements . Verify current terms before production deployment.
- **MapLibre v6 drops WebGL1 and CommonJS**: if you support older browsers or use CommonJS, plan for migration before upgrading .

---

**Made for web developers, GIS analysts, and organizations building location-aware applications.**  
Let's make mapping and GIS more open, performant, and appropriately scoped.
