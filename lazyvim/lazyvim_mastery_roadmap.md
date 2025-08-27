LazyVim Mastery Roadmap (12+ Weeks)

Audience: Experienced engineer moving to Neovim/LazyVim as primary editor, with focus on Flutter/Dart, Android/Kotlin, and general productivity on macOS & Linux.

Goals:
	•	Become fluent in Vim motions without thinking.
	•	Configure and extend LazyVim with Lua confidently.
	•	Achieve IDE‑level workflows (LSP, DAP, tests, formatting, linting) for Flutter/Dart and Android/Kotlin.
	•	Build a personal LazyVim distribution (dotfiles) you can bootstrap on any machine in minutes.

⸻

Phase 0 — Setup & Mindset (Day 0–1)
	•	Install: Neovim (latest stable), Git, ripgrep, fd, node, pyenv, lua (optional), Xcode CLT (macOS), build-essential (Linux).
	•	Install LazyVim: follow official bootstrap; keep defaults.
	•	Baseline UX toggles: relative numbers, cursorline, colorcolumn=100, wrap off, scrolloff=8.
	•	Keymap posture: home row, jk or fd for quick escape, caps→ctrl at OS level, swap left/right cmd/alt as preferred.
	•	Measurement: enable a keystroke logger plugin (optional) or track practice minutes; keep a habit journal.

Deliverable: Fresh LazyVim with zero custom plugins and a notes.md for daily captures.

⸻

Phase 1 — Vim Core Fluency (Week 1–2)

Objective: Sub-1s navigation to any token; stop using arrow keys/mouse.
	•	Motions: w e b ge, f/F t/T ; ,, 0 ^ $, gg G H M L, %, [{ ]}, * #.
	•	Text objects: ciw daw vi" ci( da[ va{, ip ap i" a", it at (HTML/TSX), i{ a{.
	•	Operators: d c y + {motion}; ~ swap case; g~ gU gu.
	•	Jumps: marks m{char}, back/forward Ctrl-o/Ctrl-i; global marks mA…mZ.
	•	Macros & registers: q{reg} … q, @a, @@, :reg.
	•	Windows/tabs/buffers: :bnext :bprev :bdelete, :enew, splits :vsplit :split, move with Ctrl-hjkl.
	•	Search/replace: / and ?, n N, :%s/old/new/gc, :g and :v.

Drills (daily 15–20m):
	•	Navigate and edit a sample code file using only motions & text objects.
	•	Record macro to align/sort/format blocks; replay it across files.
	•	Refactor variable name in a project with %s and :args.

Milestone: Complete a coding session (1h) without mouse/arrow keys.

⸻

Phase 2 — Neovim Essentials (Week 2–3)

Objective: Understand Neovim runtime and LazyVim conventions.
	•	Runtime & packs: $XDG_CONFIG_HOME/nvim, runtimepath, after/, ftplugins.
	•	Lua basics: tables, functions, modules (require), keymaps API (vim.keymap.set).
	•	Lazy.nvim: specs, events, cmd, ft, keys, dependencies, opts/config pattern.
	•	Keymaps: leader philosophy; which‑key discovery; avoiding conflicts.
	•	File finding: Telescope basics (files, live_grep, buffers, help_tags).
	•	Tree‑sitter: syntax, textobjects, incremental selection.

Exercise: Recreate one default plugin spec from memory and tweak an option.

Milestone: You can read and explain any plugin spec in your config.

⸻

Phase 3 — LSP, Format, Lint (Week 3–4)

Objective: First‑class language features.
	•	mason.nvim to install tools; nvim-lspconfig for servers.
	•	Formatting: conform.nvim or null-ls successor; set per‑lang formatters.
	•	Diagnostics: virtual text signs, severity, jump list.
	•	Code actions & rename: map under <leader>ca, <leader>cr.
	•	Symbols: outline (aerial/symbols-outline), workspace symbols via Telescope.

Deliverable:
	•	Global format‑on‑save with per‑language overrides.
	•	LSP attached autocommands (e.g., inlay hints, signature help).

Milestone: End‑to‑end: open → edit → format → lint → jump to def → rename → test.

⸻

Phase 4 — Debugging (DAP) & Tests (Week 4–5)

Objective: Replace external IDEs for step‑debug & tests.
	•	nvim-dap: adapters, configurations, breakpoints, step, scopes, repl.
	•	UI: nvim-dap-ui; virtual text.
	•	Tests: neotest for Jest, Go, Py, Dart (via adapters where available).
	•	Tasks: overseer.nvim or lazyterm for running scripts.

Milestone: Debug a failing unit test end‑to‑end inside Neovim.

