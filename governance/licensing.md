# Licensing decision brief

**Status:** Proposed. License direction is **UNDECIDED**. The [current LICENSE](../LICENSE) remains unchanged; no repository has been relicensed by this brief.

**Sources checked:** October 17, 2026. Requirements below are the publishers' statements, not acceptance decisions for Team Ooga Booga.

## Recommendation

**Proposed:** adopt **0BSD** as the binding license for original work the team has authority to license, after a rights review and contributor consultation. Preserve the Ooga Booga text separately as a clearly labeled, nonbinding plain-language summary; the standard text controls. Obtain informed open-source licensing advice before migration, including on existing contributions, third-party material, and relevant jurisdictions. This recommendation does **not** assert that the custom license is legally equivalent to 0BSD, the Unlicense, or another license.

0BSD best balances our “No ask. No pay. No club.” intent with recognized license wording and no notice-retention condition. MIT-0 is a close alternative. Prefer Apache-2.0 instead if an express contributor patent grant matters more to the team than minimal conditions. Recognition should make future [accounting software](../software/README.md) easier to evaluate, but it does not guarantee a funder, adopter, or package registry will accept a project. GitHub's [licensing guide](https://opensource.guide/legal/) explains why custom terms can create downstream review work.

## What funders and hosts publish

All sources in this table were checked October 17, 2026. A recognized license addresses only one part of eligibility; see the [funding plan](../funding/README.md) for the other gates.

