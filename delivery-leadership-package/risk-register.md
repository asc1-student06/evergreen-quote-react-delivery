# Risk Register



| # | Risk | Owner | Likelihood (L/M/H) | Impact (L/M/H) | Mitigation | Trigger to escalate |
|---|---|---|---|---|---|---|
| R1 | Flagged dev-time dependency (moderate severity) can't be upgraded until the platform team's window next week. | Platform team | M | L | Confirmed the flag is in a build-time tool, not in shipped customer code; document the decision to ship this week and track the upgrade. | If the flag is reclassified as high severity, or found to affect runtime/customer-facing code |
| R2 | Scope creep from injects (e.g., the ZIP-code field) pushes required Day 3-4 work past Thursday. | Kristen (Delivery Lead) | H | M | Protect the delivery goal; defer non-essential asks; log what's dropped on the board with a reason. | If a "must-have this week" ask can't fit without slipping the merge to main. |
| R3 | Sponsor rate values procude unbelieveable premiums after config. | Kristen (Delivery Lead) | M | M | Sanity-check auto/home/life in the browser after applying rates; confirm with sponsor if a number looks off. | If a premium is off by an order of magnitude and the sponsor can't confirm the value. |
| R4 | CI pipeline goes red on push (type-check or build fails), blocking the "green build" done criteria. | Kristen (Delivery Lead) | M | H | Run npm run type-check and npm run build locally before pushing; read CI logs as a leader, route fixes to the team. | If main is red and can't be made green before the Day 4 merge. |
| R5 | Data feed (quotes.json) fails to load, leaving customers with a broken panel. | Kristen (Delivery Lead) | L | M | The provided component handles loading/error/success states; verify all three on Day 3. | If the error state doesn't render and customers see a blank panel. |
| R6 | Merge conflicts or a minshandled PR when merging delivery/lead into main on Day 4. | Kristen (Delivery Lead) | L | M | Keep delivery/lead current; use squash-and-merge; self-review the diff before merging.| If a conflict can't be resolved cleanrly and risks losing assembled work. |

## How I'll use this register

_One short paragraph. When will you re-read it? Who else can see it? What's the cadence?_
