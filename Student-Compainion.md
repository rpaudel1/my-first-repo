# Git + GitHub for Faculty — Student Companion

**Workshop One · 60 minutes · Browser-only**
**AWS MLU Faculty Fellowship · Delaware State University**

---

## How to use this companion

This is your step-by-step walkthrough for the live workshop. It is designed so that **you can finish the hands-on work even if you fall behind, miss a moment, or get stuck** — there are 600 of us, so the room cannot stop for one question.

Three ways to use it:

- **Follow along live.** Keep this open next to your GitHub tab. Each numbered step matches a moment in the live session.
- **Catch up if you fall behind.** Each section is self-contained. Skip ahead to where the instructor is and use this to fill in what you missed.
- **Re-do it solo afterwards.** Everything you need to reproduce the workshop on your own is in this document.

Throughout this companion:

- 🟢 **Do this** — an action for you to take.
- 👀 **You should see** — what success looks like on your screen.
- ⚠️ **If you get stuck** — inline troubleshooting.
- 💡 **Why this matters** — short context that makes the step stick.

**Session timing strip** (keep an eye on the instructor's clock):

| 0–5 | 5–13 | 13–23 | **23–35** | **35–48** | 48–55 | 55–60 |
|---|---|---|---|---|---|---|
| Welcome | Git literacy | GitHub tour | **Fork** | **Edit & Commit** | github.dev | Preview & wrap |

The two bold blocks are the hands-on. If you only stay focused for one stretch, stay focused from minute 23 to minute 48.

---

## Before the session — Pre-work (do this at least 24 hours ahead)

You **cannot** complete the live hands-on without a working GitHub account. Please do these steps the day before.

### 1. Create a free GitHub account

🟢 Go to **https://github.com/signup**

🟢 Enter:
- Your email (a personal email is fine; an institutional email is also fine)
- A password
- A username — **this will appear in every URL of every repository you create**, so choose something you are comfortable with publicly. Many faculty use `firstname-lastname` or `flastname-institution`.

🟢 Solve the puzzle, click **Create account**.

🟢 Open your email and click the GitHub verification link.

👀 **You should see** your new GitHub home page at `github.com`, with your avatar in the top-right corner.

### 2. Confirm you can sign in

🟢 Sign out, then sign back in at github.com. Confirm it works without a password reset.

⚠️ **If you get a "device verification" email** — that is normal. Click the link in the email to confirm the new sign-in.

### 3. Open these three tabs and bookmark them

| Tab | URL | What it is |
|---|---|---|
| 1 | https://github.com | Your home page when signed in |
| 2 | https://github.com/aws-dsu/my-first-repo | The practice repo you will fork |
| 3 | https://github.dev | Browser-based code editor (bonus segment) |

### 4. Pre-work checklist — "You're ready when…"

- [ ] I can sign in to github.com without resetting my password.
- [ ] My username appears in the top-right corner of github.com when I am signed in.
- [ ] I can open `github.com/aws-dsu/my-first-repo` and read the README.
- [ ] I have this companion document open on a second monitor or in a second window.

---

## Part 0 · Setup (0–5 min) — Watch & listen

The instructor will set ground rules for the room. While they talk, get your screen ready.

🟢 Confirm you are **signed in** to github.com. Look for your avatar in the top-right.

🟢 Open the practice repo in a second tab: **https://github.com/aws-dsu/my-first-repo**

🟢 Keep this companion document visible.

**Room norms to know:**
- Stay muted. The room will not be unmuted.
- Chat is for clarifying questions only. Three named moderators will answer.
- If you fall behind, **do not panic** — the session is recorded with chapter markers and there are 72 hours of async help afterwards.

**By the end of this hour, you will have:**
1. Forked a real repository.
2. Made your first commit.
3. Opened a full code editor in a browser tab (no install).

---

## Part 1 · Git Literacy (5–13 min) — Watch & capture

The instructor will define git and GitHub. Capture these two definitions verbatim — they are the ones you can keep.

> **Git is a time machine for files.**
> **GitHub is the cloud where time machines live.**

### The four verbs you will keep hearing

| Verb | What it does | Browser equivalent (today) |
|---|---|---|
| **clone** | Copy a repository from GitHub down to a computer or cloud environment. | **Fork** (creates your own copy on GitHub) |
| **edit** | Change one or more files. | **Pencil icon** on github.com, or **github.dev** |
| **commit** | Save a labeled snapshot of your changes to the project history. | **Commit changes** button |
| **sync** | Send your commits up to GitHub, or pull GitHub's commits down. | **Sync** button in github.dev |

### Today's loop: F.E.C.

The three moves you will practice this hour:

```
   F  ──────►  E  ──────►  C
  Fork        Edit       Commit
```

- **F — Fork:** Click the Fork button on a repo page. Now you own a copy. The original is untouched.
- **E — Edit:** Click the pencil icon. Change the file in the web editor. Your fork only.
- **C — Commit:** Click Commit changes. Save a labeled snapshot. It is now in your history.

💡 **Why this matters:** Fork ≈ Remix. The mental move you practice today is the same one you will practice in PartyRock next session.

### Five reasons educators learn git

Skim this — do not memorize.

1. **Distribute materials** — push course resources to students with one link, and update them in place.
2. **Customize official labs** — fork AWS or vendor materials and adapt them for your syllabus.
3. **Pull updates cleanly** — when AWS revises a lab, pull updates into your fork without redoing your edits.
4. **Public teaching portfolio** — your repos become a durable, citable record of your course design.
5. **Collaborate with peers** — co-author labs with colleagues across institutions.

---

## Part 2 · GitHub Tour (13–23 min) — Watch & label

The instructor will live-tour **github.com/aws-dsu/my-first-repo**. As they speak, find each of the seven elements below on your screen.

### Seven things to locate on the repo page

```
┌─────────────────────────────────────────────────────────────────┐
│   [1] aws-dsu  /  [2] my-first-repo            [7] ⑂ Fork  ▼   │
│   ─────────────────────────────────────────────────────────────  │
│   <> Code   ⊙ Issues   ⇄ Pull requests   ...                    │
│   ─────────────────────────────────────────────────────────────  │
│   main  ▼            [5] N commits          [6] ▼ <> Code         │
│   ─────────────────────────────────────────────────────────────  │
│   [4] 📁 file tree                                                │
│       📄 README.md                                                │
│   ─────────────────────────────────────────────────────────────  │
│   [3] README.md (renders here on the front page)                 │
└─────────────────────────────────────────────────────────────────┘
```

| # | Element | What it tells you |
|---|---|---|
| 1 | **Organization** (`aws-dsu`) | Who owns this repo. `aws-dsu` is the GitHub organization hosting today's practice repo. |
| 2 | **Repository name** (`my-first-repo`) | The repo you will fork. Deliberately small and friendly. |
| 3 | **README** | Renders on the front page. This is where every project explains itself. |
| 4 | **File tree** | Every file in the repo. Click any folder to expand. |
| 5 | **Commits tab** | Every change ever made, with author and timestamp. This is what git **actually is**, made visible. |
| 6 | **Green Code button** | Holds the URL you will later use for `git clone`. Just notice it for now. |
| 7 | **Fork button** | Top-right. The one you click in five minutes. |

🟢 **Quick checklist** — find each on your screen:
- [ ] (1) `aws-dsu` in the breadcrumb
- [ ] (2) `my-first-repo` in the breadcrumb
- [ ] (3) README content on the front page
- [ ] (4) The file tree
- [ ] (5) The Commits tab (or commit count)
- [ ] (6) The green Code button
- [ ] (7) The Fork button in the top-right

💡 **Branches exist.** You do not need to use them today. We name them and move on.

---

## Part 3 · HANDS-ON #1 — Fork the repo (23–35 min)

> **Your turn. 12 minutes. By the end, everyone has a fork.**

### Recipe — Fork `aws-dsu/my-first-repo`

🟢 **Step 1.** Confirm you are signed in to github.com. Look for your avatar top-right.

⚠️ **If you do not see your avatar:** the Fork button will be greyed out. Sign in first, then come back.

🟢 **Step 2.** Navigate to **https://github.com/aws-dsu/my-first-repo**

👀 **You should see** the same page the instructor just toured — README, file tree, Code button, Fork button.

🟢 **Step 3.** Click the **Fork** button in the top-right corner of the repo page.

👀 **You should see** a page titled "Create a new fork" with `aws-dsu/my-first-repo` listed as the source.

🟢 **Step 4.** Leave every option at its default. Click the green **Create fork** button at the bottom.

👀 **You should see** a brief "Forking…" animation, then land on a new repo page.

🟢 **Step 5.** Look at the URL in your browser's address bar.

### ✅ Success check — Before vs. After

```
BEFORE:    github.com/  aws-dsu       /my-first-repo
                        ───────
                        organization

AFTER:     github.com/  <your-username>  /my-first-repo
                        ──────────────
                        YOU
```

👀 **You should see** your username (not `aws-dsu`) in the URL. Under the repo title, you will also see a small line like:
> **forked from aws-dsu/my-first-repo**

🟢 **Step 6.** Copy your fork's URL from the address bar. Paste it into the workshop chat as a check-in.

⚠️ **Inline troubleshooting:**

| Problem | Fix |
|---|---|
| Fork button is greyed out or missing | You are not signed in. Sign in at github.com and try again. |
| You clicked Fork but nothing happened | Refresh the page. If still nothing, sign out and sign back in. |
| The URL still says `aws-dsu` | You did not complete the fork. Go back to the original repo and click Fork again. |
| You got an error about an existing fork | You already forked this repo (perhaps in pre-work). Go to `github.com/<your-username>/my-first-repo` directly — you are already done. |
| Page is loading very slowly | GitHub may be congested with 600 of us forking at once. Wait 60 seconds and refresh. |

💡 **Why this matters:** Your username in the URL is the marker of ownership. Anything you change now changes **only your copy**. The original `aws-dsu/my-first-repo` is untouched.

---

## Part 4 · HANDS-ON #2 — Edit & commit (35–48 min)

> **Your turn. 13 minutes. Make your first commit.**

You should currently be on **your fork's** page: `github.com/<your-username>/my-first-repo`.

### Recipe — Edit a file, commit the change

🟢 **Step 1.** On your fork's front page, click the **README.md** file in the file tree.

👀 **You should see** the README open in "view" mode, with its rendered content.

🟢 **Step 2.** Click the **pencil icon** (✏️) in the top-right of the file view.

👀 **You should see** the README open in "edit" mode — a text editor with the file's contents, line numbers down the left side, and an **Edit / Preview** toggle at the top.

⚠️ **If you do not see the pencil icon:** check your URL. If it says `aws-dsu/my-first-repo`, you are still on the original. The pencil only appears on repos you own. Go back to **your fork** (URL contains your username) and try again.

🟢 **Step 3.** At the very **top** of the file, add a new line. Type exactly:

```
# My PartyRock app ideas
```

You can add it above whatever is already there. Press **Enter** to push the existing content down a line.

🟢 **Step 4.** Scroll to the bottom of the page. You will see a section titled **Commit changes**.

🟢 **Step 5.** In the **Commit message** box (the first text field), type:

```
my first commit
```

Leave the optional description box empty.

🟢 **Step 6.** Confirm that **"Commit directly to the `main` branch"** is selected (it is the default).

🟢 **Step 7.** Click the green **Commit changes** button.

👀 **You should see** the page jump back to a file view or repo view, with your new line at the top of the README.

### ✅ Success check — Find your commit in history

🟢 **Step 8.** Click the **Commits** tab (or the commit count link near the top of the file tree).

👀 **You should see** a list of commits with the **newest at the top**. The newest one should show:

| Field | What you should see |
|---|---|
| Author | Your GitHub username and avatar |
| Message | `my first commit` |
| Timestamp | "a few seconds ago" or similar |
| Commit SHA | A short hash like `a1b2c3d` |

💡 **That is what git actually is — made visible.** A permanent record of who changed what, when, and why.

⚠️ **Inline troubleshooting:**

| Problem | Fix |
|---|---|
| I cannot find the pencil icon | You are on the original `aws-dsu` repo, not your fork. Check the URL contains your username. |
| The commit button is greyed out | You did not change the file content. Make sure you actually typed the new line, then it will activate. |
| I clicked away and lost my edit | The edit is gone. Click the pencil icon again and re-do it. |
| My commit is not showing on the Commits tab | Refresh the page. If still missing, you may have clicked away before clicking **Commit changes** — re-do the edit. |
| I accidentally committed to the wrong branch | Today everyone commits to `main`. If you see a different branch, that is fine for now — your commit still exists. |
| I see "This file has been edited by someone else" | Unlikely on your fork. If it happens, click **Use this version** and re-commit. |

### 🎯 Drop in chat (check-in for moderators)

Paste this line into the workshop chat:

> ✅ First commit done — `<paste your fork URL here>`

---

## Part 5 · BONUS — github.dev (48–55 min) — Optional

> **If you are behind, skip this section.** The exit ticket only requires Parts 3 and 4.

`github.dev` is a full code editor that runs in a browser tab — the same one you use right now. No install. No download. No terminal.

### The trick

🟢 **Step 1.** Make sure you are on your fork's page: `github.com/<your-username>/my-first-repo`.

🟢 **Step 2.** Press the **period key** (`.`) on your keyboard.

👀 **You should see** the URL change from `github.com/...` to `github.dev/...`, and a VS Code-style editor open in the same tab.

⚠️ **If pressing `.` does nothing:**
- Click somewhere on the GitHub page first (not in the URL bar) so the page has keyboard focus.
- Some keyboards require **Shift + .** — try that.
- Or navigate directly to: `https://github.dev/<your-username>/my-first-repo`

### What just opened

```
┌──────────────────────────────────────────────────────────────┐
│  ☰  EXPLORER         │                                       │
│  📁 my-first-repo     │      (file content opens here when    │
│    📄 README.md       │       you click a file on the left)   │
│                       │                                       │
│  [⎘] [🔍] [⎇] [▶]    │                                       │
│   ↑    ↑   ↑   ↑     │                                       │
│  Files Find Source   │                                       │
│             Control  │                                       │
└──────────────────────────────────────────────────────────────┘
```

| Icon | What it does |
|---|---|
| **Explorer** (top-left) | The file tree, same as a desktop IDE |
| **Source Control** (third icon down, looks like a branch) | Stage, commit, and sync — where you save changes |
| **Editor area** | Click any file in the tree to open it. Drag a tab to split view side-by-side. |

### Make a second commit from github.dev

🟢 **Step 1.** Click **README.md** in the Explorer panel on the left.

🟢 **Step 2.** Make any small change — add a line, fix a typo, add a second heading.

🟢 **Step 3.** Click the **Source Control** icon (third icon on the left sidebar, looks like a branching line).

👀 **You should see** your changed file listed under "Changes".

🟢 **Step 4.** Hover over the file under "Changes" and click the **`+`** to stage it.

🟢 **Step 5.** Type a commit message at the top — something like `second commit from github.dev`.

🟢 **Step 6.** Click the **✓ Commit** button (the checkmark above the message box).

🟢 **Step 7.** Click the **🔄 Sync Changes** button when it appears.

🟢 **Step 8.** Switch back to your `github.com/<your-username>/my-first-repo` tab and refresh.

👀 **You should see** your second commit on the Commits tab.

💡 **Why this matters:** Many faculty use `github.dev` for course-prep editing even when they have a local setup. It is the fastest way to make small changes without leaving the browser — and you have it now.

---

## Part 6 · Preview & wrap (55–60 min)

### What comes next — the SageMaker preview

In your first AWS Workshop Studio lab, you will run this command in a terminal:

```bash
git clone https://github.com/aws-samples/aws-mlu-eep-generative-ai.git
```

That is the **same FEC muscle**, applied to the actual AWS course repository.

- `git clone` is the terminal equivalent of the Fork button — it copies the repo into your Studio environment.
- The same `edit` → `commit` loop applies, just typed instead of clicked.
- **You do not need to do this today.** Workshop Studio will provide the terminal in your lab session.

### Three rules of public-repo hygiene

Before you make your next commit:

> **1. Every commit is permanent.**
> Even if you delete a file later, the commit history still contains it. Treat every commit as public the moment you click the button.
>
> **2. No identifiable student data, ever.**
> No names, no grades, no IEP/504 information, no accommodation records, nothing FERPA-protected.
>
> **3. No institutional secrets.**
> No internal budgets, personnel files, private policy drafts, or unpublished research data.

### Exit ticket — drop these in chat (or the follow-up form)

```
My fork URL is _______________________

The commit message on my first commit was _______________________

One thing I will use my fork for in my teaching is _______________________

One question I still have about git is _______________________
```

---

## After the session — Within 48 hours

Three small things to do before your first lab. Each takes under 5 minutes.

### 1. Bookmark your fork URL

You will need it in Workshop Studio. Save it somewhere you will actually find it again — browser bookmark, notes app, calendar event for your first lab.

### 2. Make a second commit

Any file, any change. The point is to reinforce the FEC loop while it is fresh.

Suggested edits (pick one):

| Discipline | Add this to your README |
|---|---|
| Humanities | A note: "What kind of generative-AI literacy could my students benefit from?" |
| STEM | A note about which MLU lab could anchor a lecture on prompt engineering or RAG. |
| Business | Which Module 3 application pattern (chatbot, agent, RAG) maps to a course you teach. |
| Health professions | Which responsible-AI lab (Module 2) connects to your existing ethics curriculum. |
| Education | How you might remix the MLU labs for a teacher-preparation course. |
| Social sciences | A policy or data-ethics question the responsible-AI module raises for your field. |

### 3. Join the async help channel

Post one question — even a small one. The channel is open for 72 hours after the session.

---

## Appendix A · Troubleshooting Quick Reference

| If you see / experience… | Do this |
|---|---|
| "I do not have a GitHub account." | Create one at github.com/signup. You will miss the live hands-on — use the recording and office hours to catch up. |
| Fork button is greyed out or missing. | You are not signed in. Sign in at github.com and try again. |
| You clicked Fork but nothing happened. | Refresh, sign out, sign back in. GitHub may also be congested — wait 60 seconds and retry. |
| You cannot find the pencil icon. | You are looking at the original `aws-dsu/my-first-repo`, not your fork. The pencil only appears on repositories **you** can write to. Check the URL contains your username. |
| Commit button is greyed out. | You did not change the file content. Type something into the editor and it activates. |
| Your commit is not showing up. | Confirm you clicked **Commit changes** at the bottom of the edit screen (not just navigated away). Refresh the Commits tab. |
| Pressing the period key does nothing. | Click on the GitHub page first so it has keyboard focus. Some keyboards need **Shift + .** Or navigate directly to `github.dev/<your-username>/my-first-repo`. |
| "Is what I commit visible to everyone?" | Yes, if the fork is public (the default). Apply public-repo hygiene. To make it private: **Settings → General → Danger Zone → Change visibility**. |
| "Will this cost me money?" | No. GitHub free accounts include unlimited public repos, unlimited private repos, and unlimited `github.dev`. |
| "Do I need to install anything?" | Not for today. Workshop Studio will provide SageMaker Studio with git already installed — no install needed there either. |
| You accidentally edited the wrong file. | Click the **History** of the file (clock icon) and revert, or just commit a follow-up that re-fixes it. Nothing is ever truly lost. |
| You forked into the wrong account (personal vs. organization). | Delete the wrong fork in **Settings → General → Danger Zone → Delete this repository**, then fork again into the right account. |

---

## Appendix B · Reusable Git Cheat Sheet

### The four-verb loop

| Verb | What it does | Browser equivalent (today) | Terminal command (later) |
|---|---|---|---|
| **clone** | Copy a repository to your environment | Fork (creates a copy on GitHub) | `git clone <URL>` |
| **edit** | Change one or more files | Pencil icon, or github.dev | (any text editor) |
| **commit** | Save a labeled snapshot | **Commit changes** button | `git commit -m "message"` |
| **sync** | Push up or pull down changes | **Sync** button in github.dev | `git push` / `git pull` |

### Terminal commands you will see in SageMaker Studio

```bash
git clone <URL>            # Copy a repository to your environment.
git pull                   # Get the latest changes from GitHub.
git status                 # See which files have changed.
git add <file>             # Stage a file to be included in the next commit.
git commit -m "message"    # Save a labeled snapshot.
git push                   # Send your commits up to GitHub.
```

### The three rules of public-repo hygiene

1. **Treat every commit as permanent and public.** Even if you delete a file later, the commit history still contains it.
2. **No identifiable student data, ever.** No names, no grades, no IEP/504 info, no accommodation records, no FERPA-protected content.
3. **No institutional secrets.** No internal budgets, personnel files, private policy drafts, or unpublished research data.

### Three things to do after the session

1. Bookmark your fork URL.
2. Make a second commit — anywhere, any file — to reinforce the loop.
3. Join the async help channel and ask one question.

---

## Appendix C · FEC-to-GitHub Worksheet

Fill this in during or after the session. This is the artifact you bring to your first Workshop Studio lab.

| Planning item | Question | Your notes |
|---|---|---|
| GitHub account | What is your GitHub username? | |
| Account email | What email is associated with your account? | |
| Fork URL | What is the full URL of your fork of `aws-dsu/my-first-repo`? | |
| First commit message | What did you write as your first commit message? | |
| **F — Fork** | When did you fork the practice repo (date)? | |
| **E — Edit** | Which file did you edit, and what did you change? | |
| **C — Commit** | What does the Commits tab show for your fork? | |
| Privacy check | Is your fork public or private? Are you comfortable with that setting? | |
| Course connection | Which course of yours could most benefit from a forked copy of the MLU labs? | |
| github.dev tried? | Did you press `.` and open github.dev? Will you use it for course prep? | |
| Next step | What is the first thing you will do in your fork after the workshop sessions begin? | |
| Open question | What is one thing about git that still feels unclear? | |

---

## That's the whole loop

**Fork.**
**Edit.**
**Commit.**

See you in the lab.
