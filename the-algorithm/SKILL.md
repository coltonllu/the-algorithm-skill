---
name: the-algorithm
description: Run a system, process, or workflow through Jon McNeill's five-step Algorithm — question every requirement, delete every possible step, simplify and optimize, accelerate cycle time, automate last — and deliver the result as a Claude Doc. Use this whenever the user wants to redesign, rebuild, fix, streamline, speed up, or automate any process or workflow; whenever they say something is slow, bloated, manual, has too many steps, too many approvals, or "we've always done it this way"; whenever they are about to automate something or build an AI agent for a task; and whenever they invoke "the algorithm" by name. Use it even when the user only asks for the last step ("can you automate this?") — the whole point of the framework is that automation is step five, not step one, so the skill runs the earlier steps first.
---

# The Algorithm

The operating framework Jon McNeill codified while President of Tesla (2015–2018) and published in *The Algorithm: The Hypergrowth Formula That Transformed Tesla, Lululemon, General Motors, and SpaceX* (Penguin, March 2026).

Five steps, applied in strict order:

1. **Question every requirement**
2. **Delete every possible step**
3. **Simplify and optimize**
4. **Accelerate cycle time**
5. **Automate — last**

**The order is the entire point.** Skipping or reordering is the most common failure. You cannot accelerate a process you haven't deleted waste from. You cannot automate a process you haven't simplified. Automating a bad process just produces bad outcomes faster and at greater cost.

Read `references/five-steps.md` before running a session — it holds the named play, the diagnostic thresholds, and the failure modes for each step. Read `references/evidence.md` when you need case studies, verified quotes, or the honest limits of the framework.

---

## How to run a session

### Phase 1 — Scope it (ask, don't assume)

Ask **three to five questions** before producing anything. Use `ask_user_input_v0` if available — it is faster for the user than typing. Otherwise ask in prose, grouped into one message.

Ask only what you can't infer from the conversation. The questions that earn their place:

1. **What's the process, and where does it start and end?** Vague scope produces vague output. Pin the boundaries.
2. **What triggered this?** Symptom tells you which step will do the heavy lifting. "Takes three weeks" → step 4. "Nobody knows why we do this" → step 1. "We're about to buy a tool for it" → step 5 gate.
3. **What does the customer actually pay for?** This is the deletion filter for step 2. If the user can't answer, that's a finding, not a blocker.
4. **What are the current numbers?** Elapsed time, touch time, step count, approvals, volume per week. Rough is fine. Refusing to guess is worse than guessing.
5. **What's your authority to delete?** Can the user kill a step themselves, or do they need someone's sign-off? This is the framework's real constraint and it changes the recommendations — see "The permission problem" below.

Then say what you're about to do and do it. Don't ask a second round of questions.

### Phase 2 — Run the five steps

Work them in order. For each step, apply the named play from `references/five-steps.md` to the user's actual process — not a generic description of the step.

Two rules that hold throughout:

- **Be concrete or say nothing.** "Consider streamlining approvals" is worthless. "Kill the second sign-off; it has no named owner and hasn't been validated since 2023" is the product.
- **Count things.** Steps before and after. Elapsed vs. touch time. Clicks. Signatures. Days. If the user gave rough numbers, use them and mark them as estimates. A process improvement with no number attached can't be checked later.

### Phase 3 — Deliver as a Claude Doc

The output is a Claude Doc, not a chat reply.

If no docs instructions are loaded in context, call the docs connector's `guide` with `topic.instructions` first. Create the doc with headings only, then fill it in.

Doc structure:

| Section | Contents |
|---|---|
| **The system** | Scope, boundaries, owner, why now |
| **Baseline** | Step count, elapsed vs. touch time, approvals, current cost. Mark estimates as estimates. |
| **1 · Requirements** | The autopsy table: requirement, owner, last validated, verdict (physics / safety / law / convention) |
| **2 · Deletions** | Every step, color-coded. What dies immediately, what gets a two-week pilot, what survives and why |
| **3 · The simplified process** | The surviving steps, redesigned. Side-by-side with the old one |
| **4 · Cycle time** | Target elapsed time, the constraints in the way, ranked |
| **5 · Automation gate** | What now qualifies to be automated, what doesn't, and what to benchmark against |
| **Monday** | The first three things to do this week, with owners |
| **Where this doesn't apply** | Honest limits for this specific process — see "Guardrails" |

Keep the doc tight. A reader should be able to find the deletions in ten seconds.

---

## Voice

The user wants this to feel like talking to McNeill. That means his register, grounded in what he actually says and does — not an impersonation.

**What his register is:**

- Operator, not consultant. He was in the room during Tesla's near-death, and he talks about processes he personally tore apart.
- Blunt about waste, never about people. The enemy is the inherited rule, not the person following it.
- Reasons from the customer outward. "Does the customer pay for this?" is his recurring test.
- Reaches for a specific number or a specific story rather than a principle. 64 clicks. Twelve pages. Four days versus fifteen.
- Democratizing, not heroic. He is explicit that the point is that ordinary people can run this — that you don't need to be Elon Musk to do it.

**What to avoid:**

- **Never invent quotes and attribute them to McNeill or Musk.** Verified quotes are in `references/evidence.md`, with sources. Use those or paraphrase openly. A fabricated quote in a doc the user will circulate is a real harm.
- Don't write in first person as McNeill. The skill applies his framework; it doesn't play him.
- Don't import the hustle mythology — 100-hour weeks, proximity to death, brutality as method. It isn't the framework, and reviewers of the book flag it as the weakest part. The five steps work in an eight-person team without any of it.

---

## Guardrails

**Physics, safety, law are real.** Step 1 tests requirements against exactly three criteria. A rule that traces to any of them stays. In regulated work — medical, financial, legal, aviation, employment, anything with a governing body — the skill flags the requirement for the user to verify with someone qualified rather than pronouncing it a convention. McNeill's loan-document story worked because lawyers confirmed it. Recommend that confirmation; don't substitute for it.

**The permission problem.** The framework's sharpest critique is that radical deletion requires authority to delete, which most people don't have. If the user can't unilaterally kill a step, the output changes shape: it becomes a case to bring to whoever can, with the evidence assembled. Say so plainly rather than producing recommendations the user can't act on.

**Deletion has a downside the book underplays.** Every case study in the book is a survivor with deep capital reserves. Steps sometimes encode institutional knowledge, and the book examines no failures. So: propose a two-week pilot before permanent deletion of anything load-bearing, and name what would break if the deletion is wrong.

**Don't force the framework onto what isn't a process.** A hiring decision, a pricing question, a strategy call — these aren't workflows. Say so and help with the actual question instead.

**Scale down honestly.** The published case studies are Tesla, SpaceX, GM, Lululemon. Most processes the user brings will be two orders of magnitude smaller. Translate; don't inflate.

---

## Prior art worth naming

Step 4 is Goldratt's Theory of Constraints (*The Goal*, 1984) under a different name, and the book doesn't cite it. Goldratt's finding that optimizing a non-bottleneck actively harms throughput is a real refinement the Algorithm's framing misses — use it. Steps 2 and 3 overlap heavily with lean and the Toyota Production System, which McNeill positions himself against as "incremental." That characterization undersells TPS kaizen events. When lean vocabulary would serve the user better, use it.
