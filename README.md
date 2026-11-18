# Quiz #4 Review: Respiratory Care Study App

A one-page study app built from the Quiz #4 Review sheet and four lectures:

- Quiz 4 Review Sheet
- Oxygen Therapy
- Oxygen Delivery Devices
- Humidity & Aerosol Therapy
- Airway Clearance & Incentive Spirometry

It has three modes:

- **Notes:** each unit organized by topic. Includes a device cheat sheet (flow, FiO₂ and best use), the HME vs. heated passover table, and a lung volumes table. Yellow boxes point out where the slides and the review sheet disagree.
- **Flashcards:** 160 cards that you tap to flip. You can filter by unit and topic, shuffle, and keep a "Still learning" pile that your browser remembers.
- **Practice Quiz:** 76 multiple-choice questions in one pool, combining the review sheet, class practice and Jeopardy questions. Choose 10, 20, 40 or all of them. After each question you see an explanation, and at the end you get your score and a "Retry missed" button.

The whole app is a single `index.html` file, so there is nothing to install and no build step.

## Put it on GitHub Pages

1. Create a new repository on GitHub, for example `quiz4-review`.
2. Click **Add file → Upload files**, upload `index.html` (and this README if you want), then click **Commit changes**.
3. Go to **Settings → Pages**. Under **Build and deployment**, set **Source** to **Deploy from a branch**, pick **main** and **/ (root)**, and click **Save**.
4. After a minute or so, the site is live at `https://<your-username>.github.io/quiz4-review/`.

Or from the command line:

```bash
git init
git add index.html README.md
git commit -m "Quiz 4 review study app"
git branch -M main
git remote add origin https://github.com/<your-username>/quiz4-review.git
git push -u origin main
```

Then turn on Pages as described in step 3.

## Editing the content

All of the content is in the `UNITS` list at the top of the `<script>` in `index.html`. Each unit has three parts:

- `notes`: study notes, grouped by topic
- `cards`: flashcards, written as `[topic, front, back]`
- `quiz`: questions, written as `[question, correct answer, [three wrong answers], explanation]`

Add a line to any of these lists and it appears in the app. To add a new lecture, copy a whole unit block and give it a new `id`.

Anything marked **extra** isn't spelled out in the class materials, so check it against your notes.
