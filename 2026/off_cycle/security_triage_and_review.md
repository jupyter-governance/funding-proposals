# Proposal: Part-Time Security Role for Jupyter

## Summary

This proposal requests funding for a 6-month pilot program to establish a
dedicated, part-time security role across the Jupyter ecosystem. The role would
cover approximately 4 hours per week (~100 hours total) focused on triaging
security reports, coordinating vulnerability disclosure, and implementing
straightforward fixes. The estimated budget is $8,000–$10,000 for the pilot
period at a rate of $80–$100/hour.

## Problem

Unlike with publicly available issues it is difficult to see the number of
security request that are handled in private, the volume of inbound security
reports has grown — and the project currently has no dedicated bandwidth to
handle them. The practical consequences:

- **Reports go unanswered for weeks or months.** Security reports submitted
  through GitHub security advisories and other channels sit in a queue with no
  one consistently responsible for initial triage and response.
- **Opened GHSAs stall without resolution.** Several GitHub Security Advisories
  have been created but lack follow-through — no patch, no CVE coordination, no
  public disclosure timeline.
- **Maintainer time is wasted on noise.** A growing share of inbound reports are
  AI-generated submissions of questionable accuracy, or outright spam unrelated
  to actual vulnerabilities. Filtering these from legitimate reports requires
  time and security judgment that volunteer maintainers shouldn't have to donate
  ad hoc.
- **No cross-project coordination.** Security issues may span multiple Jupyter
  subprojects (e.g., a vulnerability in Jupyter Server that affects JupyterHub
  deployments). There is no one whose job it is to coordinate across these
  boundaries.

This is not a reflection of maintainer negligence — it is a resourcing gap.
Security work is specialized, time-sensitive, and difficult to do well in
occasional spare moments.

## Time sensitivity

Some reports are forwarded via platforms (huntr.com as one of the example), and
are usually automatically published after a grace period with or without
response from maintainer, in 2026 the Jupyter Project had so far 8 reports
on huntr alone,
some of them actual vulnerabilities that have not yet receive proper review, nor
patches.

## Proposed Solution

Fund a part-time security contributor to work approximately **half a day per
week (4 hours)** for an initial **6-month pilot**, starting as soon as the
proposal is approved and logistics are in place.

### In Scope

- **Triage incoming security reports** across all Jupyter subprojects. Assess
  validity, severity, and affected components. Filter out spam and low-quality
  AI-generated submissions.
- **Respond to reporters** with timely acknowledgment and status updates.
- **Handle the move to GHSA (GitHub security Advisories) if relevant** this
  requires someone with security access to all repos of all the Jupyter orgs.
- **Create tools** to view GHSA across all Jupyter Orgs and repos; as it is
  currently cumbersome and difficult.
- **Coordinate vulnerability disclosure and CVE publication.** Work with
  subproject maintainers to agree on disclosure timelines, draft advisories, and
  request CVE identifiers, and make sure there are actual progress.
- **Implement simple fixes** when the vulnerability and patch are
  straightforward enough to not require deep subproject-specific knowledge —
  reducing the burden on maintainers to a review-and-merge step.

### Out of Scope (for this pilot)

- Large-scale security audits or architecture reviews
- Developing new security policies or frameworks
- Complex fixes requiring deep involvement from subproject maintainers
- Dependency auditing across all repositories (could be a future expansion)

While out of scope if times permit, more security related work could be done by the contributor.

### Possible Extension: Trademark Review

Jason Grout has suggested that this role could also absorb a few hours of
trademark committee work — specifically, reviewing and triaging requests for
authorized usage of the Jupyter trademark. This is another area of low-intensity
but consistent governance work that currently lacks dedicated bandwidth.
Bundling it with the security role would be a natural fit: both involve triage,
cross-project awareness, and regular lightweight attention rather than deep
project-specific work. We'd welcome the council's input on whether to include
this from the start or add it later; and would depend on the willingness of
candidate.

## Candidates

Note that unlike for other proposal like developers in residence this requires
giving wide permissions scope to a single individual across Jupyter – the role
of security manager exists with limited permission access at the GitHub
enterprise level and would mostly be sufficient, but give read access to all
existing Jupyter Organisations and Repositories

**Yann Pellegrini** is a recent contributor who has been actively working on
Jupyter security triage under mentorship and is available to take on this role.
He is already familiar with the workflows involved and could hit the ground
running, and work in the same coworking space as M. Bussonnier.

M and Michał Krassowski (Quansight) would remain available in an advisory
capacity — helping with context on specific subprojects, reviewing fixes, and
onboarding Yann where needed — but are unlikely to be the primary contractors
for a engagement of this size due to organizational overhead.

The role is also open to other qualified contributors if the council prefers.

## Budget

| Item | Estimate |
|---|---|
| Hours per week | ~4 |
| Duration | 6 months (~26 weeks) |
| Total hours | ~100 |
| Hourly rate | $80–$100 |
| **Total cost** | **$8,000–$10,000** |

### Funding Source

This proposal is submitted for consideration by the Jupyter Executive Council.
The specific funding mechanism — whether from existing Linux Foundation /
Jupyter project funds, a targeted sponsor, or another source — is a question for
the council. We are happy to work with whatever structure makes sense.

Before the move to Linux Software Fundation there used to be a NumFOCUS
Jupyter-Security dedicated fund, I do not know if it is still present, nor
wether it could be considered for this project.

## Success Metrics

At the end of the 6-month pilot, the council should be able to evaluate the
program against these concrete outcomes:

- **Response time:** All new security reports receive an initial triage response
  within 1 week (down from weeks/months today).
- **Backlog cleared:** The existing backlog of stalled GHSAs and unanswered
  reports is resolved — either patched, disclosed, or closed as invalid/spam.
- **Noise filtered:** AI-generated and spam reports are identified and closed
  promptly, freeing maintainers from this burden entirely.
- **Disclosure coordination:** Any confirmed vulnerabilities during the pilot
  period have a clear disclosure timeline communicated to reporters and followed
  through to CVE publication.
- **Transparency:** A brief monthly summary is shared with the Executive Council
  documenting volume of reports, resolution status, and any systemic issues
  identified.
- **Reporting** : activity reports to https://github.com/jupyter/cve/issues.

We do not include preventive security work in the success metrics of this
proposal as we believe triaging and responding to security issue should already
take most of the time, though we don't exclude improving the tooling as
practices as we work through existing issues.

## After the Pilot

At the 6-month mark, the council would evaluate whether to:

1. **Renew** the role at the same scope for another period.
2. **Expand** the role — for example, adding dependency auditing, security
   policy work, or increasing hours if the volume warrants it.
3. **Discontinue** if the volume of legitimate reports turns out to be low
   enough that ad hoc handling is sufficient.

The pilot is deliberately scoped to be low-cost and low-risk, while providing
concrete data to inform a longer-term decision about Jupyter's security
resourcing.

---

*Submitted by: [your name]*
*Date: [date]*
*Contact: [email]*

