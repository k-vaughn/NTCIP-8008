<!-- markdownlint-enable require-heading-body -->
<div class="section-2" markdown="1">
<style>
  .section-2 { counter-set: section 2; }
</style>

# Overview {.body}

Managing an open-source project involves four major activities as described in
the following clauses:

1. Establishing the project
2. Processing comments
3. Processing contributions
4. Approving releases

## Establishing the Project {.body}

Figure 1 provides an overview of the process to establish a new open-source project.

```mermaid
%%{init: { 'sequence': { 'mirrorActors': false } }}%%
sequenceDiagram
  participant Proposer
  participant Committee
  participant WG as Working Group
  participant Maintainer
  participant Repo as Open-Source Project Repository

  Proposer ->> Committee: Propose project
  Committee ->> WG: Establish WG
  Committee ->> Maintainer: Assign maintainer
  Maintainer ->> Repo: Establish public repository
  Maintainer ->> Repo: Upload initial baseline
  Maintainer ->> WG: Suggest project plan
  WG -->> Maintainer: feedback
  Maintainer ->> Repo: Post project plan
  Maintainer ->> Repo: Create appropriate branches for work
```

When someone identifies a need for a new shared resource (e.g., industry
standard, reusable code, etc.) within ITS, they can develop a proposal and
submit it to an appropriate committee. The
proposal can be relatively simple (e.g., a statement of goals and structure) or
a complete prototype.

If the proposal is accepted by the committee, the committee will assign a working group and one or more
maintainers who will become responsible for leading the project. This will often
include the individual proposing the project. The maintainer will establish the
open-source project repository on the standards development organization's
open-source website (e.g., GitHub account) and upload the initial project files.

!!! question "Needs Review"
    !!! note
        The maintainer is a key role in the project. If the maintainer is not available for any reason, it can delay the triage of identified issues. It is the responsibility of the committee to ensure that the maintainer either has sufficient resources or has sufficient backup to provide a high degree of confidence that there is not an articicial bottleneck when contributors wish to address problems.

Once the initial upload is provided, the maintainer will work with the working
group to refine the vision for the project and establish the set of baseline
issues as a part of the project plan. The project plan will also define the
planned release schedule, which can be based on a calendar schedule, reaching
milestones, or achieving other metrics. Members of the WG are encouraged to
submit their issues directly so that the originator can be properly captured and
to encourage WG members to become familiar with the process; however, the
Maintainer can submit comments on the behalf of others, if needed.

The Maintainer is also responsible for creating any necessary branches for developing draft materials. The "main" branch should always be restricted to formal releases. Working drafts and pre-releases should be contained within branches so that industry users do not accidentally look at a draft thinking that it is approved.

!!! question "Needs Review"
    We need to review this process with a GitHub expert to determine the best way for managaing the website (and PDF) rendered versions of the current release alongside drafts. In other words, deployments need ready access to the current version (and all previous versions) while WG members need access to the current draft. By default GitHub only allows one rendered version but we could:

    - Use separate repositories (e.g., NTCIP-8008 and NTCIP-8008-future)
    - Use subdirectories (e.g., docs for current and docs/future for draft)
    - Use a GitHub action to publish different branches to different subdirectories of the gh-pages branch
    - Use a GitHub action to publish different branches to different repositories, one for each published/draft branch

    All projects should likely use the same mechanism and the selection should be made in consultation with GitHub experts.

## Process comments {.body}

Figure 2 provides an overview of how comments are processed for an open-source
project.

```mermaid
%%{init: { 'sequence': { 'mirrorActors': false } }}%%
sequenceDiagram
  participant Commenter
  participant WG as Working Group
  participant Maintainer
  participant Repo as Open-Source Project Repository

  Proposer ->> Repo: Review materials
  Proposer ->> Repo: Submit comment
  Repo -->> Maintainer: Notify
  Maintainer ->> WG: Seek guidance
  WG -->> Maintainer: Provide feedback
  Maintainer ->> Repo: Perform triage
```

Users of open-source projects often have questions, encounter bugs, request
features, or provide feedback on usability. Submitting comments is the primary
way for the community to help guide the development of the project. Comments can be submitted at any time.

