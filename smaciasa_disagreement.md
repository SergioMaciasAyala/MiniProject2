# Disagreements

**Parties:** smaciasa (validator) and cwolver1 / Chase (project owner). Chase reviewed and agreed to every resolution below.

I found 12 disagreements out of 50 checks. Here are four that show the main kinds of problems.

---

## 1. tdunning_t-digest: HasRecovered

- **Chase said:** Yes. It came back with docs updates and merge activity.
- **I said:** No.
- **Resolution:** No. *(I kept my value.)*

**Why:** After the 13-month gap there are 6 commits, but only one of them is real: a README link added on 2025-02-16. The other 5 look like "Merge 74996c7 into 7905f3d." They are GitHub's automatic test-merges for pull requests that were never merged. The same PR hashes show up before the gap too, just merged into a different base. The main branch on GitHub has had nothing since 2025-02-16.

**Takeaway:** "Merge <sha> into <sha>" commits make a project look busier than it is. We should filter them out before calling something recovered.

---

## 2. villano-lab_nrsicap: HasRecovered

- **Chase said:** Yes.
- **I said:** No, because it went quiet again after August 2024.
- **Resolution:** Yes. *(Chase's value kept.)*

**Why:** At first I counted it as not recovered because there's been nothing since 2024-08-15. But Kitty Harris was one of the main people on the project before the gap, with 170+ commits. She came back and worked on it over about 6 months in 2024. The field asks whether work started again after the gap, and it did. Whether the project is alive *now* is what Currentstatus is for, and it's already marked Inactive there.

I did push back on Chase's WhyRecovered text, though. It said "new analysis" and "documentation," but the commits are uploads of analysis and config files plus a Travis fix, with no docs changes. The proposed fix keeps his Yes and rewrites the reason, so that row is a Compromise.

**Takeaway:** I was mixing up "did it recover" with "is it still active." They are separate fields.

---

## 3. mourner_rbush: Currentstatus

- **Chase said:** Active, using a last commit date of 2026-04-03.
- **I said:** Inactive.
- **Resolution:** Inactive. *(I kept my value.)*

**Why:** The rule says to check for commits in the 6 months before 2025-09-30. On GitHub, rbush has a commit on 2024-09-24 and then nothing until 2025-11-22, so there were zero commits in that window. Chase used the newest date he saw, which is after the cutoff. rbush is active again today, and I noted that in the comments. Under the rule, though, it's Inactive.

**Takeaway:** Use the cutoff date in the rule, not today's date.

---

## 4. fabsig_gpboost: ActivityPattern

- **Chase said:** irregular.
- **I said:** rising.
- **Resolution:** steady. *(Compromise.)*

**Why:** The yearly commit counts are 123, 237, 155, 185, 331, and 225. Chase is right that it bounces around, and 2025 is lower than 2024, so "rising" is a stretch. But it never went more than one month without a commit, which doesn't feel random either. "Steady" fits a project that just keeps going at a decent pace.

**Takeaway:** The categories don't have exact rules. Looking at the yearly totals helped more than eyeballing the monthly plot.
