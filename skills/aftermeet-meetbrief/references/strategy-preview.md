# Strategy Preview

Before generating the document, show a strategy preview based on the real meeting.

The preview must help the user decide the document direction, not merely choose a speed option.

Keep the preview fast and actionable. It should be the only required confirmation before generation. After the user accepts it, continue automatically until the document is produced unless a true blocker appears.

## Required Fields

- Meeting topic
- Meeting duration
- Meeting type and supplemental tags
- Classification basis
- Recommended plan and reason
- Concise plan: screenshots, quotes, modules, use case
- Detailed plan: screenshots, quotes, modules, use case
- Screenshot path: browser capture first, last-resort media-based screenshot fallback only if needed, embedded-image fallback
- Document framework preview
- Document style: AfterMeet structured brief style
- Cleanup behavior

## Framework Preview

Show the rough final document structure:

- Mind map top-level branches
- Meeting overview
- Type-specific front module
- Core viewpoint sections
- Screenshot distribution
- Speaker viewpoints and quote direction
- Action guide direction

## Example

```text
I checked this meeting and prepared a generation strategy:

Meeting topic: 04-10 | Mini Camp 第一期：玩转飞书 CLI 专场
Duration: about 2h 21m
Type: Guest sharing + competition mobilization + tool practice
Basis: It contains prize/submission information, multiple guest shares, and dense screen demos.

A. Concise version
- Screenshots: 15-25
- Quotes: 5-8
- Modules: mind map, overview, core conclusions, key screenshots, quotes, action guide
- Best for: quick review

B. Detailed version
- Screenshots: 35-60
- Quotes: 10-18
- Modules: mind map, competition info, viewpoint breakdown, step screenshots, speaker viewpoints, quotes, action guide
- Best for: long-meeting archive, public case, demo

Recommended: B, because this meeting is long, multi-speaker, and visually dense.

Framework preview:
1. Mind map: meeting storyline, competition info, CLI concepts, guest cases, action path
2. Overview: topic, duration, type, goal
3. Competition info: prizes, submission method, packaging advice
4. Core viewpoints: CLI as Agent execution entry, Feishu workflows, scene-based Skills
5. Screenshots: rules pages, tool concepts, guest demos, case results
6. Speaker viewpoints and quotes
7. Action guide

Reply "go" to proceed, or tell me what to adjust. After confirmation, I will finish the document automatically and only ask again at the end for cleanup or revision.
```
