# Global Cybersecurity Intelligence Center (GCIC)

GCIC is a self-contained, browser-based cybersecurity intelligence dashboard. It collects publicly available security information, normalizes and correlates records, and presents the results in an operational dashboard.

## What It Does

- Collects vulnerability data from NVD and the CISA Known Exploited Vulnerabilities catalog.
- Reads supported public security advisory and news feeds.
- Correlates duplicate records, especially records that share a CVE identifier.
- Displays live intelligence, incidents, vulnerabilities, advisories, source health, a timeline, and verified geographic data.
- Provides search and filters for category, severity, source, date, and region.
- Creates rule-based alerts for critical vulnerabilities, CISA KEV entries, zero-days, and selected vendors or products.
- Stores collected intelligence locally in the browser with IndexedDB.
- Exports filtered or retained data as CSV or JSON.
- Continues showing previously collected records when sources are unavailable.

## Run Locally

No build process or package installation is required. Open `index.html` in a modern browser, or serve the folder with a local static web server:

```sh
python3 -m http.server 8000
```

Then open `http://localhost:8000`.

## Data and Privacy

GCIC runs entirely in the browser. Collected records and settings remain in that browser's local storage, and no API credentials are embedded in the application.

Some external feeds may be unavailable because of browser CORS policies, authentication requirements, API rate limits, or source outages. Disabled sources are listed in the dashboard with the reason they are not configured. A backend proxy would be required for authenticated or browser-restricted feeds.

## Disclaimer

This project is intended for security awareness and research. Source availability, publication delays, and source accuracy affect coverage. The absence of an event in the dashboard does not indicate the absence of a threat or attack.