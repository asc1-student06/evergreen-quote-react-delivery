# Copilot-Assisted Assembly Critique

**Task:** I asked Copilot to add two realistic rows to public/quotes.json matching the existing shape.

**What it got right:** The structure was exactly current; right fields, right types, sequential IDs, plausible-looking values. npm run type-check passed cleanly, confirming the rows honor the Quote contract.

**What it got wrong:** The premium values it invented (129.6 for auto, 336.0 for life) don't match our actual pricing formula in premiums.ts, which would produce different numbers. The values are well formed but not correct.

**Would I ship it as-is?** No. The type system confirms the data is well formed, but cannot confirm the numbers are right, exactly the gap behind this week's incident, where a validly-typed but wrong value reached a customer. I'd keep the rows only after recomputing each premium against our real rate logic.