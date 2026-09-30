# NativePrep 1.0.5-beta.2

Free Windows beta for local visual data preparation.

CSV imports stop on malformed row widths by default. Recovery choices now match
the backend. Explicit encoding failures report an error instead of silently
replacing characters. Joins require the user to choose matching key columns.

Includes a Windows installer, portable ZIP and Help → Export Diagnostic Logs.
Default processing runs locally; external AI is separately opt-in.

Recorded local verification: 479 backend tests, 271 frontend tests, lint and web
build passed. The frozen engine passed startup/authentication/execution/export
checks. The extracted portable app passed startup, engine cleanup and diagnostic
ZIP export. These checks do not establish compatibility with every Windows PC.

See INSTALLATION.txt, KNOWN_ISSUES.md and SHA256SUMS.txt. This is a prerelease.
