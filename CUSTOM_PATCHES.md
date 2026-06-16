# Custom Patches — Session Manager Plugin

Base: zellij v0.44.2

## Patches

### 1. Ctrl+J/K navigation bindings
- **Files:** `default-plugins/session-manager/src/main.rs`
- **Why:** Vim-style navigation (Ctrl+J = down, Ctrl+K = up) across all session-manager screens
- **Upstream PR:** None — personal preference, not planned for upstream

### 2. Custom header with version
- **Files:** `default-plugins/session-manager/src/ui/components.rs`, `default-plugins/session-manager/src/main.rs`
- **Why:** Visual indicator that a custom plugin build is loaded
- **Upstream PR:** None

### 3. Request permissions for file-based plugin loading
- **Files:** `default-plugins/session-manager/src/main.rs`
- **Why:** Allow loading the plugin from a filesystem path (rather than the bundled URI) without permission prompts each launch
- **Upstream PR:** None

### 4. Alphabetical session ordering (single-screen mode)
- **Files:** `default-plugins/session-manager/src/single_screen.rs`, `default-plugins/session-manager/src/ui/mod.rs`
- **Why:** Order the default (empty-search) session list alphabetically by name instead of by recency, so a session is easy to find and related families (e.g. `engineer-*`) cluster together. Keeps active-before-resurrectable grouping; sort is case-insensitive. Replaces `cmp_by_type_then_recency` with `cmp_by_type_then_name` and drops the now-unused `creation_time` field from `UnifiedSearchResult`/`SessionUiInfo`.
- **Upstream PR:** None — personal preference, not planned for upstream
