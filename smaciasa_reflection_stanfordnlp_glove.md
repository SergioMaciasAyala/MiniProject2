# Reflection: stanfordnlp_glove

## Inactivity pattern
GloVe has the most stars of all my projects (7230) but very few commits (263). It has 11 gaps which is the most. The longest gap is 13 months from October 2023 to October 2024. It got a small amount of work regularly until 2020 and after that only a few commits a year.

## Was the gap easy or hard to read?
Medium. No message says why it stopped. But the commits before the gap were all small fixes sent in by outside people like a memory overflow fix for huge machines and an option to output context vectors. GloVe came out in 2014 so the original Stanford team had moved on. The repo only changed when someone sent a pull request. Also some of the commits in WoC are GitHub's test merges for pull requests that were never actually merged (like the ones from Erin George). That makes the project look a bit more active than it really was.

## Likely reason for the gap and recovery
I think it went quiet because nobody was in charge of it. It came back for two reasons. First NumPy 2.0 came out in 2024 and removed np.Inf which broke the evaluation script. People sent fixes for that in November 2024 and July 2025. Second Stanford trained new 2024 GloVe vectors. In July 2025 rlyCarlson (who has a Stanford email) updated the docs and linked the new vectors. The README now has a "NEW 2024 VECTORS" section. Half of the people after the gap were new (leo9827 and Jesper Olsen) and the original authors did not come back.

## Summary
GloVe is famous (7230 stars) but gets very few commits and has 11 gaps. The 13 month gap in 2023 and 2024 happened because nobody was maintaining it and changes only came from outside pull requests. It came back in 2024 and 2025 because NumPy 2.0 broke a script and because Stanford released new 2024 vectors.
