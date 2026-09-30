# NativePrep 1.0.5-beta.3

Free Windows beta for local visual data preparation.

This beta adds bounded DuckDB query memory and temporary disk spill, a
byte-bounded in-memory table cache, and clearer memory-failure advice.
Temporary execution directories are removed on normal completion and
cancellation. These controls reduce resource pressure; they do not make every
operation larger-than-memory or guarantee that every file within the import cap
will succeed.

Includes a Windows installer, portable ZIP and Help → Export Diagnostic Logs.
Default processing runs locally; external AI is separately opt-in.

The frozen engine passed startup, authentication, desktop CORS and all five
export-format checks. Deterministic CSV lookup-join/group/export checks passed
at 10k, 100k, 1m and 3m rows; a 10k-row XLSX check also passed. Every exported
group total matched, previews stayed bounded, and malformed input was rejected
with successful subsequent execution. The 3m-row CSV was about 59 MB: these
local checks are not a promise of arbitrary large-file support or compatibility
with every Windows PC.

See INSTALLATION.txt, KNOWN_ISSUES.md and SHA256SUMS.txt. This is a prerelease.

Release verification: 488 backend tests and 273 frontend tests passed; lint,
desktop static export and website static export passed. The extracted portable
app passed startup, owned-engine cleanup and diagnostic ZIP export. An initial
backend run alongside packaging/benchmarks had one integration failure; that
test passed alone and the subsequent full suite passed all 488 tests.
