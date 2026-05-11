# Capture Rules

## Priority

1. Browser capture: default first path whenever the replay page is visible and playable in a logged-in browser.
2. Temporary media-based screenshot capture: last technical fallback only after browser capture has been attempted and found unavailable or insufficient.
3. Embedded Minutes images: final fallback.

## Browser Capture

Use browser automation if available. The user should open or allow opening the Feishu Minutes page and ensure the account can visibly play the replay.

If the replay page is public or share-accessible and can be played in the browser, continue with browser capture even if the user is not the meeting creator and even if media export fails.

Do not start by downloading meeting media. Downloading media consumes local disk space and may fail because of resource-level permissions. Browser capture is the normal path.

Capture strategy:

- Capture the presentation area, not the whole desktop when possible.
- Sample at a reasonable interval.
- Deduplicate visually similar frames.
- Prefer slides/screens that remain visible, contain dense text, show rules/results, or are explained repeatedly.

## Last-Resort Media-Based Screenshot Fallback

Only consider temporary media-based screenshot capture after browser capture has been attempted and cannot produce usable screenshots. Before downloading media, explain why browser capture failed or is insufficient, explain the temporary storage impact, and ask for permission.

Downloaded meeting media is temporary and must be stored inside the current AfterMeet task folder.

If Feishu/Lark returns `403 permission denied` for media access, do not describe the whole task as failed and do not stop for permission troubleshooting first. Treat it as "direct media export is blocked" and continue with the best available visual source:

1. Browser capture from a logged-in replay page, if the replay is visible and playable.
2. Embedded Minutes images or linked document images, clearly labeled as partial visual coverage.
3. Text-only meeting brief, if no visual source is available.

Only tell the user to ask the meeting creator or admin for replay permission when the replay page itself cannot be opened or played. If the page can be opened and played, browser capture is enough.

Shared document images are not equivalent to full replay screenshot coverage. If browser replay capture is unavailable and the user expects dense visual coverage, ask them to open the replay page with an account that can view the original meeting recording, or ask the meeting owner/admin to grant access.

## Embedded Image Fallback

If only embedded images are available, tell the user image count may be low. Do not pretend this is full screenshot coverage.

## Screenshot Density

Use soft ranges:

- Guest/theme sharing: 20-40
- Competition mobilization: 15-40
- Product demo/tool practice: 20-50
- Project/task sync: 3-25

For 2+ hour dense live sessions, fewer than 25 images is usually insufficient.
