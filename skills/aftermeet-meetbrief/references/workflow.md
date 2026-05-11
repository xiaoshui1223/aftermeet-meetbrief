# Workflow

## End-to-End Flow

1. Parse the Feishu/Lark meeting or Minutes link.
2. Check dependencies and authorization.
3. Read meeting metadata: title, duration, owner, note ID, available artifacts.
4. Read AI notes, chapters, todos, transcript, and embedded images when available.
5. Classify meeting type with primary type plus optional tags.
6. Generate one meeting-specific strategy preview.
7. Ask the user once to accept the proposed plan or provide adjustments.
8. After confirmation, run automatically without step-by-step interruption.
9. Capture or select key screenshots.
10. Generate mind map structure.
11. Generate structured document content.
12. Create or update the Feishu document.
13. Ask once whether to clean, keep, or revise task materials.

## Low-Intervention Experience

The product experience should feel highly automated. The normal interaction has only two user questions:

1. Start: show a fast but concrete first-draft plan and ask whether to proceed or adjust.
2. End: after the document is generated, ask whether to clean local task materials, keep them, or revise the document.

Do not ask the user to confirm each screenshot, each section, each formatting choice, or each intermediate step. Make reasonable decisions from the strategy preview and proceed.

## Do Not Skip Preview

Never go straight from link to final document. The preview is part of the product experience and protects the user from getting a wrong document direction.

## Blockers

Pause and ask only when:

- Missing permission or scope.
- Meeting link cannot be read.
- Browser capture cannot proceed and last-resort fallback needs temporary media access.
- The initial strategy preview has not yet been accepted or adjusted.
