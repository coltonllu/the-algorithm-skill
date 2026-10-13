# The Five Steps in Depth

Each step below has: the core question, the named play, the diagnostic thresholds that tell you the step applies, and the failure mode.

**Contents**
1. [Question Every Requirement](#1--question-every-requirement)
2. [Delete Every Possible Step](#2--delete-every-possible-step)
3. [Simplify and Optimize](#3--simplify-and-optimize)
4. [Accelerate Cycle Time](#4--accelerate-cycle-time)
5. [Automate — Last](#5--automate--last)
6. [The metric underneath all five](#the-metric-underneath-all-five)
7. [Goal-setting: the multiplier on the whole framework](#goal-setting-the-multiplier-on-the-whole-framework)

---

## 1 · Question Every Requirement

### The core question

Every rule governing this process gets tested against exactly three criteria:

- Is it a requirement of **physics**?
- Is it a requirement of **safety**?
- Is it a requirement of **law**?

If the answer isn't yes to one of those, it is a candidate for deletion. Not a requirement — a convention, a custom, a recommendation that calcified. McNeill's framing: when constrained by rules, investigate; what looks like a requirement usually turns out to be a convention nobody has revisited.

### Two structural rules

**Every requirement has a name.** A requirement must trace to a *person*, not to a department, not to "compliance," not to "legal." If it can only be attributed to an institution, nobody can be argued with, and the rule becomes unchallengeable by design. Push until there is a name.

**Requirements are debt, not safety.** The instinct in most organizations is that adding a requirement de-risks. It doesn't — it adds carrying cost forever, paid by everyone downstream. Requirements documents grow and never shrink. That asymmetry is the disease.

### The play: Requirement Autopsy

A two-hour session per process. List every rule governing it. For each, demand two things:

1. **Who owns this?** (a person)
2. **When was it last validated?** (a date)

No owner, or no validation inside 12 months → reclassify as convention, mark for deletion review. Assign each surviving item a single owner who must **defend it or kill it within 14 days.**

Expect to surface 30–80 items on a real process. Expect to delete at least half.

### Where to look first

Look for the places nobody has interrogated in years. McNeill's point is that people who have been inside a business a long time stop seeing the base assumptions at all. The oldest untouched rule is usually the most expensive.

### Diagnostic thresholds

- Teams cite "compliance" or "we've always done it this way" to block a change
- Requirements documents that have only ever grown
- New hires accept inherited rules without asking why
- Nobody present can name who created a given rule

### Failure mode

Accepting the first answer. "Legal requires it" is the beginning of the inquiry, not the end. In the loan-document case, the lawyers came back and said *none* of the twelve pages were legally required — and that existing case law already protected the company's right to repossess without any of it. Every paragraph had been inserted by well-meaning lawyers protecting the company from imagined risk.

---

## 2 · Delete Every Possible Step

### The core question

**Does the customer pay for this step?**

If not, it's a deletion candidate. If it can't be deleted, can it be made invisible to the customer?

Musk's corollary, which McNeill carries forward: if you aren't occasionally deleting a step you later have to add back, you aren't deleting enough. A deletion process with a zero error rate was too timid.

### The play: Color-coded process map

Physical wall, sticky notes, one step per note, end to end. Then color:

| Color | Meaning | Action |
|---|---|---|
| **Green** | Customer directly pays for this | Keep — this is the actual work |
| **Yellow** | Internal overhead | Document what breaks without it, then run a two-week pilot deleting it |
| **Red** | Pure latency — waiting, queuing, batching, sitting in a tray | Eliminate now. Red has no defense. |

Red steps don't get a pilot. They get removed this week.

### The subtler version: delete the step by deleting its reason

The strongest deletions come from step 1, not step 2. Tesla's mobile service came from asking whether a repair requires a building at all — the question dissolved an entire category of steps rather than trimming them. Tesla's giant single-piece castings replaced hundreds of welded parts (the idea reportedly came from looking at a Matchbox toy car). Inline quality inspection was deleted by making each worker responsible for passing only finished work downstream, and tracking passback rate instead — the inspector step vanished rather than being optimized.

### Diagnostic thresholds

- Customer-facing process exceeds 10 steps
- Approval chains needing 3+ signatures
- Onboarding or purchase flows over 20 clicks
- Any step where work sits waiting for a different person to look at it

### Failure mode

Optimizing something that shouldn't exist. This is the most expensive mistake available, because the work looks productive. Deletion is also not a one-time cleanup — it's a discipline that runs continuously, because steps grow back.

---

## 3 · Simplify and Optimize

### The core question

Now that only necessary steps remain — what is the simplest possible version of each?

This step comes *third* for a reason. Refining a step you should have deleted is wasted effort, and it's worse than wasted because it creates sunk-cost attachment to the step.

### The play: collapse the artifact, then the motion

**Collapse the artifact.** Replace multi-page SOPs with a single directive that captures the intent. Tesla replaced a month-long new-hire training program with one line: be so great they'll talk about you at dinner. The twelve-page loan document became a single paragraph covering rate, term, and monthly payment. If the team can't explain the core process in 60 seconds, it isn't simple yet.

**Economy of movement.** Borrowed from the kitchen at Alinea: every tool, template, and resource pre-positioned so there is no wasted motion. Time each surviving step. Set a 50% reduction target. Run daily standups for two weeks while iterating.

Tesla's delivery prep went from 5–6 hours to 4 minutes through this kind of work.

### Diagnostic thresholds

- Frontline training exceeds two weeks
- SOPs run over 10 pages
- Nobody can explain the process in 60 seconds
- Handoff errors account for more than 15% of defects

### Failure mode

Treating simplification as documentation. Rewriting the manual more clearly is not simplifying the process. The test is whether the *work* got shorter, not whether the description did.

---

## 4 · Accelerate Cycle Time

### The core question

What is the total elapsed time from start to finish — and how much of that is actual work?

### The play: elapsed vs. touch time

Measure both on your three highest-volume processes.

- **Elapsed time** — wall-clock, start to finish
- **Touch time** — hours of actual work inside it

**A ratio above 5:1 means you have a cycle-time problem, not a capacity problem.** The gap is pure latency: approvals, handoffs, batching, waiting. Hiring more people does nothing for latency. This distinction is the most useful single diagnostic in the framework, because organizations reliably misdiagnose latency as understaffing.

McNeill's illustration: auto body repair runs about 18 days elapsed against 5–6 hours of actual work.

### The mechanism: concurrency and co-location

Sequential cross-functional work is where elapsed time goes to die. The interventions:

- Cross-functional owners in a shared war room
- Daily 15-minute standups
- Cut the deadline by 50% as a forcing function, then document every constraint that surfaces and attack them in priority order

Results McNeill cites: GM's Hummer EV from four years to 19 months. Lululemon's Olympic kit from 18 months to four.

### Why speed is a diagnostic, not just a goal

Speed reveals faults. If something can move fast, it has to be simple and it has to be good — which is why McNeill argues the good/fast/cheap trilemma is false and you can have all three. But this only holds **after** steps 1–3. Accelerating a flawed process accelerates failure and multiplies cost.

Speed is also cultural, not procedural: better to test something unfinished quickly than to ship something supposedly perfect slowly.

### Diagnostic thresholds

- Elapsed time exceeds 5x touch time
- Teams work sequentially across functions rather than concurrently
- Status visibility requires manual spreadsheet reconciliation

### Failure mode

Accelerating everything. This is where the framework is weaker than Goldratt's Theory of Constraints, which it restates without citation. Goldratt's finding: optimizing a non-bottleneck actively harms throughput. Find the constraint, fix the constraint, then re-find it. Don't spread speed evenly.

### The remote caveat

The acceleration mechanics assume co-location — the Lululemon sprint worked specifically because cross-functional managers were in one room. Steps 1–3 run fine asynchronously. Step 4 needs adaptation for distributed teams, and the book doesn't provide it.

---

## 5 · Automate — Last

### The core question

Has this process been through steps 1–4? If not, there is nothing here to automate yet.

### The principle

Automation is the reward for finishing the first four steps, not a substitute for them. Automating a broken process scales the dysfunction — you get to the wrong answer faster, more expensively, and now it's encoded in software where it's harder to remove.

McNeill's own line: automating a bad process just speeds up the time to a bad outcome.

### The founding scar

Tesla designed the Model 3 line fully automated, digitally, before a single brick was laid. Machines were placed six inches apart — no room for a human to reach in and calibrate anything. It didn't work. The company nearly went bankrupt because the predicted cash flow never arrived.

The rescue was the opposite of automation: dismantle it, build a tent outside the factory, and make cars by hand. A hundred a week, then five hundred, until they understood the process well enough to build an automated line that reflected reality. The postmortem produced the rule: **perfect the process before you automate it.**

### The pattern elsewhere

- **DoorDash** launched with a PDF and a phone number, mapping the workflow manually before writing code
- **Amazon** took book orders on a web page with no fulfillment capability, then ran to a bookstore, bought the book, and boxed it — learning the business by hand first

### The play: the automation gate

No automation approved without a completed steps 1–4 audit showing before and after state.

Two rules that follow:

1. **Benchmark against the simplified manual process, not the original.** Comparing automation to the old bloated version inflates the ROI of automating waste.
2. **Kill any automation initiative where the simplified manual process already hits the target cycle time.** Often it does. That's a win, not a failure.

### Diagnostic thresholds

- A team is evaluating AI or RPA for a process not redesigned in over two years
- Automation projects routinely overrun budget by 50%+ or miss ROI
- "We'll fix it in the code" is a common refrain

### Why this matters more now

This step is the framework's most timely insight. AI makes it trivially easy to automate a bad process. The advantage now belongs to whoever can tell what shouldn't exist in the first place. Any request that starts "can you build an agent that…" or "can we automate…" is a step-5 request arriving before steps 1–4 have been run.

---

## The metric underneath all five

**Cash velocity** — the speed from investment to revenue recognition. McNeill treats this as the highest-level competitive metric, above output volume or margin.

His comparison: Toyota converts raw aluminum into a finished car in about four days; Tesla took roughly fifteen. That gap means Toyota needs roughly 2.5x less working capital to run the same business. Processes that compress the cash conversion cycle outperform on capital efficiency regardless of margin.

For non-manufacturing work, the equivalent question is: how long between spending effort and the effort producing something you get paid for? Then compress that.

---

## Goal-setting: the multiplier on the whole framework

The five steps sit inside a goal-setting posture that determines how hard they get applied.

**Set targets at 50–100% improvement, not 5–10%.** The reasoning is mechanical, not motivational: a modest goal invites local fixes — people polish edges. An order-of-magnitude goal makes local fixes obviously insufficient, which forces the team to question whether the process, the interface, the staffing model, and the product were designed wrong to begin with. That question is step 1.

McNeill was told to improve digital car sales 20x at a time when selling an expensive car online sounded absurd. The clicks went from 64 to 12 in ten months.

His defense of the approach: hitting 50–60% of an extreme goal still beats what conventional goal-setting produces, and the attempt itself compounds organizational learning.

**The honest counterweight:** this is where survivorship bias lives. Tesla survived; nobody writes books about the companies that chased unrealistic goals and died. Use extreme targets as a thinking tool to break incrementalism — not as a promise about outcomes, and not in contexts where missing the target is fatal.

---

## Two adjacent habits worth carrying

**Mystery-shop your own process.** Walk the customer's path yourself, step by step. Refuse to treat internal dashboards as reality when customers are visibly stuck. McNeill's own entry point at Tesla was noticing how long it took to call an interested buyer back — a bottleneck most companies would have buried inside a report.

**Follow Me Home.** Watch someone actually use the thing in the wild rather than asking them about it. Original process insight starts as an annoyance or a delay somebody else stopped noticing.
