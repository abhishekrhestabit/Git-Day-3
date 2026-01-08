# Merge Conflict Postmortem

## What happened
Two developers modified the same line in `fruits.js` in parallel using separate clones.

## Evidence

###  Diverging commit history before merge
- ![SS1](images/ss1.png)

### Git reporting a merge conflict
- ![SS2](images/ss2_1.png)
- ![SS2](images/ss2-2.png)
- ![SS2](images/ss2_3.png)

### Merge commit after resolution
- ![SS3](images/ss3.png)

## Why the conflict occurred
Git could not automatically merge changes made to the same line.

## Resolution
Both changes were intentionally preserved by keeping both log statements.

## Lessons Learned
- Pull frequently to avoid large conflicts
- Avoid editing the same lines simultaneously
- Git requires human decisions when intent conflicts
