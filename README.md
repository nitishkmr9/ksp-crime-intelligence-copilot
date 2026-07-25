# KSP Crime Intelligence Copilot

**AI-powered conversational crime intelligence platform for Karnataka State Police**, built as part of **GeoShield India's** submission to the Bharatiya Antariksh Hackathon (BAH) 2026.

## Problem

Police investigators spend significant time manually cross-referencing FIRs, case histories, and offender records across disconnected systems. Critical patterns — repeat offenders, emerging crime hotspots, case linkages — often go unnoticed simply because the underlying data isn't easy to query or visualize in real time.

## Solution

This copilot lets an investigator ask questions in **plain English or Kannada** and instantly get back structured, source-attributed answers — no SQL, no manual cross-referencing. It layers three views on top of the same case data:

- **Conversational Search** — Ask about a case, an accused, or a pattern; get contextual follow-up answers (e.g. "which of these are still open?") without repeating context. Every AI answer includes a "View source" trace showing which record it was grounded in, for auditability.
- **Offender Network Analysis** — Visualizes links between accused individuals across cases, automatically surfacing repeat-offender clusters.
- **Hotspot Intelligence** — A density heatmap of recent incidents alongside a 6-month case trend line, helping identify emerging crime concentrations before they escalate.

## Why it matters

- **Bilingual by design** — built for real Karnataka field usage, not just English-speaking HQ staff
- **Explainable AI** — every answer is traceable to a source record, addressing a key trust barrier for law-enforcement AI tools
- **Pattern surfacing, not just retrieval** — the network and hotspot views turn scattered case data into actionable intelligence

## Tech stack

- React 18 + Vite
- Tailwind CSS
- Recharts (trend visualization)
- Lucide React (icons)

## Run locally

Requires [Node.js](https://nodejs.org) (v18+).

```bash
npm install
npm run dev
