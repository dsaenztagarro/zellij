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