⸻

Phase 5 — Workflow Power‑Ups (Week 5–6)

Objective: Cut friction; automate rituals.
	•	Git: gitsigns, lazygit integration (open in floating terminal), diffview.
	•	Refactor: treesj/splitjoin, mini.move, substitute.nvim.
	•	Text motion: leap.nvim or flash.nvim; hop‑style jumps.
	•	Surround & pairs: mini.surround/which; nvim-autopairs.
	•	Snippets: luasnip; per‑lang snippet collections; link Tab/Shift‑Tab.
	•	Commenting: Comment.nvim with ts‑context‑commentstring.
	•	Project: project.nvim; root detection strategies.

Deliverable: A cheatsheet buffer (:help your-cheatsheet) bound to <leader>?.

⸻

Phase 6 — Flutter/Dart & Android/Kotlin (Week 6–8)

Objective: IDE‑level mobile dev inside LazyVim.

Flutter/Dart
	•	Servers: dartls via lspconfig; flutter-tools.nvim for UI, dev‑log, hot‑reload, :FlutterRun and :FlutterDevTools.
	•	Format/lint: dart format + dart fix; integrate with conform.
	•	Tests: neotest‑dart (or run via overseer tasks).
	•	DAP: via flutter‑tools (uses Dart debug adapter under the hood).
	•	Hot reload keys: map <leader>fr to hot reload, <leader>fR to restart.

Android/Kotlin
	•	Servers: kotlin-language-server; Java: jdtls per‑project workspace.
	•	Build/Tasks: overseer + Gradle tasks (./gradlew assembleDebug etc.).
	•	Lint: ktlint/detekt wired to conform/diagnostics.
	•	DAP: Java debug (jdtls + vscode‑java‑debug adapter).

Milestone: Ship a small Flutter feature branch 100% in Neovim.

⸻

Phase 7 — Performance, Profiling, Reliability (Week 8–9)

Objective: Start fast, stay fast.
	•	Lazy profiling: :Lazy profile (startup time, offenders).
	•	Lazy load: events, ft, cmd; remove redundant plugins.
	•	Health: :checkhealth and fix red flags.
	•	Large files: conditionally disable treesitter/lint; use fastinspect.
	•	Backup/undo: persistent undo, swap, backup dirs.

Deliverable: A documented PERF_NOTES.md with before/after timings.

⸻

Phase 8 — Dotfiles as a Product (Week 9–10)

Objective: Portable, reproducible setup.
	•	Structure: ~/.config/nvim/lua/plugins/ (plugin specs), lua/config/ (core), ftplugin/ overrides, after/.
	•	Bootstrap: install.sh that installs deps, symlinks config, runs nvim --headless '+Lazy! sync' +qa.
	•	Secrets: machine‑local settings in local.lua git‑ignored.
	•	Docs: README.md with screenshots, keymaps table, onboarding steps.

Milestone: New machine → fully working LazyVim in <10 minutes.

⸻

Phase 9 — Mastery Projects (Week 10–12)

Pick 2–3:
	1.	Refactor‑athon: Port a legacy module using macros, LSP rename, treesitter textobjects.
	2.	Debugger deep dive: Build a DAP config for a niche runtime.
	3.	Plugin authoring: Write a 100–300 LOC Lua plugin (e.g., quickfix enhancer, time tracker).
	4.	Telescope pro: Custom pickers (live grep in changed files, GH issues, Flutter routes).
	5.	Neotest suite: Full test UX for your main stack.

Deliverable: Public repo of your config + a blog‑style NOTES.md.

⸻

Daily/Weekly Practice Plan (Template)
	•	Daily (30–45m):
	•	10m motion drills (random code, no arrows)
	•	10m LSP/DAP practice (navigate diagnostics, run tests)
	•	10–25m build one automation (macro/snippet/command)
	•	Weekly:
	•	1h refactor session using only Vim operators/textobjects
	•	30m profiling & cleanup
	•	30m notes update and keymap review

⸻

Opinionated Keymap Set (Starting Point)
	•	Leader: <space>
	•	Navigation: s (leap/flash), ; repeat, , reverse
	•	Buffers: <leader>bb buffers, <leader>bd delete, <leader>bo only
	•	Files: <leader>ff files, <leader>fg live grep, <leader>fh help
	•	Git: <leader>gg lazygit, <leader>gd diffview, [g/]g hunks
	•	LSP: gd goto def, gr refs, <leader>cr rename, <leader>ca code action, <leader>cs symbols
	•	Tests: <leader>tn nearest, <leader>tf file, <leader>to output
	•	Debug: <F5> continue, <F10> step‑over, <F11> step‑in, <F9> toggle bp, <leader>du DAP UI
	•	Flutter: <leader>fr hot‑reload, <leader>fR restart, <leader>fl dev‑log

