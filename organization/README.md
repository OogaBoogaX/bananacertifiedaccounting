# Organization profile

[profile-README.md](profile-README.md) is the authoritative source for Team Ooga Booga's public GitHub organization README.

**Status:** Proposed profile wording, not copied to the GitHub organization profile. Changes to that profile and repository metadata need separate authorization. **Checked:** October 17, 2026.

GitHub displays an organization's public profile from `profile/README.md` in a public repository named `.github`, here [OogaBoogaX/.github](https://github.com/OogaBoogaX/.github). A file in this accounting repository does not change the profile by itself. See [GitHub's organization profile instructions](https://docs.github.com/en/organizations/collaborating-with-groups-in-organizations/customizing-your-organizations-profile), checked October 17, 2026.

## Proposed profile and description decisions

List **Ooga Arcade** as a planned extraction with a placeholder repository, and **Oogatron** as existing tooling whose license needs clarification. This gives visitors an honest map of the public projects without presenting a placeholder as shipped software or implying unrestricted reuse of unlicensed work. Recheck these labels before publication. The [project history](../funding/project-history.md) contains the dated source evidence.

The published profile differs from this local source and omits both projects ([reviewed published copy](https://github.com/OogaBoogaX/.github/blob/e4f005fd7dc26069b232951da643bc593e4d0229/profile/README.md), October 17, 2026). The teaching mission, node launch, forthcoming bitcoin donations, and bitcoin treasury direction were supplied by the team on the same date; they are not claims of independently verified teaching outcomes or reconciled funds.

**Proposed repository description, exact text:**

> Funding plans and public financial records for Team Ooga Booga, plus planned general-purpose open-source accounting software anyone can use.

This replaces the member-focused wording with the public purpose while preserving the software intent. The software is Planned, not an existing application.

## Pending external updates

| Action | Exact preparation | Status |
| --- | --- | --- |
| Copy organization profile | After approval, copy the final local `organization/profile-README.md` unchanged to `profile/README.md` in `OogaBoogaX/.github` by pull request, then verify the public overview | **Needs authorization** |
| Change B.C.A. repository description | Set the GitHub About description to the exact text above | **Needs authorization** |
| Resolve Oogatron licensing | Audit rights and contribution terms, choose the license through the [licensing brief](../governance/licensing.md), then prepare a license change in that repository with appropriate consent | **Needs authorization** |

Before copying the profile, publish the approved B.C.A. documentation so its supporting project history is available. No repository metadata, profile, license in another repository, or donation service was changed in this review.

## Updating the profile

1. Approve [profile-README.md](profile-README.md) here through a pull request and record authorization for the external copy.
2. Review it against the checklist below.
3. After that pull request is merged, copy the content unchanged to `profile/README.md` in [OogaBoogaX/.github](https://github.com/OogaBoogaX/.github) through a pull request there.
4. Once that change is merged, confirm it appears on the [organization overview](https://github.com/OogaBoogaX).

There is no automatic synchronization, so keep both copies identical. To compare them from a local checkout of each repository (adjust the path to wherever your `.github` checkout lives):

```bash
diff organization/profile-README.md ../.github/profile/README.md
```

No output means the copies match.

## Review checklist

- [ ] Every project link opens the right repository, and each description matches that repository's README.
- [ ] Funding wording matches the [funding plan](../funding/README.md) status. Describe exploration as exploration, and do not mention a sponsor, tax deductibility, or donation instructions until the [decision log](../governance/decisions.md) records the arrangement.
- [ ] No figures appear that are not in the [budget](../finance/budget.md), and estimates are not presented as actual costs.
- [ ] The title emojis and motto lines are intentional.
