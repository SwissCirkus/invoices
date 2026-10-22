# Invoices

A single-page invoice and quote app (`index.html`). No server, no build step.

- Invoices and quotes typed straight onto the document, with a customer list.
- Withholding tax button (rate set in Settings), financial-year breaks, paid / partially paid tracking.
- PDFs of paid invoices are saved to a Google Drive folder called `Invoices`.
- Data lives in the browser and in your own Google Drive (`Invoices/invoice-data.json`). This repository holds only the app, no personal data.

Live at https://swisscirkus.github.io/invoices/

## Setup notes

The app uses a Google OAuth *Web application* client ID (set at the top of `index.html`). The page's address must be listed under **Authorized JavaScript origins** for that client (`https://swisscirkus.github.io`). The only permission requested is `drive.file`, which lets the app see just the files it created.

For local testing run `python -m http.server 8765` in this folder and add `http://localhost:8765` as an origin.
