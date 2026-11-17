# Ride Prep Agent – ANWB Ontmoetingsplek Team

Mobile web app (PWA) to prepare team rides: road, gravel and beach.

## Features
- **Plan your ride first:** enter date, start time and distance (+ average speed) → expected weather for exactly that period (hourly), tides around the ride, low-tide fit for beach rides with a suggested start time, daylight/lights and gust warnings
- 14-day weather overview (tides 8 days ahead) and low/high tide times for 18 NL/BE beach locations (coverage follows primastrandje.cc)
- Ride-window advice: beach = low tide ±2 h in daylight; road/gravel = best 3 h daylight block
- Wind strategy (start into the wind), kit advice, shareable team briefing (WhatsApp)
- Per-rider tyre pressure (SILCA-style inputs, approximation; beach surfaces are an extension)
- Route planning links to Komoot, Strava and Garmin + draft GPX export

## Install on your phone
1. Open the GitHub Pages URL in Safari (iPhone) or Chrome (Android).
2. iPhone: Share → *Add to Home Screen*. Android: menu → *Install app*.

## Data sources
- Weather: [Open-Meteo Forecast API](https://open-meteo.com) (free, no key)
- Tides: Open-Meteo Marine API `sea_level_height_msl` (model-based, ±15–30 min). Always confirm on [primastrandje.cc](https://primastrandje.cc) or [Rijkswaterstaat Waterinfo](https://waterinfo.rws.nl).
- Tyre pressure reference: [SILCA Pro Tire Pressure Calculator](https://silca.cc/en-eu/pages/pro-tire-pressure-calculator)

## Privacy
Rider profiles (incl. body weight) are stored only in the browser of each device (localStorage). Nothing is sent to a server.

## Deploy
Static site — GitHub Pages serves the `main` branch root. No build step.

## Roadmap
- Strava / Komoot / Garmin account connection (requires registered API apps + small backend for OAuth secrets) — decision pending
- Dutch UI
