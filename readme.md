# Capacity-Constrained Newsvendor RAG Tutor

Open `capacity_newsvendor_rag_tutor.html` in a browser. No server is required.

This standalone web app adapts the capacitated newsvendor lecture into a tutor-led class activity.

## Main features

- A single RAG-style tutor workspace with no personas.
- A separate complete problem brief window that states the case and questions to be answered without revealing the learning objectives or detailed solution steps.
- Scenario controls for production capacity and quantities for the Autumn and Leaves parka styles.
- Separate live windows for product data, demand graph, expected-profit frontier, expected-profit map, marginal-contribution curves, rule/benchmark comparison, critical-fractile table, and symbol glossary.
- Open information windows automatically refresh when students change capacity or quantities, reveal the ordinary benchmark, or reveal the optimizer benchmark.
- Printable learning sheet for browser Print / Save as PDF at the end of the session.
- Local tutor knowledge base with 124 concept/symbol cards and 14894 generated student-question examples.

## Local/privacy behavior

The app is a static file and does not call external APIs, CDNs, analytics, `fetch()`, or `XMLHttpRequest()`.

## Teaching design

The main student plan gives high-level guidance only. It does not reveal the exact computations needed to solve the assignment. Formula and optimizer details are available in separate windows and through the tutor when students ask targeted questions or reveal the benchmark.
