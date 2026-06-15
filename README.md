# Hi, I'm Steve 👋

Enterprise IT Executive and Infrastructure Architect based in South London, with 35 years of experience scaling infrastructure for some of the most technically demanding organisations in the world — Google DeepMind, Shazam, and Apple.

I'm currently between roles after a redundancy and using the time to build things I've always wanted to build, sharpen my Python, and start learning Go.

---

## What I'm building

### Tempest Weather Station System
A multi-repo personal weather station project built around a WeatherFlow Tempest
station mounted on my house in Selhurst, South London.

| Repo | What it does |
|---|---|
| [tempest-logger](https://github.com/stetho/tempest-logger) | Polls the Tempest API every 10 minutes and stores observations in SQLite, running 24/7 in Docker |
| [tempest-analytics](https://github.com/stetho/tempest-analytics) | Pure Python library of meteorological calculations — Zambretti forecaster, Beaufort scale, clear sky index, frost risk, storm tracking and more. 120 tests. |
| [tempest-dashboard](https://github.com/stetho/tempest-dashboard) | Dark-themed Flask dashboard with live conditions, 24-hour charts, records tracker and derived analytics. Live at [tempest.23wwc.cloud](https://tempest.23wwc.cloud) |
| [tempest-camera](https://github.com/stetho/tempest-camera) | Captures frames from a rooftop RTSPS camera stream and composites live weather readings onto the image as an overlay, updated every 10 minutes |

### Aircraft & Environmental Noise Correlation
Using tar1090 ADS-B data from a Raspberry Pi in the loft, audio extracted from
a Unifi G3 Flex rooftop camera via FFmpeg, and Tempest weather data to investigate
whether wind direction affects aircraft noise levels over South London. Data flows
into InfluxDB with Grafana for visualisation.

---

## Background

**Google DeepMind** (2013–2025) — IT Operations Manager. Built and scaled the global IT operations framework from early-stage startup through Alphabet acquisition, supporting 6,000+ personnel including 4,000+ AI researchers. Designed infrastructure for landmark AI milestones including AlphaGo, AlphaFold, and Gemini. Engineered the data privacy architecture for DeepMind Health, processing live NHS patient data under medical regulatory frameworks.

**Shazam** (2009–2013) — IT Operations Manager. Scaled infrastructure during hyper-growth, pioneering predictive auto-scaling and leading the transition to Infrastructure-as-Code with Puppet.

**Apple UK** (1989–1996) — Technical Support Engineer. Part of Apple's foundational UK expansion.

---

## What I'm good at

- Enterprise infrastructure architecture at scale
- Python automation and API integration
- DevOps, IaC, and real-time telemetry
- AI governance, data privacy, and compliance frameworks
- Leading global engineering teams and multi-million pound budgets

---

## Currently learning

- **Go** — building a WebSocket-based lightning alert service as my first real Go project
- Applying Python skills I've used professionally for years to larger structured projects for the first time
- Exploring the intersection of my DeepMind experience with the socio-legal AI governance frameworks I'm studying at the Open University

---

## Open to opportunities

I'm actively looking for senior roles in infrastructure, platform engineering, technical operations, or AI governance — particularly in organisations where technical depth and leadership experience both matter.

📧 stevet@me.com | 📍 South London

---

*This profile is a work in progress — more projects incoming.*
