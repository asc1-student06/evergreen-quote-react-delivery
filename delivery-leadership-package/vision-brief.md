# Evergreen Quote: Vision Brief

> Copy this file into `delivery-leadership-package/vision-brief.md` in your repo and fill it in. Target length: 1 page (~300 words). Write for a Liberty Mutual VP who has 90 seconds.

## Product
**Name:** Kristen Marturano
**Delivery week:** 2026-08-31
**Delivery Lead:** Kristen Marturano
**Engineering team (represented by):** (https://github.com/asc1-student06/evergreen-quote-react-delivery)
**GitHub Project board:** https://github.com/users/asc1-student06/projects/5/views/1

## Who is the customer?
Prospective insurance customers who want a fast, self-serve estimate of their monthly premium before talking to an agent. They value speed, clarity, and a sense that the number they see is trustworthy.

## What pain does Evergreen Quote remove?
Today, getting a premium estimate means calling an agent or filling out a long form and waiting. Evergreen Quote removes that friction: the customer picks a coverage type, enters a few details, and sees an instant estimate that updates as they adjust the inputs - no phone call, no waiting.

## What does "good" look like at end of the week?
A working, assembled Evergreen Quote React app that:
- Shows a live premium estimate that recalculates as the customer types 
- Has the correct product title and the sponsor's approved rates configured.
- Passes the TypeScript type-check (contracts hold- no bad data reaches a customer).
- Loads recent quotes from a data feed with proper loading/ error/ susccess states.
- Uses the provided custom hook + context provider, with "Save this quote" working.
- Is merged to 'main' via a reviewed PR with a green CI run and a passing production build.

## What are we explicitly NOT doing this week?
- Writing application code from scratch (this is assembly, not authoring).
- Building a backend, database, user accounts, or payment/policy binding.
- Refactoring the engineering team's starter project.
- Adding in coverage types or features beyond what the kit provides (unless a sponsor inject asks for it). 

## How will we know if it worked?
We'll know this week succeeded if, by Thursday EOD, all of the following are true:
- **It runs:** the app loads and a customer can get a live premium estimate that updates as they change inputs.
- **The contracts hold:** 'npm run type-check' passes with no errors, and the production build ('npm run build') completes successfully.
- **The data feed works:** recent quotes load from the feed, and the customer always sees one of three states - loading, error, or the actual data (never a blank panel). 
- **Save works**: clicking "Save this quote" adds it to the top of the list.
- **It's shipped properly:** the work is merged to 'main' through a reviewed PR with a **green CI run** - not pushed straight to main. 
- **The board tells the story:** every issue is in Done with its done-criteria met, so a stranger could look at the board and see what was delivered.
