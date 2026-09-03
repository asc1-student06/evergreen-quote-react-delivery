#Inject #2: Incident Routing Message

**Posted to**: #incidents
**From:** Kristen Marturano, Delivery Lead
**Time:** ~14:05 Wednesday

**What I observed**: CI on 'main' has been red for ~40 minutes, failing at the type-check step: src/premium.ts(10,3): Type 'string' is not assignable to type 'number', which points at the "adjust home rate" hotfix pushed ~40 min ago. Separately, support has a reproducible customer report of a $3,120/month quote for $180k home coverage, which looks far too high.

**What I'm asking, and of whom:** @[hotfix author/ on-call engineer], can you confirm whether the "adjust home rate" hotfix commit is what support's $3,120 case is hitting, or whether that's a second, separate issue? The timing and the shared "home rate" thread suggest they may be the same root cause, but I don't want to assume.

**Who owns the next step:** The hotfix author / on-call engineer owns diagnosing and correcting the rate change on 'main'; I'm not touching 'premium.ts' myself.

**Air cover:** I'll keep my data-feed and hook/context work parked on my branch and hold any merge to 'main' until it's green again. Happy to move our check-in if the team needs time to focus on the fix.