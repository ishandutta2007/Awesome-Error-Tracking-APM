# Awesome-Error-Tracking-APM

# Top Error Tracking & APM Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on Exception Monitoring, Performance Tracing & Self-Hosted Observability*  
**Last updated: October 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Error Tracking & Application Performance Monitoring (APM)**. These tools help engineering teams detect production exceptions, trace slow requests, and understand user-impacting failures—moving from reactive log-grepping to proactive, context-rich debugging.

**Examples** include Sentry, Datadog, Raygun, Bugsnag, Rollbar, New Relic, Dynatrace, AppDynamics, LogRocket, and TrackJS (the category leaders).

**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting, Sentry-SDK compatibility, and transparent telemetry pipelines—ideal for teams that need data sovereignty, predictable costs, and auditable monitoring infrastructure. The open-source landscape is anchored by **Sentry Self-Hosted** (source-available, full-featured) and its lightweight compatible alternatives **GlitchTip** and **Bugsink**, with strong full-stack options in **Highlight.io** and **HyperDX**, plus OpenTelemetry-native APM platforms **SigNoz** and **Uptrace**.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[Sentry](https://sentry.io/)**  
  The category-defining error tracking and performance monitoring platform. Supports 100+ SDKs across languages and frameworks, with issue grouping, release tracking, and session replay. Team plan starts at $26/user/month with 50,000 errors included .

- **[Datadog](https://www.datadoghq.com/)**  
  Full-stack observability platform covering APM, infrastructure monitoring, logs, and real user monitoring (RUM). Deep integration across the entire stack but pricing scales with hosts, custom metrics, and log volume.

- **[Raygun](https://raygun.com/)**  
  Error tracking and APM focused on developer-friendly crash reporting and real user monitoring. Strong for mobile and web applications with clear, actionable reports.

- **[Bugsnag (SmartBear)](https://www.bugsnag.com/)**  
  Error monitoring platform with stability scores and release tracking. Popular for mobile apps. Acquired by SmartBear and increasingly integrated into their broader tooling suite.

- **[Rollbar](https://rollbar.com/)**  
  Real-time error tracking with AI-assisted grouping and debugging. Supports 20+ languages and frameworks. The open-source JavaScript SDK (`rollbar.js`) is maintained on GitHub.

- **[New Relic](https://newrelic.com/)**  
  Enterprise APM platform with distributed tracing, infrastructure monitoring, and browser monitoring. Offers a generous free tier (100GB/month) but costs escalate quickly at scale.

- **[Dynatrace](https://www.dynatrace.com/)**  
  AI-powered enterprise observability platform with automatic discovery, distributed tracing, and root cause analysis (Davis AI). Best for large enterprises with complex, hybrid infrastructure.

- **[AppDynamics (Cisco)](https://www.appdynamics.com/)**  
  Enterprise APM with business transaction monitoring and infrastructure visibility. Strong for traditional enterprise Java/.NET environments.

- **[LogRocket](https://logrocket.com/)**  
  Session replay and frontend monitoring platform. Captures user sessions with console logs, network activity, and Redux/Vuex state for debugging frontend issues.

- **[TrackJS](https://trackjs.com/)**  
  JavaScript error tracking focused on browser-side issues. Lightweight and developer-friendly, with detailed context around JavaScript exceptions.

## Open-Source GitHub Projects

- **[Sentry Self-Hosted](https://github.com/getsentry/sentry)**  
  The full Sentry platform, available for self-hosting. Source-available under the Functional Source License (FSL), converting to Apache 2.0 after two years . All product features—Issues, Performance, Dashboards—are implemented in the open component, not hidden behind a paywall . **Operationally heavy**: requires Kafka, ClickHouse, Snuba, and dozens of services with 16GB+ RAM . Best for organizations with dedicated platform teams that need the complete Sentry experience on their own infrastructure.

- **[GlitchTip](https://github.com/glitchtip/glitchtip-backend)**  
  Open-source, Sentry-SDK-compatible error tracking platform. Change the DSN and existing `@sentry/*` SDK code works immediately—no re-instrumentation needed . Runs in **4 containers on 512MB RAM** (vs. Sentry's 16GB+), with error tracking, uptime monitoring, and performance monitoring. Active development (v6 February 2026) with improved stack traces and performance monitoring . Best for small-to-mid teams that want Sentry compatibility without Sentry's operational weight.

- **[Bugsink](https://github.com/bugsink/bugsink)**  
  Open-source, self-hosted error tracking compatible with Sentry SDKs. Focuses on stacktrace-first debugging with local variables and context. Docker one-liner for evaluation. Claims 80% cheaper than Sentry at scale, with predictable event-based pricing and a European hosted option . Best for teams that want a lightweight, Sentry-compatible tracker with a clear path to managed hosting if needed.

- **[Highlight.io](https://github.com/highlight/highlight)**  
  Full-stack monitoring platform combining session replay, error monitoring, logs, and traces. Open source with a hobby self-hosted option (<10k sessions, <50k errors/month) and enterprise self-hosted tier . DOM-based session replay captures every interaction and console log, tightly correlated with errors. Best for frontend-heavy applications where user-reported bugs are the primary pain point.

- **[HyperDX](https://github.com/hyperdxio/hyperdx)**  
  Open-source observability platform built natively on ClickHouse. Unifies session replay, exceptions, logs, metrics, and traces in one UI with OpenTelemetry-native ingestion . Acquired by ClickHouse in March 2025, ensuring continued investment . Query directly on your existing ClickHouse cluster without schema changes. Best for teams already running ClickHouse or wanting session replay stitched to backend spans .

- **[SigNoz](https://github.com/SigNoz/signoz)**  
  OpenTelemetry-native APM with traces, metrics, and logs in a unified UI. Built on ClickHouse with broad query flexibility: visual builder, PromQL, and raw ClickHouse SQL escape hatch . Strong community momentum and no retention cap on self-hosted. Best for 10–50 engineer teams with one platform person who need flexible querying without vendor lock-in.

- **[Uptrace](https://github.com/uptrace/uptrace)**  
  OpenTelemetry-native APM focused on cost-efficiency. Uses ClickHouse and can process billions of spans on a single server . **Important caveat**: the free Community edition is hard-capped at 14 days retention; paid self-hosted tiers start around $39/month for 50GB/day . Best for high-volume, cost-sensitive teams that want flat-rate self-hosted pricing.

- **[Jaeger](https://github.com/jaegertracing/jaeger)**  
  CNCF-graduated distributed tracing platform, originally from Uber. Jaeger v2 is built on the OpenTelemetry Collector framework, aligning with modern OTLP pipelines . Mature, battle-tested, with flexible storage backends (Elasticsearch, Cassandra, Kafka). Best for organizations that need pure distributed tracing and already have logging/metrics covered elsewhere.

- **[Apache SkyWalking](https://github.com/apache/skywalking)**  
  Apache top-level project for application performance monitoring, especially strong for Java microservices. Provides distributed tracing, service mesh telemetry, metrics aggregation, and alerting. Best for large-scale Java environments with existing Apache ecosystem investments.

### Additional Strong Open-Source Options

- **OpenTelemetry** — Vendor-neutral observability framework for collecting traces, metrics, and logs. The standard instrumentation layer that most modern open-source APM tools build upon . Instrument once, switch backends without changing application code.
- **Grafana Tempo** — High-volume, minimal-dependency distributed tracing backend from Grafana Labs. Pairs naturally with Grafana for visualization and Loki for logs .
- **Pinpoint** — Java APM for large-scale distributed systems, with bytecode instrumentation and call-stack-level visibility. Best for Java-heavy organizations needing deep transaction tracing.
- **Frameworks for building custom systems**: Use **OpenTelemetry** as the instrumentation layer, **GlitchTip** or **Bugsink** for error tracking, **SigNoz** or **HyperDX** for unified APM, and **Jaeger** for pure tracing at scale. For frontend bugs, pair **Highlight.io** session replay with backend traces from your APM.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Self-hosted Sentry requires significant infrastructure (Kafka, ClickHouse, 16GB+ RAM); smaller teams should consider GlitchTip or Bugsink for Sentry compatibility with far lower operational overhead .
- Uptrace's free Community edition has a 14-day retention cap; verify licensing terms before assuming "free forever" self-hosting .

---

**Made for software engineers, SRE teams, platform engineers, and developers who believe production visibility should be transparent and controllable.**  
Let's make error tracking and APM more open, affordable, and observable.
