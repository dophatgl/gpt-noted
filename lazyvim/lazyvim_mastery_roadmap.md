# LazyVim Mastery Roadmap (12+ Weeks)

**Audience:** Experienced engineer moving to Neovim/LazyVim as primary editor, with focus on Flutter/Dart, Android/Kotlin, and general productivity on macOS & Linux.

**Goals:**
- Become fluent in Vim motions without thinking.
- Configure and extend LazyVim with Lua confidently.
- Achieve IDE‑level workflows (LSP, DAP, tests, formatting, linting) for Flutter/Dart and Android/Kotlin.
- Build a personal LazyVim distribution (dotfiles) you can bootstrap on any machine in minutes.

---

## Phase 0 — Setup & Mindset (Day 0–1)
- **Install**: Neovim (latest stable), Git, ripgrep, fd, node, pyenv, lua (optional), Xcode CLT (macOS), build-essential (Linux).
- **Install LazyVim**: follow official bootstrap; keep defaults.
- **Baseline UX toggles**: relative numbers, cursorline, colorcolumn=100, wrap off, scrolloff=8.
- **Keymap posture**: home row, `jk` or `fd` for quick escape, caps→ctrl at OS level, swap left/right cmd/alt as preferred.
- **Measurement**: enable a keystroke logger plugin (optional) or track practice minutes; keep a habit journal.

**Deliverable**: Fresh LazyVim with zero custom plugins and a notes.md for daily captures.

---

## Phase 1 — Vim Core Fluency (Week 1–2)
**Objective:** Sub-1s navigation to any token; stop using arrow keys/mouse.

- **Motions**: `w e b ge`, `f/F t/T ; ,`, `0 ^ $`, `gg G H M L`, `%`, `[{ ]}`, `* #`.
- **Text objects**: `ciw daw vi" ci( da[ va{`, `ip ap i" a"`, `it at` (HTML/TSX), `i{ a{`.
- **Operators**: `d c y` + `{motion}`; `~` swap case; `g~ gU gu`.
- **Jumps**: marks `m{char}`, back/forward `` Ctrl-o/Ctrl-i ``; global marks `mA…mZ`.
- **Macros & registers**: `q{reg} … q`, `@a`, `@@`, `:reg`.
- **Windows/tabs/buffers**: `:bnext :bprev :bdelete`, `:enew`, splits `:vsplit :split`, move with `Ctrl-hjkl`.
- **Search/replace**: `/` and `?`, `n N`, `:%s/old/new/gc`, `:g` and `:v`.

**Drills (daily 15–20m):**
- Navigate and edit a sample code file using only motions & text objects.
- Record macro to align/sort/format blocks; replay it across files.
- Refactor variable name in a project with `%s` and `:args`.

**Milestone:** Complete a coding session (1h) without mouse/arrow keys.

---

...(truncated for brevity in this snippet)...
