# Validation Reflection

Across both of our checks (100 records), Chase and I agreed on 81 before talking anything through. We disagreed more on his projects (12 of 50) than on mine (7 of 50). Currentstatus matched the most (90%, κ = 0.78) because it has a clear date rule. RecentThemes matched the least (70%), mostly because we counted merges and refactors differently. HasRecovered was 80% (κ = 0.65). "Did it recover" sounds simple, but neither of us had decided what counts as real activity, and most of the splits on Chase's projects came from that question.

## What comes before a long gap

The projects with the longest gaps were t-digest (13 months), nrSiCap (20 months), and rbush (8 months). Before their gaps, they had all already stopped adding features. The last 10 commits before each gap were mostly Dependabot bumps, README links, or a release getting wrapped up. nrSiCap is the clearest case: the last thing before its gap was the 2.1.0 release. Tensor2robot was the same, slowly winding down with logging and Python 2 cleanup. So the warning sign isn't a drop in commits. It's when the commits switch from "building stuff" to "keeping the lights on." byname is the one where a release came right before the gap and it still came back fine, so a release by itself doesn't mean the end.

## What makes a project come back

Three kinds of things restarted projects. The first is the main person coming back to finish something they started, like Allan Leal on autodiff, Luc Moreau on ProvToolbox, and oblonski on jsprit. The second is something outside breaking the code. byname came back to fix an R matrix class change, and RIFE came back because of a NumPy deprecation fix from an outside person. The third is bots: rbush basically restarted through Dependabot. Only the first kind led to a lot of new work afterward. Fixes and bot bumps kept things running, but they didn't really bring the project back to life.

## When a gap doesn't mean the project is dead

ProvToolbox had a 7-month gap in 2017–18 and then had its biggest year ever in 2023 with 529 commits. That's why we called it U-shaped. autodiff's gap happened only a few months after it started. byname goes quiet between releases almost every year. And rbush looks dead under the 2025-09-30 rule but is getting commits again in 2026. Small, finished libraries like rbush and t-digest don't need constant commits, so a gap there can just mean the library works and nobody needs to touch it.

## Mistakes we kept making

1. **Test-merge commits.** Commits like "Merge <sha> into <sha>" are GitHub test-merges for PRs that never got merged. They show up in the World of Code data but not on the main branch. They made t-digest and tensor2robot look recovered and padded the "Other" counts in RecentThemes. The fix is to check the GitHub main branch or filter these out.
2. **Mixing up fields.** I almost marked nrSiCap as not recovered just because it's dead now. Recovery is about what happened after the gap, and Currentstatus is about now.
3. **The wrong date.** The status rule is "as of 2025-09-30," not today. That one rule flipped rbush.
4. **Fuzzy categories.** "Irregular" was a catch-all, and refactors and merges both fall into "Other," which is easy to forget. Looking at yearly commit counts and counting every commit message one by one fixed most of these.

