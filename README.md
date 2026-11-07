# Vacti

**Vacti is an AI-driven autonomous penetration-testing platform.** It runs real security
assessments the way a skilled human tester would — but continuously, consistently, and with every
finding proven before it is reported. It is built for security teams, consultancies and
organisations that need more testing than their people can deliver by hand, and who cannot afford
to spend analyst time sorting a report full of false positives.

This repository holds the source of the public product site at **[vacti.org](https://vacti.org)**.

## What Vacti does

- **Autonomous assessment.** Point it at an authorised target and it does the work: discovery,
  enumeration, hypothesis and exploitation — across web, mobile, network and cloud surfaces.
- **Proof, not possibility.** A finding is only reported once it has been demonstrated against the
  live target. No "may be vulnerable" entries.
- **One view of your risk.** Findings, exposure and breach intelligence roll into a single risk
  score, so a board or a client gets one number instead of five dashboards.
- **Built for professional delivery.** Reports are evidence-grade and ready to hand to a client or
  an auditor.

## Where it runs

Vacti is **self-hosted**. You run the control plane on infrastructure you control, and engines run
on appliances you also control. Nothing about your targets or your findings leaves your
environment. Engines reach out to your control plane; they never open an inbound port.

You can try it as a **managed engagement** with our team, or deploy it as a **partnership** inside
your own delivery practice.

## This repository

The site is a single static page with no build step and no runtime dependency.

```text
index.html                     the whole page
styles.css                     the design system (white + blue)
assets/                        logo, icon, and supporting imagery
.github/workflows/deploy.yml   publishes the site on every push to main
```

To preview locally, serve the directory with any static file server (`python3 -m http.server 8080`)
and open <http://localhost:8080>.

## Documentation

Full product documentation — installation, administration, the user guide, and the architecture
overview — is at **[docs.vacti.org](https://docs.vacti.org)**.

## Licence

MIT. See [LICENSE](LICENSE).

Vacti is for authorised security testing only. Only ever test systems you have written permission
to test.
