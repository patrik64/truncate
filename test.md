# Maintaining Operational State (BROKEN REPRO)

## Setup
This file intentionally references images that can never resolve to force a hard fetch failure.

## Broken image (external, Markdown)
![Broken-External-MD](https://definitely-does-not-exist.invalid/abc123.png)

## Broken image (external, HTML)
<img src="https://definitely-does-not-exist.invalid/abc123.png" alt="Broken-External-HTML" />

## Broken image (relative, Markdown)
![Broken-Relative-MD](./__surely_missing__/nope.png)

### Post-image validation section
If you can read this in **GitHub** but it is **missing** in **Ketryx**, the parser truncated after a failed attachment fetch.

#### Extra content below to rule out length/format edge cases
- Bullet A
- Bullet B

```json
{"note":"A fenced code block placed after the images; if this doesn't render in Ketryx, truncation occurred above."}

| Col A | Col B |
| ----: | :---- |
|     1 | ok    |
|     2 | ok    |


3) **Commit directly** to the same branch Ketryx analyzes.

4) In **Ketryx → Settings → Repositories**, confirm:
   - The **glob** covers this path (it will if your previous file synced).
   - The feature flag **`enableGitBasedItemsAttachments`** is enabled for this environment.

5) **Trigger a re-parse** (any one of these works):
   - Click **Save changes** on the repository settings (even without edits), or
   - Make a tiny change (add a space) to the file and commit again.

6) Open the new record for `Body-broken.md` in Ketryx.

### Expected
- GitHub shows the **entire** file.
- **Ketryx** renders **until one of the broken images**, then **“Post-image validation section”** (and content below it) does **not** appear.

---

## If it still doesn’t truncate
Some environments now continue rendering after failures. Two escalations:

- **Move the first broken image to the very top** (line 1) to ensure it’s hit before anything else.
- **Use an absurd relative escape** that cannot map inside the repo:
  ```markdown
  ![Absurd](../../../../../../../../__missing__/nope.png)
