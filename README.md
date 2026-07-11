# Hi, I'm Steve 👋

Enterprise IT Executive and Infrastructure Architect based in South London, with 35 years of experience scaling infrastructure for some of the most technically demanding organisations in the world - Google DeepMind, Shazam, and Apple.

I'm currently between roles after a redundancy and using the time to build things I've always wanted to build, sharpen my Python, and start learning Go.

---

## What I'm building

### Tempest Weather Station System
A multi-repo personal weather station project built around a WeatherFlow Tempest
station mounted on my house in South London. I noticed that this weather station
produces a wealth of data through its API but it does nothing with it. The App 
will tell you how hot it is and if it's raining or not but that's it. So I started
with a simple web page to display the API data and then I Googled what I could do
with this rich source of hyperlocal weather data. That led to things like the 
Zambretti forecaster and the Beaufort scale. I then pasted the API output into 
Gemini, Claude and ChatGPT and asked what they could do with the data. And now it's
all gone a bit crazy. Live at [tempest.23wwc.cloud](https://tempest.23wwc.cloud) so
you too can see how much information you can get out of a weather station. If you
have a Tempest weatherstation and want to try this, you'll need a machine running 24/7
but it should run on a Raspberry Pi without breaking a sweat.

Although all these subprojects are now marked live I've still got a backlog of ideas. 

| Repo | What it does | Status |
|---|---|---|
| [tempest-logger](https://github.com/stetho/tempest-logger) | Polls the Tempest API every 10 minutes and stores observations in SQLite, running 24/7 in Docker. Logs the full set of API fields including WBGT, delta-T, heat index, wind chill and lightning epoch. | ✅ Live |
| [tempest-analytics](https://github.com/stetho/tempest-analytics) | Pure Python library of meteorological calculations - Zambretti forecaster, Beaufort scale, clear sky index, frost risk, storm tracking, heatwave detection, thermal stress (WBGT), UV exposure and burn time, pollution dispersion index, and pollen risk. 120+ tests. | ✅ Live |
| [tempest-dashboard](https://github.com/stetho/tempest-dashboard) | Flask dashboard with live conditions, 24-hour charts, records tracker, and a growing suite of derived analytics. Tabs cover temperature, wind, pressure, solar, rain, lightning, air quality, camera and microclimate. Features include Met Office heatwave detection, UK DAQI air quality index, UV exposure tracker for three skin types, pollen risk from CAMS via Open-Meteo, thermal stress index, pollution dispersion index, Zambretti forecast, Bayesian rain prediction, and evapotranspiration. Live at [tempest.23wwc.cloud](https://tempest.23wwc.cloud) | ✅ Live |
| [tempest-camera](https://github.com/stetho/tempest-camera) | Captures frames from a rooftop RTSPS camera stream, composites live weather readings and Zambretti forecast onto the image, and generates a daily timelapse video. | ✅ Live |
| [tempest-air](https://github.com/stetho/tempest-air) | Systemd service running on a Raspberry Pi 3B+ with a Pimoroni Enviro+ HAT and PMS5003 sensor. Polls particulate matter readings every 60 seconds, buffers locally to SQLite, and flushes to the dashboard every 5 minutes. Feeds the air quality tab with PM1.0, PM2.5, PM10, particle counts, US EPA AQI and UK DAQI. | ✅ Live |

### Projects Backup Tool
A Python CLI tool that intelligently backs up a developer's projects directory.
Scans for project types (Python, Go, Node etc.), checks each has a remote git
origin, excludes venvs and build artifacts automatically, creates a manifest with
metadata, and supports multiple backup destinations (local, Dropbox, Google Drive,
Nextcloud) via a config file. Designed to be useful to any developer, not just me.

*Planned*

### JobTrail - Job Search Intelligence
A self-hosted job search tracker built as a Flask web app with a dark theme,
multi-user support, and a full contacts/organisations CRM. Tracks every application
through its complete lifecycle with a timeline of events, not just a status field.

Designed to answer questions a spreadsheet can't: which sources convert best,
how long does the average response take, which agencies are actually performing,
and what needs following up today.

Features:
- Full pipeline view with funnel metrics and conversion rates
- Organisations and contacts CRM - track agencies, companies and individual
  recruiters separately, with contacts shared across applications
- Complete event timeline per application - every email, call and interview logged
- Source intelligence - differentiate direct, agency, LinkedIn, referral and headhunted
- Follow-up reminders and cold application detection
- Deployable as a Docker container for anyone to self-host

*Paused* - I got Capacities to bend to my will and use that for tracking my job applications. Writing a job tracking system when you should be looking for a job is a distraction, but I still think it will be a genuinely useful tool when finished.

### ISO 27001 Control Evidence Collector
A Python CLI tool that automatically gathers evidence for common ISO 27001 Annex A
technical controls from a Linux system - disk encryption status, password policies,
open ports, running services, user accounts, sudo access, failed login attempts and
more. Produces a structured report mapped to ISO 27001 controls. Built by a certified
ISO 27001 auditor with 35 years of enterprise IT experience (me).

*Planned*

### Google Coral Cloud Cover Classifier
Using a Google Coral USB TPU accelerator connected to the homelab server to run
real-time ML inference on the rooftop weather camera feed. Classifies sky conditions
(clear, partly cloudy, overcast, stormy) directly from the image and cross-validates
against the clear sky index calculated from solar radiation data.

*Planned*

### Tube Delay Predictor
Uses the TfL open API to analyse historical delay patterns and predict which lines
are likely to be delayed at what times of day. Genuinely useful for South London
commuters and a good excuse to do some proper data analysis.

*In progress* - tfl-delay-collector has been running since June 2026 and has accumulated over 1.2 million records. Three analysis notebooks are complete covering data caveats, delay patterns by corridor, and further analysis. The Thameslink corridor emerges as the worst performer; Victoria terminal shows near-zero delays. Full predictive modelling follows once the dataset matures.

### gedcom-toolkit
A Python CLI tool for analysing GEDCOM family tree files as directed graphs. Commands include stats, validate, findid, findrelationship, rn, and sources, with 94 tests. Further commands in development covering places, duplicates, completeness, diff, surnames, timeline, and geographic export. And if you've landed here because you're researching your family tree and your surname is Thompson (or Whitmore, Todd, Toone, Cowan and many others) my tree is on Ancestry.

*In progress*

### Mini Job Queue System
A lightweight job queue implementation in Go - a learning project that covers goroutines, channels, persistence and worker pools. Go's concurrency model makes it a natural fit for this kind of problem.

*Planned*

### Tempest Alerts
A Go service that connects to the Tempest WebSocket API and fires notifications
when configurable thresholds are crossed - frost risk, storm approach, UV spikes,
lightning within range. First real-world Go project built on existing Tempest
infrastructure.

*Planned*

### Improv Scene Generator
A tool that generates improv scene setups from random parameters - location,
relationship, object, game - with suggested structures and exercises. Built with
the Claude and Gemini APIs. A deliberately fun project from someone with a background in
improv comedy (me). Think of it as computerising Clive Anderson.

*Planned*

### CI/CD Pipeline
GitHub Actions workflows to automatically build and push Docker images to a
container registry on every push to main, with no-cache builds to ensure dependencies
are always fresh.

*Complete*

### Beautiful Dead Ends
I've often been aware of things in general that people say can't be done because it's very difficult. Maths has a lot of these so I set out to understand - for myself - why they're impossible. Follow along in beautiful-dead-ends as I try and put the pieces together.

Topics covered so far: Collatz Conjecture, Hadwiger Conjecture, Kaprekar's Constant, Untouchable Numbers, Abundant Numbers, Goldbach's Conjecture, Derangements, and Waring's Problem.

*In progress*

### Everything I learned at DeepMind
It turns out that Artificial Intelligence and Machine Learning are quite important topics. When I joined DeepMind as their first IT guy I didn't realise how important it would be but I took the opportunity to learn as much as I could. In what-i-learned-about-ai I've tried to document all of it in an accessible way. Unfortunately I quickly discovered that explaining the equations leads to explaining the equations that explain the equations and it just got messy. So this repo is essentially a series of cheat-sheets for me but I hope others find it useful.

Topics covered: LSTMs, SGD, Transformers, Attention, GANs, RLHF, Actor-Critic/PPO, Markov Processes, MCMC, KNN, SVM, Bagging and Random Forests. CNNs and ResNets in progress.

### Various Data Projects
uk-climate-analysis is my attempt to address a certain aspect of the "warm summers" we keep having. Five notebooks complete analysing Met Office HadUK-Grid regional data. Key finding: the warming rate has nearly tripled, and +2°C above baseline arrives in the late 2030s under the current trend. I think it's the only repo where I get angry about something.

sen-exclusions-analysis was inspired by a conversation with my social worker wife. I didn't actually find what I went looking for but I did find something else.

crime-stats-uk - the main thing I learned from this is that the UK's largest police force - the one that covers where I live - is absolutely useless at supplying data to data.police.uk.

### tier-zero-grimoire
A tool I wrote initially for use at DeepMind. Export all your support tickets and your company knowledge base, run this script on the collected data, receive data that can be pasted into a Tier 0 LLM-powered support chatbot. There are three versions, the only difference originating from me testing which mainstream LLM (Gemini, Claude, ChatGPT) returned the best interpretation of the supplied documentation.

*Complete*

### Personal nonsense
**ha-blind-spots** - Do you have Home Assistant? Do you have motion sensors and smart lighting? Does every motion sensor in room X control a light in room X? No? You're missing an automation. That's it - it looks for sensible matches between inputs and outputs and lists things you might have missed. Phase 1 complete and working; Phase 2 (LLM suggestion layer) and Phase 3 (HTML report) in progress.

**mlops-homelab** - The scripts I used to build a basic ML workflow in my homelab so I can keep my MLOps knowledge up to date and attempt to deploy large models on a Kubernetes cluster running on some Raspberry Pis. Because I can.

**content-coding** - Engineering pipeline that implements academic qualitative content analysis paradigms at scale.

---

## Background

**Google DeepMind** (2013-2026) - IT Operations Manager. Built and scaled the global IT operations framework from early-stage startup through Alphabet acquisition, supporting 6,000+ personnel including 4,000+ AI researchers. Designed infrastructure for landmark AI milestones including AlphaGo, AlphaFold, and Gemini. Engineered the data privacy architecture for DeepMind Health, processing live NHS patient data under medical regulatory frameworks.

**Shazam** (2009-2013) - IT Operations Manager. Scaled infrastructure during hyper-growth, pioneering predictive auto-scaling and leading the transition to Infrastructure-as-Code with Puppet.

**Research In Motion (BlackBerry)** (2003-2008) - Provisioning Infrastructure Engineer. Maintained 24/7 operational reliability of RIM's global carrier provisioning infrastructure (WebLogic/Oracle) at peak scale - supporting 85 million active devices across virtually every carrier and MVNO worldwide, underpinning service entitlement, service book delivery, and carrier billing for RIM's entire consumer device estate.

**Contracting Work** (1996-2003) - Somehow after getting made redundant from Apple I started off contracting as a support person in many London-based Advertising Agencies and Publishing Companies, mainly showing them how to install Quark XPress, but ended up a Lotus Domino and Microsoft Exchange administrator.

**Apple UK** (1989-1996) - Technical Support Engineer. Part of Apple's foundational UK expansion.

---

## What I'm good at

- Enterprise infrastructure architecture at scale especially when starting at zero
- Python automation and API integration
- DevOps, IaC, and real-time telemetry
- AI governance, data privacy, and compliance frameworks
- Leading global engineering teams and multi-million pound budgets

---

## Currently learning

- **Go** - building a WebSocket-based lightning alert service as my first real Go project
- Applying Python skills I've used professionally for years to larger structured projects for the first time
- Exploring the intersection of my DeepMind experience with the socio-legal AI governance frameworks I'm studying at the Open University

---

## Open to opportunities

I'm actively looking for senior roles in infrastructure, platform engineering, technical operations, or AI governance - particularly in organisations where technical depth and leadership experience both matter.

📧 stevet@me.com | 📍 South London

---

*This profile is a work in progress - more projects incoming.*
