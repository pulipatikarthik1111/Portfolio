# Portfolio

A personal portfolio project, developed and maintained with **Cursor** as the primary editor and AI-assisted workflows via **Claude Code** and **Codex**.

---

## Environment setup

This section documents the tooling installed on this machine, the setup checklist that was completed end-to-end, and the practical issues encountered along the way (plus how they were resolved).

### Tools installed

| Tool | Role | How it was added |
|------|------|-------------------|
| **Cursor IDE** | Code editor with integrated AI and Git workflows | Downloaded and installed from the official site (see link below). |
| **Claude Code** (Cursor extension) | AI assistant integrated into the editor | **Extensions** panel in Cursor → search **“Claude Code”** → install → sign in. |
| **Codex** (Cursor extension) | Additional AI coding support in Cursor | **Extensions** panel in Cursor → search **“Codex”** → install → sign in. |
| **Git** | Lets Cursor clone, commit, and sync with GitHub | Installed **Git for Windows** from the official installer so the `git` command is available on the system `PATH` (see challenge #1 below). |

Both extensions were installed from Cursor’s **Extensions** page (same flow as VS Code: open Extensions, search by name, install, then complete provider login when prompted).

---

## Setup checklist (completed)

The following steps were completed in order to have a working GitHub + Cursor workflow for this repository.

1. **Install Cursor IDE**  
   Installed Cursor from the official download page: [https://cursor.com/](https://cursor.com/)

2. **Add Claude Code in Cursor**  
   Opened **Extensions**, searched for **“Claude Code”**, installed the add-on, and signed in so the extension could be used from the editor.

3. **Add Codex in Cursor**  
   Opened **Extensions**, searched for **“Codex”**, installed the add-on, and signed in the same way.

4. **Create a public GitHub repository**  
   Created a GitHub account (where needed) and a **public** repository to host this project. GitHub’s home page: [https://github.com/](https://github.com/)

5. **Open the repository in Cursor**  
   Cloned or opened the GitHub repo inside Cursor so all edits, commits, and pushes happen in one place.

6. **Author this README**  
   Added this `README.md` to describe installed tools, completed steps, and issues faced during setup.

---

## Challenges and how they were solved

### 1. Cloning the GitHub repository in Cursor

**What went wrong:** Cloning from Cursor failed because **Git was not installed locally**. Cursor’s Git integration (and features like **Clone Repository**) rely on a working `git` executable on your machine; without it, the clone step cannot run.

**What helped:**

- Downloaded and installed **Git for Windows** from the official Git project site ([https://git-scm.com/download/win](https://git-scm.com/download/win)).  
- Accepted the installer defaults that add Git to the system **PATH** (or chose **“Git from the command line and also from 3rd-party software”** so GUI apps like Cursor can find `git`).  
- **Closed and reopened Cursor** (or signed out of Windows once) so it picked up the updated `PATH`.  
- Ran **Clone Repository** again in Cursor and signed in to GitHub when prompted for HTTPS access, if needed.

### 2. Browser settings while creating the GitHub account

**What went wrong:** Minor difficulty during GitHub account creation, often related to the browser (pop-ups blocked, cookies/tracking restrictions, or verification flows not showing).

**What helped:**

- Allowed **pop-ups** and **third-party cookies** (temporarily) for `github.com` so verification and OAuth flows could complete.  
- Tried another browser or an **incognito/private** window to rule out extensions blocking scripts.  
- Completed **email verification** from the inbox and refreshed the GitHub tab if the UI stalled.

---

## Repository purpose

This repo holds the **Portfolio** project source. Future updates can extend this README with build instructions, tech stack, and deployment notes as the project grows.

---

## Quick links

- [Cursor](https://cursor.com/)  
- [GitHub](https://github.com/)  
- [Git for Windows](https://git-scm.com/download/win)  