When comments are submitted, maintainers (and other followers) are notified. If
the comment is submitted as an issue (as opposed to a discussion item), the
maintainer triages the issue by determing its relevance, classification (e.g.,
bug, documentation issue), and priority. If needed, the maintainer can discuss
the issue with the commentor or sponsoring WG to ensure consensus from the
broader community.

!!! question "Needs Review"
    Each project should identify its goals for triaging submitted issues. By default, projects should have a goal of triaging all comments within one month of their submittal, but the exact timeline might vary based on available resources, the criticality of the project, and other factors. If a submitted issue is not triaged within this timeline, the submitter should contact the parent standards development organization for guidance.

As a result of the review, the issue can be accepted, merged
with another issue, split into multiple issues, or rejected (e.g., if it does
not fit with the project's goals). Once the triage is complete, the maintainer
adds tags as appropriate to the issue so that it can properly be managed.

## Procss Contributions {.body}

Figure 3 provides an overview of processing contributions to an open-source project.

```mermaid
%%{init: { 'sequence': { 'mirrorActors': false } }}%%
sequenceDiagram
  participant WG as Working Group
  participant Maintainer
  participant Contributor
  participant Repo as Open-Source Project Repository

  Contributor ->> Repo: Review open issues
  Contributor ->> Repo: Claim issue
  Repo -->> Maintainer: Notify
  Contributor ->> Repo: Create copy
  Repo -->> Copy: Copy
  Contributor ->> Copy: Make edits
  Contributor ->> Repo: Submit pull request
  Repo -->> Maintainer: Notify
  Maintainer ->> Copy: Review
  Maintainer ->> WG: Optionally coordinate
  WG -->> Maintainer: Feedback
  alt if acceptable
    Maintainer ->> Copy: Merge
    Copy -->> Repo: Merge
  end
```

Open-source projects encourage contributions from the community, allowing others
to solve issues or implement features. Contributors gain experience and
recognition, while the project benefits from a broader range of solutions.

Interested contributors browse the list of open issues, claim one they are
interested in, and start working on a solution. When they have develped and
tested their proposed solution, they submit a request for the maintainer to
"pull" a copy of their changes from their site. This is known as a pull request
(PR).

When a PR is submitted, the maintainer is automatically notified and is
responsible for reviewing the request to ensure that it:

- can be safely merged with the project without overwriting other changes,
- solves the stated problem without introducing bugs, and
- meets the project's guidelines (e.g., coding standards).

During the review process, the maintainer can communicate with the contributor
if questions arise or with the WG to ensure consensus on the details of the
proposed change. If the process identifies any issues with the proposed change,
it can be returned to the contributor to make additional revisions. If the
changes are deemed to be satisfactory, the maintainer can accept the pull
request and the changes will be merged into the open-source project.

## Approve Releases {.body}

Figure 4 provides an overview of the process to approve a new release of an
open-source project.

```mermaid
%%{init: { 'sequence': { 'mirrorActors': false } }}%%
sequenceDiagram
  participant AG as Approval Group
  participant Maintainer
  participant Repo as Open-Source Project Repository

  Maintainer ->> AG: Suggest release (suggested release number)
  AG ->> Repo: Review materials
  AG -->> AG: Vote
  AG -->> Maintainer: Report results
  alt if approved
    Maintainer ->> Repo: Tag as identified release number
  else
    Maintainer ->> Repo: Address identified issues
  end
```

Releasing a project allows users to access a stable, tested version with new
features, bug fixes, or improvements. It also provides a versioned snapshot that
is easier to manage and distribute.

Once all expected changes have been made to fulfil a defined stage in the
project plan, the maintainer will follow the project's defined process for
obtaining approval of the current draft as a formal release (e.g., v01.01.03)
from the identified approval group (e.g., perhaps selected experts for a patch, the WG for a new feature, or the parent committee for non-backwards compatible changes). The exact approval group is defined in the project's plan.

If approval is received, the maintainer:

- documents changes in release notes (if not already included);
- if it is a full release, moves the version to the main branch;
- tags the current version as a new release (e.g., "v01.01.03"); and
- provides a downloadable archive.

If approval is not received, the maintainer ensures that all of the identified issues are properly recorded on the issues page and continues the process of addressing issues through contributions.

This collaborative process allows open-source projects to evolve through
contributions from users and developers worldwide, promoting continuous
improvement while ensuring transparency and accountability.

</div>
