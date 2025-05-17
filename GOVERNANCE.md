# Compat Table Governance

## Maintainers

The current maintainers are:
 
 - [@chicoxyzzy](https://github.com/chicoxyzzy)
 - [@kangax](https://github.com/kangax)
 - [@ljharb](https://github.com/ljharb)
 - [@webbedspace](https://github.com/webbedspace)
 - [@zloirock](https://github.com/zloirock)

To become a maintainer, an existing maintainer must privately nominate you to the other maintainers.
Within 2 weeks, if [a majority of maintainers have explicitly approved and zero maintainers have rejected the nomination](#decisions), it will pass.

### Inactivity

A maintainer who has not reviewed or commented on a PR in the past 6 months will be automatically moved to Emeritus status.
If a maintainer being moved to [emeritus](#emeritus) comments on the PR moving them, the PR should be moved to draft status for 2 weeks.
If after that time, they have reviewed or commented on one or more PRs, the PR will be closed; otherwise it will be merged.

### Emeritus

This section is a list of maintainers that are no longer active: (Currently empty)

### Permissions

An active maintainer will have Write permissions, at a minimum.
An emeritus maintainer will have Triage permissions, so they remain in the github org and can easily have their permissions restored should they wish to return.

Admin permissions will remain reserved for a private subset of active maintainers.

## Decisions

Any decision requires a majority of maintainers to agree, and must have zero maintainer objections.
Objections may not be overridden unless a majority of maintainers believe the objection is not made in good faith.
Only votes of active maintainers (non-[emeritus](#emeritus)) are considered, both for determining “majority” and for agreement/objections.

## Test Results

Only results explicitly tested in the relevant implementation version (by a human or a vetted script) should exist in the data files.
No test result may be changed or removed unless a human has explicitly verified it to be incorrect, and attested to that in the PR.

## Pull Requests

Pull requests for changes require two maintainers’ approval (including the PR author, implicitly, if they are a maintainer) if it meets any of the following criteria:

  - Changes this governance document
  - Adds a new implementation
  - Removes an existing implementation
  - Creates significant layout or strutural changes
  - Alters or deviates from the criteria for a version being obsolete
  - Restoring a returning maintainer to active status

Other categories of changes may land with one maintainer’s approval.
The PR author *does not count*, unless 2 weeks have passed since the PR was posted.

Examples in this category:
  - Unbreaks CI or other infrastructure
  - Rerunning the build script (no data changes)
  - Adds new versions of an existing implementation
  - Updates version release dates or obsolete status
  - Moving a maintainer to inactive status

If there is any ambiguity about which bucket a PR falls into, assume it falls into the one with stricter requirements, and consider opening a PR to clarify this document to avoid discovered ambiguity.
