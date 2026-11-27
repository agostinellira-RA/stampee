# Project memory

## Product intent & audience

- Vite + React app with authentication, dashboard, card scanning, and customer management features.
- Likely a customer-facing or staff-facing tool involving card-based interactions (e.g., loyalty/membership cards).
- Backend relies on Supabase for auth and data (login, loading cards, saving customers).

## Brand personality & voice

- Not yet inferred.

## Visual design & UX direction

- Error surfaces may include banners or toasts (unconfirmed); exact UI for "service unavailable" still unclear.
- No visual design details inferred yet.

## Decisions, constraints & rationale

- Supabase chosen as backend service for auth and database.
- App expects Supabase connection via environment variables (`.env`); when absent, it falls back to a fake placeholder address, causing real database requests to fail.
- Missing `.env` configuration is a known cause of service-unavailable-style errors across login, card loading, and customer saving.

## Open questions & assumptions

- Where exactly "service is unavailable" appears (login, dashboard, card scan, etc.) — user hasn't confirmed.
- Exact form of the error (banner, blank screen, toast, browser error) — unconfirmed.
- Full product purpose and audience still to be clarified.
- No `.bolt/prompt` provided; no explicit global instructions exist yet.