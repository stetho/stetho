# Hi, I'm Steve 👋

Enterprise IT Executive and Infrastructure Architect based in South London, with 35 years of experience scaling infrastructure for some of the most technically demanding organisations in the world — Google DeepMind, Shazam, and Apple.

I'm currently between roles after a redundancy and using the time to build things I've always wanted to build, sharpen my Python, and start learning Go.

---

## What I'm building

### Tempest Weather Station System
A multi-repo personal weather station project built around a WeatherFlow Tempest
station mounted on my house in Selhurst, South London.

| Repo | What it does | Status |
|---|---|---|
| [tempest-logger](https://github.com/stetho/tempest-logger) | Polls the Tempest API every 10 minutes and stores observations in SQLite, running 24/7 in Docker | ✅ Live |
| [tempest-analytics](https://github.com/stetho/tempest-analytics) | Pure Python library of meteorological calculations — Zambretti forecaster, Beaufort scale, clear sky index, frost risk, storm tracking and more. 120 tests. | ✅ Live |
| [tempest-dashboard](https://github.com/stetho/tempest-dashboard) | Dark-themed Flask dashboard with live conditions, 24-hour charts, records tracker, storm predictor and derived analytics. Live at [tempest.23wwc.cloud](https://tempest.23wwc.cloud) | ✅ Live |
| [tempest-camera](https://github.com/stetho/tempest-camera) | Captures frames from a rooftop RTSPS camera stream, composites live weather readings and Zambretti forecast onto the image, and generates a daily timelapse video | ✅ Live |

### Aircraft & Environmental Noise Correlation
Using tar1090 ADS-B data from a Raspberry Pi in the loft, audio extracted from
a Unifi G3 Flex rooftop camera via FFmpeg, and Tempest weather data to investigate
whether wind direction affects aircraft noise levels over South London. Data flows
into InfluxDB with Grafana for visualisation.

*In progress*

### Monzo Spending Intelligence
A Python dashboard that reads from a live Monzo-connected Google Sheet via the
Google Sheets API and produces monthly spending breakdowns, subscription detection
with price change alerts, unusual spending flags, savings rate tracking and foreign
currency summaries. Built to be useful to any Monzo customer.

*Planned*

### Tube Delay Predictor
Uses the TfL open API to analyse historical delay patterns and predict which lines
are likely to be delayed at what times of day. Genuinely useful for South London
commuters and a good excuse to do some proper data analysis.

*Planned*

### Mini Job Queue System
A lightweight job queue implementation in Go — a learning project that covers
goroutines, channels, persistence and worker pools. Go's concurrency model makes
it a natural fit for this kind of problem.

*Planned*

### Improv Scene Generator
A tool that generates improv scene setups from random parameters — location,
relationship, object, game — with suggested structures and exercises. Built with
the Claude API. A deliberately fun project from someone with a background in
improv comedy.

*Planned*

### Wordle Solver
An algorithm that solves Wordle optimally using information theory — picks the
best starting word and narrows down candidates after each guess. A clean showcase
of algorithmic thinking with a very shareable output.

*Planned*

### CI/CD Pipeline
GitHub Actions workflows to automatically build and push Docker images to a
container registry on every push to main, replacing the current manual deployment
process across all tempest repos.

*Planned*
---

## Background

**Google DeepMind** (2013-2025) — IT Operations Manager. Built and scaled the global IT operations framework from early-stage startup through Alphabet acquisition, supporting 6,000+ personnel including 4,000+ AI researchers. Designed infrastructure for landmark AI milestones including AlphaGo, AlphaFold, and Gemini. Engineered the data privacy architecture for DeepMind Health, processing live NHS patient data under medical regulatory frameworks.

**Shazam** (2009-2013) — IT Operations Manager. Scaled infrastructure during hyper-growth, pioneering predictive auto-scaling and leading the transition to Infrastructure-as-Code with Puppet.

**Research In Motion (BlackBerry)** (2003-2008) - Provisioning Infrastructure Engineer. Maintained 24/7 operational reliability of RIM's global carrier provisioning infrastructure (WebLogic/Oracle) at peak scale — supporting 85 million active devices across virtually every carrier and MVNO worldwide, underpinning service entitlement, service book delivery, and carrier billing for RIM's entire consumer device estate.

**Apple UK** (1989-1996) — Technical Support Engineer. Part of Apple's foundational UK expansion.

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