⸻

Minimal Plugin List to Master (LazyVim‑compatible)
	•	Core: telescope.nvim, nvim-treesitter, which-key.nvim, flash.nvim/leap.nvim, neo-tree.nvim, gitsigns.nvim, comment.nvim, nvim-autopairs, luasnip, conform.nvim, mason.nvim, nvim-lspconfig, null-ls successor (if used), trouble.nvim, aerial.nvim, nvim-dap, nvim-dap-ui, overseer.nvim, project.nvim, diffview.nvim.
	•	Mobile: flutter-tools.nvim, jdtls, kotlin-language-server.

⸻

Config Skeleton (Lua)

-- ~/.config/nvim/lua/plugins/flutter.lua
return {
  {
    "akinsho/flutter-tools.nvim",
    dependencies = { "nvim-lua/plenary.nvim", "stevearc/dressing.nvim" },
    ft = { "dart" },
    opts = {
      ui = { border = "rounded" },
      widget_guides = { enabled = true },
      closing_tags = { highlight = "Comment" },
      dev_log = { enabled = true, open_cmd = "tabedit" },
      lsp = { color = { enabled = true } },
    },
    keys = {
      { "<leader>fr", function() require("flutter-tools.commands").reload() end, desc = "Flutter Hot Reload" },
      { "<leader>fR", ":FlutterRestart<CR>", desc = "Flutter Restart" },
      { "<leader>fl", ":FlutterDevTools<CR>", desc = "Flutter DevTools" },
    },
  },
}

-- ~/.config/nvim/lua/plugins/kotlin.lua
return {
  {
    "neovim/nvim-lspconfig",
    opts = {
      servers = { kotlin_language_server = {} },
    },
  },
  {
    "stevearc/conform.nvim",
    opts = {
      formatters_by_ft = {
        kotlin = { "ktlint" },
      },
    },
  },
}

-- ~/.config/nvim/lua/config/autocmds.lua
vim.api.nvim_create_autocmd("TextYankPost", {
  callback = function()
    vim.highlight.on_yank({ higroup = "IncSearch", timeout = 200 })
  end,
})


⸻

Troubleshooting & Pitfalls
	•	Too many plugins: profile and remove. Prefer lazy‑loading.
	•	Keymap collisions: standardize your leader map; document all non‑default maps.
	•	LSP noise: tune diagnostics (virtual text off for info), set signs by severity.
	•	Filetype gotchas: ensure ft detection; add autocmds for uncommon extensions.
	•	JDTLS workspaces: per‑project data dirs to avoid clashes.
	•	Flutter attach: ensure flutter-tools manages dartls to avoid double‑attach.

⸻

Mastery Checkpoints
	•	Wk 2: 100% keyboard navigation; macros for repetitive edits.
	•	Wk 4: LSP/format/lint stable across 3 languages.
	•	Wk 6: Debugging & tests inside Neovim.
	•	Wk 8: Flutter feature built & debugged with hot reload.
	•	Wk 10: New machine bootstrap <10m.
	•	Wk 12: Ship a small Lua plugin and publish your dotfiles.

⸻

Extension Ideas (Post‑12 Weeks)
	•	Treesitter queries for custom textobjects.
	•	Writing in Neovim: markdown pipelines (glow preview/markdown‑preview), table mode.
	•	AI assist: inline completions via cmp sources/coding assistants.
	•	Remote dev: sshfs/:Term/tmux; oil.nvim for remote editing.
	•	TUI dashboards: start screen with recent projects, sessions, timers.

⸻

Checklist (Printable)
	•	No arrows/mouse for 1 full session
	•	Macro recorded & reused
	•	Telescope custom picker created
	•	Format‑on‑save per language
	•	DAP configured for 2 runtimes
	•	neotest wired to run nearest test
	•	Flutter hot‑reload keymaps
	•	Kotlin LSP + ktlint
	•	install.sh bootstrap working
	•	README + cheatsheet buffer

⸻

Your Next 7 Days (Quick Start)

Day 1: Install + learn 20 motions (write them on a card).
Day 2: Text objects + operators drill; set up Telescope.
Day 3: Mason + LSP for Dart/Kotlin; format‑on‑save.
Day 4: Git integrations + lazygit; create keymap cheatsheet.
Day 5: DAP base + neotest; run tests from Neovim.
Day 6: Add flutter‑tools; map hot‑reload/restart/devtools.
Day 7: Profile startup; remove 3 plugins; write notes.
