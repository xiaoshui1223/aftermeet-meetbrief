# Cleanup Policy

All local temporary materials must live under the current task folder:

```text
aftermeet-runs/
└── meetbrief-{minute_token}-{timestamp}/
    ├── media/
    ├── raw-frames/
    ├── selected-frames/
    ├── output/
    └── manifest.json
```

Only clean files inside this folder.

## End-of-Task Prompt

After generating the document, ask once:

```text
The Feishu document is ready.
This task produced temporary screenshots and working materials on your computer. If last-resort media fallback was used, downloaded meeting media and raw frames are also stored inside this task folder.

What would you like to do?
1. Looks good, clean all local temporary files from this task.
2. Keep the local files; I may need them.
3. I want revisions; I will tell you what to adjust.
```

## Behavior

- Option 1: clean the current task folder.
- Option 2: keep the current task folder.
- Option 3: keep materials for revision, then ask again after revision.

Never delete files outside the current task folder.
