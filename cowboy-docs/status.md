# Cowboy Dev Range — Current Status

## Root Directory

```
~/dev/cowboy
```

Current structure:

```
cowboy/
├── _template
├── tools
│   └── bootstrap
├── lasso
├── wrangler
```

---

# Bootstrap CLI

Bootstrap is the **Cowboy project launcher**.

Command:

```
bootstrap
```

Features:

• interactive project selector
• fuzzy search using `fzf`
• README preview using `glow`
• project descriptions from `.meta`
• launches Hyprland workspace environment

---

# Bootstrap Interface

TUI shows:

```
🐎 Cowboy Dev Range
────────────────────────

lasso        System Networking Info
wrangler     Network device automation
```

Right side preview:

```
README.md rendered with glow
```

---

# Project Launcher

When a project is selected:

```
~/dev/scripts/workspace-launchers/code.sh <project-dir>
```

This launches:

Workspace 4 layout

```
┌─────────┬───────────────┐
│ Claude  │     nvim      │
│ terminal│               │
├─────────┼───────┬───────┤
│ util1   │ util2 │       │
└─────────┴───────┴───────┘
```

---

# Current Projects

## lasso

Purpose:

System networking information CLI tool.

Focus:

• bash scripting
• CLI parsing
• linux networking commands

Commands used:

```
ip
hostnamectl
resolvectl
awk
grep
```

---

## wrangler

Purpose:

Network automation framework.

Focus:

• Python
• network automation
• device inventory
• SSH/API interaction

---

# Planned Projects

Future Cowboy projects:

```
roundup      system monitoring CLI
telegraph    API exploration tool
bountyboard  task automation framework
```

---

# Cowboy Design Philosophy

Projects should:

• teach a **specific core skill**
• be **small but complete** tools
• have **clear documentation**
• be **portfolio quality**

Each project should include:

```
architecture.md
roadmap.md
README.md
demo screenshots
```

---

# Planned Bootstrap Improvements

Future upgrades for `bootstrap`:

### Project dashboard preview

Preview panel could show:

```
Project name
Description
Last commit
README
```

---

### Additional commands

```
bootstrap new
bootstrap open
bootstrap list
bootstrap status
```

---

### Project metadata

Projects may eventually include:

```
.meta
stage
language
created date
```

---

# Long-Term Vision

Cowboy Dev Range becomes a **personal engineering lab** where each project teaches a focused set of skills:

```
bash
python
devops
network automation
API design
systems programming
```

while building a real portfolio of tools.

---

If you'd like, the **next thing I would strongly recommend** is something that will make this system dramatically more powerful:

Turning `bootstrap` into a **full CLI tool with subcommands and TUI**, similar to tools like `kubectl` or `gh`.

That only requires about **40–50 more lines of code**, but it makes the whole Cowboy environment feel like a real developer platform.
