# Custom Patches — Session Manager Plugin

Base: zellij v0.44.0

## Patches

### 1. Ctrl+J/K navigation bindings
- **Files:** `default-plugins/session-manager/src/main.rs`
- **Why:** Vim-style navigation (Ctrl+J = down, Ctrl+K = up) across all session-manager screens
- **Upstream PR:** None — personal preference, not planned for upstream

### 2. Custom header with version
- **Files:** `default-plugins/session-manager/src/ui/components.rs`, `default-plugins/session-manager/src/main.rs`
- **Why:** Visual indicator that a custom plugin build is loaded
- **Upstream PR:** None

### 3. Fix: do not reset layout selection (#4919)
- **Files:** `default-plugins/session-manager/src/main.rs`
- **Why:** Cherry-picked from upstream main — fix landed after v0.44.0 release
- **Upstream PR:** #4919 — will be in next release, drop this patch when rebasing onto it
