# throughline-medium-web

The **web-page channel** of the **medium** content axis, expressed as a
[throughline](https://pypi.org/project/throughline/) **source** — a standalone,
grounded requirements graph that a consuming project composes with
[throughline-compose](https://github.com/rhodium-org/throughline-compose).

This repository holds no application code. It is a directory of small YAML items with
permanent UIDs, validated by `tl check`. Consumers import it under a namespace and
reference its rules as `medium:SR-0001` or its principles as `medium:UR-0001`.

## One orthogonal axis, one channel

The medium axis is *how the delivery channel shapes the content* — how it is
structured, how long it runs, how the reader navigates and acts, how it is framed and
how it is presented. This source is **only** the medium axis, and **only** its **web
page** channel: content read on screen, often reached by search, scanned rather than
read, with live hyperlinks and a reflowing layout. It says nothing about:

- **readability** (word choice, sentence length, active voice) — `throughline-plain-language`
- **conventions** (spelling, punctuation, capitalisation, numbers) — `throughline-conventions-uk`
- **register** (formal, neutral, informal) — `throughline-tone-*`
- **purpose** (inform, instruct, persuade) — `throughline-purpose-*`
- **audience** (general, practitioner, expert) — `throughline-audience-*`

The axis owns only what the channel imposes. Whether there is a sign-off is a *medium*
decision — a letter has one, a web page does not — while the *register* of any sign-off
is a tone decision. The medium axis sits alongside the others and a consumer composes
all it needs.

Channels are **mutually exclusive**: a piece of writing is delivered as a web page *or*
a letter *or* an email *or* an SMS, never several at once. So each channel is a
**sibling** source (`throughline-medium-letter`, and others as they are built) and a
consumer composes exactly one under the `medium` namespace — swapping channel is a
one-line `url`/`ref` change. A task like *"a plain, formal, general-reader web page"*
becomes a **compose** of `plain` + `tone-formal` + `audience-general` + `medium-web`.

## What's in the graph

<!-- tl:count type == 'user_requirement' -->
5
<!-- tl:end --> principles as `user_requirement`s, each `derives_from` the root
intent, and
<!-- tl:count type == 'system_requirement' -->
10
<!-- tl:end --> rules as `system_requirement`s, each `implements` its principle. The
published spec is generated from the graph at [`docs/spec.md`](docs/spec.md).

## Source & licensing

The rules are original house content guidance, licensed under
Apache-2.0. They reproduce no third-party standard. Each rule records its channel and
dimension in `attrs.source_ref` and its owning principle in `attrs.principle`. See
[`NOTICE`](NOTICE).

## Extending the source

Items are hand-authored static YAML — one file per item, one permanent UID per file.
To add a rule, create the next `SR-00NN.yml` by hand (never renumber an existing one)
and link it with `implements` to its principle. Then:

```sh
tl check --strict      # the graph must stay sound
tl docs                # regenerate docs/spec.md + README.md
tl docs --check        # CI gate: docs must match the graph
```
