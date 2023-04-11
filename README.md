# onboarding-3

Create onboarding PR. Then modify the onboarding branch.

## Expectations: 
  - Fall back to git for modified/conflicted calculation
  - Invalidate cache when checking isOnboarded()
  - Invalidate Extract Cache
  - New PR body which reflect the changes to config done in onboarding branch
  
## Observations:
  - Fall back to git for modified/conflicted calculation ✅
  - Use cache when checking isOnboarded() ✅
  - Invalidate Extract Cache ✅
  - New PR body which reflect the changes to config done in onboarding branch ✅

## Relevant logs:

*note: logs are from the run after onboarding branch was modified

```log
DEBUG: checkOnboarding() (repository=RahulGautamSingh-testing/onboarding-3)
DEBUG: isOnboarded() (repository=RahulGautamSingh-testing/onboarding-3)
DEBUG: Onboarding cache is valid. Repo is not onboarded (repository=RahulGautamSingh-testing/onboarding-3)
DEBUG: Repo is not onboarded (repository=RahulGautamSingh-testing/onboarding-3)
...
DEBUG: Onboarding PR already exists (repository=RahulGautamSingh-testing/onboarding-3)
DEBUG: Onboarding branch modified. Removing outdated extract cache for branch=main (repository=RahulGautamSingh-testing/onboarding-3)
DEBUG: isBranchConflicted(main, renovate/configure) (repository=RahulGautamSingh-testing/onboarding-3)
DEBUG: branch.isConflicted(): using git to calculate (repository=RahulGautamSingh-testing/onboarding-3)
... cloning & finding conflicted status ...
DEBUG: branch.isConflicted(): false (repository=RahulGautamSingh-testing/onboarding-3)
DEBUG: Merge onboarding branch in default branch (repository=RahulGautamSingh-testing/onboarding-3)
DEBUG: Update Onboarding Cache (repository=RahulGautamSingh-testing/onboarding-3)
       "onboardingCache": {
         "defaultBranchSha": "ffa89b0eeb4a29d7bde79009a58c152c73cbc3f8",
         "onboardingBranchSha": "655fcfea7de56ed5aebac9d7a165a90000fe2e07",
         "isConflicted": false
       }
...
DEBUG: extract() (repository=RahulGautamSingh-testing/onboarding-3) // no cache as we removed it 
...
DEBUG: Found open onboarding PR (repository=RahulGautamSingh-testing/onboarding-3)
DEBUG: updatePr(1, Configure Renovate, body) (repository=RahulGautamSingh-testing/onboarding-3)
DEBUG: PR updated...prNo: 1 (repository=RahulGautamSingh-testing/onboarding-3)
 INFO: Onboarding PR updated (repository=RahulGautamSingh-testing/onboarding-3)
       "pr": 1
```
