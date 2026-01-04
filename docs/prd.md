# Product Requirement Document: GitVault
**Status:** Draft / In Progress
**Author:** Muhammad Guntur Ricky Adhitya

---

## 1. Summary
A mobile Git Client using Obsidian Aesthetic (Vault, Markdown)

## 2. User Persona
- Developer who store their second brain on Github
- Users who find existing mobile Github Client too IDE-Focused and want a clean environment to write

## 3. Core Features (MVP)
### A. Vault Manager
- [ ] Open a local folder as Vault
- [ ] Support for nested folders and basic file operations (Rename, Delete, Add, Move, Copy)
- [ ] Dual Sidebars (Explorer on left, Metadata on Right)

### B. The Editor
- [ ] Syntax highlighting
- [ ] Floating Button to open command pallete (new file, push, pull, commit)
- [ ] Live preview mode or high-quality rendering

### C. Github Sync
- [ ] OAuth integration for Github
- [ ] Automatic Background commits on file save
- [ ] Manual "Pull/Push" sync indicator in the status bar
- [ ] Merge conflict resolution UI (Keep Local or Keep Remote)

## 4. Technical Constraint
- Must use libgit for performance
- Use android scoped storage but allow user-selected folder access
- OAuth tokens must be stored in the Android Keystore

## 5. User Journey
1. **First Run:** User log in to Github --> Select a Remote Repo --> App Clone the Repo to local storage
2. **Daily Use:** Users edits note.md --> app trigger git commit locally --> app pushes on the background

---
## 6. Success Metrics
- Sync Speed < 3 seconds for small text changes
- Zero data loss during simultaneous edits
