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

Bootstrap is a project launcher and creation tool for **Cowboy**.

**Command:**

```
bootstrap
```

**Features:**
- interactive project selector
- fuzzy search using `fzf`
- README preview using `glow`
- project descriptions from `.meta`
- launches Hyprland workspace environment

---

## Bootstrap TUI Interface

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

## Project Launcher
> Opens an existing project in a development workspace

When a project is selected:

```
~/dev/scripts/workspace-launchers/code.sh <project-dir>
```

This launches:

Workspace layout with all terminals in project directory

```
┌─────────┬───────────────┐
│ Claude  │     nvim      │
│ terminal│               │
│         ├───────┬───────┤
│         │ util1 │ util2 │
└─────────┴───────┴───────┘
```

## Project Creation
> Create a new project from _templates

**Command:**
```
bootstrap new <project-name>
---

**Creates a new project directory with templated documents:**

```
<project-name>/
├── README.md
├── architecture.md
├── roadmap.md
├── Makefile
├── .gitignore
├── .meta
└── docs/
    ├─ concepts.md
    └── design-decicions.md

**Initializes a gig repo for the project:**
```
git -C "$PROJECT_DIR" init
git -C "$PROJECT_DIR" add .
git -C "$PROJECT_DIR" commit -m "Initial project scaffold"
```

**Creates a <project-name>.md notes file in Obsidian vault**


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

