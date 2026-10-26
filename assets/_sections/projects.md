---
title: Projects
slug: projects
order: 2
heading: Projects
class: projects
---

Small tools I build and run myself, mostly for everyday document work in a small business. They run on my homelab server (Docker, nginx, Traefik) and are deployed automatically from my self-hosted Forgejo.

**jink**, **chop** and **numi** belong to a small toolbox called [Doc](https://doc.sunshard.de). Each tool is a single HTML file with no build step and no server-side processing: documents never leave the browser.
{: .projects-intro}

<ul class="project-cards">

  <li class="project-card">
    <h3 class="project-card-title"><a href="https://jink.sunshard.de">jink</a></h3>
    <p class="project-card-sub">Redact documents locally in the browser</p>
    <p>Removes personal data from PDF, Word, Excel, XML (including CAMT bank statements), text files and images. Values are found by pattern (email, IBAN, phone, address, tax ID, amounts), by custom terms, or marked by hand.</p>
    <p>PDF pages are rebuilt as images so redacted values can't be copied or recovered from the file. In Office files it also masks comments, tracked deletions and document metadata.</p>
    <ul class="project-tags">
      <li>JavaScript</li><li>PDF.js</li><li>pdf-lib</li><li>Tesseract.js OCR</li><li>CSP / SRI</li><li>Playwright tests</li>
    </ul>
  </li>

  <li class="project-card">
    <h3 class="project-card-title"><a href="https://chop.sunshard.de">chop</a></h3>
    <p class="project-card-sub">Split a scanned stack of mail into single documents</p>
    <p>Takes one long scanned PDF, detects where each letter ends (page numbers, salutation, address block, invoice number, sender) and names each document <code>Date_Sender_Type</code>. Results come back as a ZIP.</p>
    <p>Uncertain split points are highlighted for review instead of guessed silently. Includes parallel OCR, blank-page and upside-down detection, and an optional searchable text layer.</p>
    <ul class="project-tags">
      <li>JavaScript</li><li>Tesseract.js OCR</li><li>Web Workers</li><li>pdf-lib</li><li>Playwright tests</li>
    </ul>
  </li>

  <li class="project-card">
    <h3 class="project-card-title"><a href="https://numi.sunshard.de">numi</a></h3>
    <p class="project-card-sub">Natural-language calculator in a notepad layout</p>
    <p>Each line is evaluated live and can reference earlier lines, in the style of Soulver. Handles units, currencies (daily exchange rates with offline fallback), dates and time zones, and validates IBANs and credit card numbers.</p>
    <p>Installable as an offline-capable web app; sheets are stored locally in the browser.</p>
    <ul class="project-tags">
      <li>JavaScript</li><li>PWA</li><li>Service Worker</li><li>Node tests</li>
    </ul>
  </li>

  <li class="project-card">
    <h3 class="project-card-title">trends</h3>
    <p class="project-card-sub">Google Trends dashboard for Germany and the US</p>
    <p>A small Python service in Docker collects the current trending searches every 30 minutes, with a request budget, back-off on rate limits and an RSS fallback. A static page shows the trends with 24-hour curves, a 7-day history of dropped topics and a sports filter.</p>
    <ul class="project-tags">
      <li>Python</li><li>Docker</li><li>supercronic</li><li>nginx</li><li>Traefik</li>
    </ul>
  </li>

</ul>

## Also

- **[autofy](https://github.com/raiden-e/autofy)**: Python scripts that automate my Spotify playlists, such as a weekly lo-fi playlist and a playlist archive, run on a schedule via GitHub Actions.
