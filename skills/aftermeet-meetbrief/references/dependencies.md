# Dependencies

AfterMeet MeetBrief depends on `lark-cli` and Feishu/Lark CLI Skills.

## Check First

Before processing a meeting link, check:

- `lark-cli --version`
- Feishu auth status: `lark-cli auth status`
- Whether relevant Lark Skills are installed locally.
- Whether required scopes are granted.

## Install With User Consent

If `lark-cli` or Lark Skills are missing, ask before installing:

```text
I need Feishu CLI and Feishu CLI Skills to read meetings, capture materials, and write the final Feishu document.
May I install or configure them now?
```

Install:

```bash
npm install -g @larksuite/cli
npx skills add larksuite/cli -g -y
```

First-time app config:

```bash
lark-cli config init --new
```

## Common Scopes

Use minimum necessary scopes and request them only when needed.

```bash
lark-cli auth login --scope "minutes:minutes.media:export"
lark-cli auth login --scope "docx:document:create"
lark-cli auth login --scope "docx:document:write_only"
lark-cli auth login --scope "vc:note:read"
```

## Permission Notes

Being able to read Minutes text, transcripts, AI summaries, or shared document images does not always mean the same account can export the original meeting media. Feishu/Lark may block media access with `403 permission denied` because the user is not the meeting creator, because of meeting owner settings, tenant policy, cross-organization sharing, or missing resource-level permission.

When media export is blocked but the replay page can be visibly opened and played, continue with browser capture. Do not require creator/admin permission for this path, and do not try media download before browser capture. If the replay page itself cannot be viewed or played, tell the user they likely need the meeting creator or admin to open replay access, then downgrade to embedded images or text-only output if needed.

## Updates

If `lark-cli` reports an update, tell the user the current and latest versions and ask before updating.

```bash
npm update -g @larksuite/cli
npx skills add larksuite/cli -g -y
```
