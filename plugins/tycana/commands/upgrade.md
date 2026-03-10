---
description: "Check for plugin updates and upgrade to the latest version."
allowed-tools:
  - Bash
---

# /tycana:upgrade — Plugin Update

Check for and install updates to the Tycana plugin.

## Process

1. **Get current version.** Read the installed plugin version:

   ```bash
   cat "${CLAUDE_PLUGIN_ROOT}/../../.claude-plugin/plugin.json" 2>/dev/null | grep '"version"' | head -1
   ```

   If that fails, try finding it relative to where the command is running. The version is in `.claude-plugin/plugin.json`.

2. **Check latest version.** Fetch the latest release from GitHub:

   ```bash
   curl -s "https://api.github.com/repos/tycana/tycana-claude-plugin/releases/latest" | grep '"tag_name"' | head -1
   ```

   Strip the `v` prefix if present for comparison.

3. **Compare versions.**

   **If already on latest:**
   ```
   Tycana plugin is up to date (v1.0.0).
   ```
   Done.

   **If update available**, continue to step 4.

4. **Show what changed.** Fetch the changelog:

   ```bash
   curl -s "https://raw.githubusercontent.com/tycana/tycana-claude-plugin/main/CHANGELOG.md"
   ```

   Display entries between the installed and latest versions.

5. **Confirm with the user.** Show the update summary and ask:

   ```
   Tycana plugin update available: v1.0.0 → v1.1.0

   What's new:
   - Added /tycana:wrap-up command
   - Improved capture inference guidelines

   Update now?
   ```

6. **Run the update.** Use the built-in plugin update mechanism:

   ```bash
   claude plugin update tycana
   ```

7. **Confirm success.**

   ```
   Tycana plugin updated to v1.1.0.
   Restart Claude Code to pick up the changes.
   ```

## If Offline or GitHub Unreachable

"Couldn't check for updates (offline or GitHub unreachable). You can update manually with `claude plugin update tycana`."
