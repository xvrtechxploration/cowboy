# Cowboy — Current Status

**Current structure:**

```
cowboy/
├── _template
├── cowboy-docs
├── projects
│   ├── lasso
│   └── wrangler
└── tools
    └── bootstrap
```

---

# Bootstrap

Bootstrap is the **Cowboy project launcher**.

**Command:**

```
bootstrap
```

**Features:**

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

Workspace layout

```
┌─────────┬───────────────┐
│ Claude  │     nvim      │
│ terminal│               │
│         ├───────┬───────┤
│         │ util1 │ util2 │
└─────────┴───────┴───────┘
```

---

# Current Projects

| Name     | Description                       | Skills                              |
| -------  | --------------------------------- | ----------------------------------- |
| lasso    | Networking information CLI tool   | bash, networking, shell scripting   |
| wrangler | Gather network device information | python, automation, networking, api |

---

# Planned Projects

Future Cowboy projects:

| Name        | Description               | Skills |
| ----------- | ------------------------- | ------ |
| roundup     | system monitoring CLI     |        |
| telegraph   | API exploration tool      |        |
| bountyboard | task automation framework |        |


---

# Cowboy Design Philosophy

Projects should:

• teach a **specific core skill**
• be **small but complete** tools
• have **clear documentation**
• be **portfolio quality**

Each project should include:

- architecture.md
- roadmap.md
- README.md
- demo screenshots

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

