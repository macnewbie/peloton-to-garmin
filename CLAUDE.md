# Peloton to Garmin — Claude Context

## Project Overview
Fork of the open-source [philosowaffle/peloton-to-garmin](https://github.com/philosowaffle/peloton-to-garmin) project.
Syncs Peloton workouts to Garmin Connect automatically. Supports Bike, Tread, Rower,
Strength, Meditation, Outdoor and more. Earns Garmin badges and contributes to VO2 Max / TSS.

## Fork Notes
- Upstream: `https://github.com/philosowaffle/peloton-to-garmin`
- Any local customizations should be documented here as they're made
- Before making changes, check if upstream has addressed the issue first

## Tech Stack
- **.NET / C#** — solution file `PelotonToGarmin.sln`
- **Docker** — `docker/` directory with compose configs
- **Docs:** MkDocs (`mkdocs/`) — published to GitHub Pages

## Running
See the [Wiki](https://philosowaffle.github.io/peloton-to-garmin) for full setup instructions.

### Docker (recommended)
```bash
docker compose -f docker/docker-compose.yml up
```

### Configuration
Copy `configuration.example.json` → `configuration.json` and fill in credentials.
**Never commit `configuration.json`** — it contains Peloton + Garmin credentials.

## Important Notes
- Credentials (Peloton + Garmin) are stored in `configuration.json` — **excluded from git**
- For Docker WebUI or GitHub Actions deployments, credentials are encrypted at rest
- Console/headless deployments store credentials in plaintext — use with caution
- `global.json` pins the .NET SDK version
