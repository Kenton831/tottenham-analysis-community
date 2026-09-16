# Efficiency and delegation

The rule is to save repeated steps, not content. Cutting source verification, sections, player detail, voiceover length, or charts to save tokens is cutting corners, not efficiency. When an efficiency rule conflicts with the quality bar, redesign the work; never delete information to make it cheaper.

## One research pass, many outputs

Verify each fact once, keep the source or raw payload in a file, then write the article, the voiceover, the short vertical cut and the chart captions from that same verified fact base.

## Do not re-derive what is already on disk

- Check the existing data snapshot before opening a new source.
- Read selectively: search for the section or statistic you need instead of loading whole documents, and read a reference file only when its output mode applies.
- Reuse the previous match's chart code and adapt it to the new match; patch a file for a small edit instead of regenerating it.
- Run independent lookups in parallel rather than one after another.

## Keep context small at the source

- Long tool or API output belongs in a file; report only what changes the analysis.
- Every file has one canonical location. A chat reply carries the result and the paths, not a copy of content that already exists on disk, unless the user asks to read it in chat.
- Each deliverable stands alone, and inside one deliverable the same conclusion is not repeated under several headings.

## Phase checkpoints

Context is re-sent with every request, so a session that has grown very long makes every remaining step expensive.

- At each phase boundary - record verified, then analysis, then writing, then charts - make sure the snapshot, the event list and a project context file hold the complete state, then continue in a fresh session that reads those files.
- Never let the only copy of a fact be the conversation. Raw event data, full source pages and superseded drafts stay in files and are re-read only when a claim needs rechecking.
- Do not open the writing phase while the raw match data is still in context.

## Subagent delegation

A full-history fork re-sends the whole inherited conversation on every request, so a child agent can cost more than the main thread for the same work. Delegate deliberately.

- Spawn a subagent only for work that genuinely runs in parallel: separate source lookups, chart building while the script is drafted, or an independent check of one specific claim. Do not split one sequential deliverable across several agents.
- Give the child a bounded brief: the exact question, the folder paths, the single file it owns, the acceptance standard, and the minimum context it needs instead of the full conversation.
- One owner per file and per claim set. Do not let a child repeat research or chart work the main thread is already doing, and do not re-verify in the main thread what the child confirmed.
- The child writes into the project folder and returns the conclusion, the file paths and any open uncertainty, not a restatement of the context.
- Delegation must not reduce verification, coverage, player detail or the deliverables. If a task cannot be separated cleanly, keep it in the main thread.

## Coordination cost

Every poll, message or status check re-sends the whole context.

- Wait once with a long timeout instead of polling in a loop.
- Have a subagent write its result to a file and report the path; read the file instead of asking for the text again.
- Send a message only when it changes the next decision, not as a progress heartbeat.

## Chart production efficiency

Chart code and full-resolution images stay in context and are re-sent on every later request, so keep both small.

- Keep one reusable style module for palette, type scale, canvas sizes, footer and axes, plus a per-match entry script that changes only numbers, labels and titles. Start from the previous accepted set instead of authoring the styling again.
- Fix the spec before rendering: canvas size, type scale, margins, palette, and which numbers are labels versus encodings.
- Render one sample chart, usually the match overview, confirm it, then batch the rest. Iterate on the sample rather than re-rendering the whole set.
- Check layout, hierarchy and spacing on a roughly 1200px preview, and open the full-resolution original only as a tight crop around the label or region in question. Do not re-open an image that already passed review.
