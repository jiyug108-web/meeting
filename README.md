# Visitor Appointment Submit Page

A lightweight static page to submit the visitor appointment request.

## Implemented Rules

- `v_name` and `v_plateNumber` are fixed to default values and rendered as read-only.
- `v_timeStr` defaults to today's `08:00:00`.
- `v_lvTimeStr` defaults to today's `23:56:00`.
- Except start/end time values, all payload fields remain unchanged from the provided parameter set.
- Submission logs and status are shown on the page.

## Files

- `day.html`: page UI and log area
- `payload-utils.js`: fixed payload + time and endpoint helpers
- `index.js`: form init, validation, request submit, logs
- `test.js`: minimal Node test harness

## Quick Start

```bash
npm test
npm start
```

Then open:

- `http://localhost:8080/day.html`

## Notes

- The request is sent directly from browser to the provided HTTPS endpoint.
- If the target service blocks CORS or has certificate/network restrictions, the page will show failure logs with details.

