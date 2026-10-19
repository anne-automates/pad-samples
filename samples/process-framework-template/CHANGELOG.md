# Changelog - Process framework template

## 1.0.0 - 2026-10-19

- First public version: a desktop flow template to start every process from. `Main` and 11 local functions in numbered, coloured regions, a note on every action, condition, loop and region (525 notes), settings per environment, business and system exceptions with retries, log, run report, a JSON summary for the cloud flow and a `Tests` subflow of 24 cases. With it, the invoice reminders example made from the template.
- After that run, only comments changed: the three header lines of the local functions are written in the form of the lab (`# local subflow:`, `# inputs:`, `# outputs:`). No action changed, no new run needed.
- Tested on Power Automate Desktop 2.73.155 on 2026-10-19: `Tests` 24 PASS, 0 FAIL in 151 s; `Main` on the 6 demo items COMPLETED in 148 s (2 successes, 3 business exceptions, 1 system exception after 3 attempts with 3 screenshots), every file of the run checked. On 2026-10-18 the same flow was saved as a template, published and used with *New › Flow from template*, and the invoice reminders example was made from it (`Tests` 24 PASS, `Main` COMPLETED with 2 Outlook drafts and nothing sent).
