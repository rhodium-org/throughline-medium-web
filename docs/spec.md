# Medium — Web page — throughline source

This document is **generated from the graph** by `tl docs`; `tl docs --check` gates
it in CI. The prose headings are hand-owned — everything between `tl:*` markers is
injected from the YAML items, so the published spec can never drift from the graph.

This source is the **medium axis** for one channel: a **web page**, read on screen,
often reached by search, scanned rather than read, with live hyperlinks and a
reflowing layout. It governs how delivery is *shaped for that channel* — structure,
length, navigation, framing and presentation — not universal readability, spelling,
punctuation, register, purpose or audience, each of which is its own throughline
source. Channels are mutually exclusive: **web**, **letter**, **email**, **SMS** and
**print** are sibling sources and a consumer composes exactly one under the `medium`
namespace. Every principle is a `user_requirement`; every rule is a
`system_requirement` that `implements` its principle. The throughline UIDs are this
source's own and immutable — a consumer cites a rule as `medium:SR-0001`.

It carries
<!-- tl:count type == 'user_requirement' -->
5
<!-- tl:end --> principles and
<!-- tl:count type == 'system_requirement' -->
10
<!-- tl:end --> rules.

## Purpose

<!-- tl:item INT-0001 -->
**INT-0001 — Text is delivered as a web page** — `intent`, status `approved`

> A web page is read on screen, often reached through search, scanned rather than read word by word, and may be viewed on a small mobile screen. The reader scrolls, jumps between headings and clicks links, and the page competes for their attention. This axis governs how delivery is shaped for that channel — structure, length, navigation, framing and presentation — not universal readability, spelling, register, purpose or audience, each of which is a separate source. Channels are mutually exclusive: a consumer composes exactly one of the web, letter, email, SMS or print sibling sources.

**source_ref**: TBS Medium — Web page
<!-- tl:end -->

## 1. Structure the page for scanning, not linear reading

<!-- tl:item UR-0001 -->
**UR-0001 — Structure the page for scanning, not linear reading** — `user_requirement`, status `approved`

> Readers scan a web page and jump around it; shape the content so the key point comes first and sections can be found at a glance.

*Derives from:* INT-0001

**source_ref**: TBS Medium — Web page — Structure for the channel
<!-- tl:end -->

<!-- tl:table attrs.get('principle') == 'UR-0001' -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0001 | system_requirement | approved | Put the most important information first |
| SR-0002 | system_requirement | approved | Break the page into short sections with descriptive headings |
<!-- tl:end -->

## 2. Keep each page focused and lead with what matters

<!-- tl:item UR-0002 -->
**UR-0002 — Keep each page focused and lead with what matters** — `user_requirement`, status `approved`

> A web page should cover one thing and put the essential information where the reader sees it first.

*Derives from:* INT-0001

**source_ref**: TBS Medium — Web page — Length and density
<!-- tl:end -->

<!-- tl:table attrs.get('principle') == 'UR-0002' -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0003 | system_requirement | approved | Keep each page to a single topic or task |
| SR-0004 | system_requirement | approved | Place the essential information before the reader must scroll |
<!-- tl:end -->

## 3. Connect and act through the page's live affordances

<!-- tl:item UR-0003 -->
**UR-0003 — Connect and act through the page's live affordances** — `user_requirement`, status `approved`

> On a web page the reader can click, so link related content and offer actions rather than spelling out addresses.

*Derives from:* INT-0001

**source_ref**: TBS Medium — Web page — Navigation and actions
<!-- tl:end -->

<!-- tl:table attrs.get('principle') == 'UR-0003' -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0005 | system_requirement | approved | Link related content and next steps as live hyperlinks |
| SR-0006 | system_requirement | approved | Offer one clear call to action the reader can click |
<!-- tl:end -->

## 4. Frame the page the web way, not as correspondence

<!-- tl:item UR-0004 -->
**UR-0004 — Frame the page the web way, not as correspondence** — `user_requirement`, status `approved`

> A web page is framed by its title, not by a salutation and sign-off; give it a heading that works in search and omit letter framing.

*Derives from:* INT-0001

**source_ref**: TBS Medium — Web page — Opening and closing
<!-- tl:end -->

<!-- tl:table attrs.get('principle') == 'UR-0004' -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0007 | system_requirement | approved | Open with a descriptive page title that works in search |
| SR-0008 | system_requirement | approved | Do not frame a web page as a letter |
<!-- tl:end -->

## 5. Use on-screen formatting and let it reflow

<!-- tl:item UR-0005 -->
**UR-0005 — Use on-screen formatting and let it reflow** — `user_requirement`, status `approved`

> Use the formatting the screen supports to aid scanning, and do not tie the content to a fixed page size.

*Derives from:* INT-0001

**source_ref**: TBS Medium — Web page — Presentation and formatting
<!-- tl:end -->

<!-- tl:table attrs.get('principle') == 'UR-0005' -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0009 | system_requirement | approved | Use on-screen formatting to aid scanning |
| SR-0010 | system_requirement | approved | Do not hard-format for a fixed page width |
<!-- tl:end -->