| Route | Published licensing requirement | Consequence for us | Official source |
| --- | --- | --- | --- |
| Software Freedom Conservancy | Software must be under licenses that are both OSI-approved and DFSG-free. Documentation has additional permitted Creative Commons options. | Custom wording is an obstacle. OSI approval alone does not establish the separate DFSG test or overall eligibility. | [Membership criteria](https://sfconservancy.org/projects/apply/) |
| OpenSats | Requires a proper open-source license; funded source and documents must be public and reusable, and educational material openly licensed. | Obtain clarity on the selected license and actual project scope before applying; broad intent in a custom text is not documented approval. | [Application criteria](https://opensats.org/apply), [grantee requirements](https://opensats.org/faq/grantee) |
| SPI | Its IP policy encourages good free-software licenses. The GPL-compatible requirement concerns software copyright **assigned to SPI**. | Do not turn that assignment policy into a blanket admission rule. Ask SPI whether our existing or proposed licensing is acceptable; no assignment is proposed here. | [IP resolution, section 3](https://www.spi-inc.org/corporate/resolutions/1998/1998-11-16.iwj.2/), [project HOWTO](https://www.spi-inc.org/projects/associated-project-howto/) |
| Open Source Collective | Requires clear open-source licensing and follows standards from OSI, FSF, Debian, Fedora, and OSHWA. | A standard license makes the application easier to assess; its list of standards is not a promise to accept every license or project. | [Eligibility requirements](https://docs.oscollective.org/interested-in-joining-osc/acceptance-criteria) |
| Claude for Open Source | Program terms section 2.3 requires maintaining or contributing to at least one project under an OSI-approved license. | Licensing can block an individual tool benefit too. Discretion on popularity criteria should not be assumed to waive this requirement. | [Program terms](https://www.anthropic.com/claude-for-oss-terms) |

## Options for the team

| Option | Benefit | Main trade-off |
| --- | --- | --- |
| Keep the custom license | No migration; keeps the current voice and stated intent. | Leaves interpretation and recognized-license eligibility unresolved. Do not claim OSI approval or standard-license equivalence. |
| Dual-license the same covered work under the custom text **OR** a standard license | Recipients can choose the standard grant while the original text remains a license. | Requires authority for both grants and precise scope/choice wording; adds maintenance and ambiguity with little benefit over a summary. A second file alone is not a complete dual-license declaration. |
| Adopt a standard binding license; preserve Ooga Booga as a summary | Clear terms for new contributors, tooling, funders, and adopters while preserving personality. | Needs an explicit decision, rights audit, and careful treatment of older and third-party work. **Recommended.** |

### Candidate licenses

Approval and descriptions below were checked against the linked official texts on October 17, 2026. These are comparisons of the published wording, not a legal opinion on this team's code.

| Candidate / SPDX identifier | OSI-approved? | Fit with our intent and main trade-off |
| --- | --- | --- |
| [Zero-Clause BSD / 0BSD](https://opensource.org/license/0bsd) | Yes | Permission without a fee or notice-retention condition; short warranty disclaimer. No express patent grant. Recommended simple copyright license. |
| [MIT No Attribution / MIT-0](https://opensource.org/license/mit-0) | Yes | Broad permissions including sublicensing and sale without MIT's notice-retention condition. No express patent grant. Close alternative to 0BSD. |
| [The Unlicense / Unlicense](https://opensource.org/license/unlicense) | Yes | Closest to the stated wish to relinquish ownership, including heirs, through a public-domain dedication and broad reuse wording. Public-domain treatment across jurisdictions deserves informed advice. |
| [MIT / MIT](https://opensource.org/license/mit) | Yes | Broad permissions, but copies or substantial portions must retain the copyright and permission notice. More obligation than the motto suggests. |
| [Apache License 2.0 / Apache-2.0](https://opensource.org/license/apache-2.0) | Yes | Express contributor patent grant with termination on specified patent litigation. Requires license/notice preservation and marking changes; more text and conditions. |
| [CC0 / CC0-1.0](https://spdx.org/licenses/CC0-1.0.html) | **No** | Public-domain waiver with a fallback license. Not a solution to an OSI-approved-software requirement: OSI says the application was withdrawn and flags the explicit exclusion of patent rights. See the [OSI FAQ](https://opensource.org/faq). |

OSI approval is not a finding that the custom license matches any of these, nor a certification of worldwide enforceability. For dependencies, assets, and documentation, preserve applicable third-party licenses even if our own original code uses 0BSD.

## Existing contributions and future contributions

**Proposed:** start a private rights inventory using commit history, imported sources, contributor agreements if any, and the [public project history](../funding/project-history.md). A GitHub contributor count is a starting point, not a list of all copyright holders. Employers, upstream authors, asset creators, and contributors no longer active may hold relevant rights; bot attribution alone does not settle provenance. GitHub's [guide to changing licenses](https://opensource.guide/legal/#what-if-i-want-to-change-the-license-of-my-project) distinguishes licensing new contributions from relicensing existing work.

For each covered component, document either the existing permission that supports the proposed distribution or the rights holder's informed consent. Because the current license is custom, do not infer unlimited relicensing authority, treat silence as consent, or assume a maintainer vote overrides other holders' rights. If permission is unavailable, preserve the applicable original terms and scope, omit the component, or arrange an independently created replacement after advice. Do not rewrite past release history or claim old downloads acquired new terms.

For future contributions, propose a short `CONTRIBUTING` notice stating the exact adopted license and requiring contributors to have the necessary rights. GitHub's [Terms of Service, D.6](https://docs.github.com/en/site-policy/github-terms/github-terms-of-service#6-contributions-under-repository-license) provide a default of contributions under the repository's license; they do not provide blanket consent to an unrelated future license. If provenance attestation is useful, consider the [Developer Certificate of Origin](https://developercertificate.org/), which is an origin certification, not copyright assignment or universal relicensing consent. Keep contribution paperwork proportionate.

## Proposed migration checklist

- [ ] Record the selected option, exact SPDX identifier, covered work, and authorization in the [decision log](decisions.md). This brief is not that decision.
- [ ] Inventory **every** OogaBoogaX repository and its code, documents, artwork, vendored dependencies, and release artifacts. Use the [dated project history](../funding/project-history.md); do not assume all repositories have identical licensing or rights holders. Include the unresolved Oogatron license noted in [pending external updates](../organization/README.md).
- [ ] Complete the rights/consent review above; keep private correspondence and employer information restricted. Publish only the necessary notices and a consent-status summary.
- [ ] Confirm the intended funder's requirements and obtain informed advice on the migration and any patent concerns.
- [ ] Once separately authorized for each repository, prepare a reviewable PR with the exact standard license, required retained notices, an explicitly nonbinding Ooga Booga summary, contribution terms, and accurate package metadata or SPDX headers. State any excluded components clearly.
- [ ] Check shipped archives, generated files, dependency notices, README wording, and GitHub license detection. Detection is a tooling check, not a legal review; GitHub describes its [limited license-matching method](https://docs.github.com/en/rest/licenses/licenses).
- [ ] Publish migration scope and effective release/date after approval. Update funder materials only after the applicable work is actually covered. Keep historical releases and permissions traceable.

No outside repository edits, contributor messages, license adoption, or applications are authorized by this proposal.
