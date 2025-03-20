<!-- markdownlint-disable MD033 -->
<div style="text-align: center;">
  <img alt="NTCIP" src="images/NTCIP.jpg">
  <h1>NTCIP 8008 Intelligent Transportation Systems (ITS) Open-Source Development</h1>
  <strong>An open-source specification of the NTCIP Joint Committee</strong>
</div>
<!-- markdownlint-enable MD033 -->

## Important Links

- [Website for most recent version](https://ite-org.github.io/ITS-open-source/)
- [PDF of most recent version](https://ite-org.github.io/ITS-open-source/)
- [Previously released versions](https://www.github.com/ite-org/ITS-open-source/releases)
- [Discussion forum](https://ite-org.github.io/ITS-open-source/discussions)
- [Report an issue](https://ite-org.github.io/ITS-open-source/issues)
- [Report a security issue](SECURITY.md)
- [Requirements for making contributions](CONTRIBUTING.md)
- [Code of Conduct](CODE_OF_CONDUCT.md)
- [License](LICENSE.md), which references the [Creative Commons CC BY 4.0 License](https://creativecommons.org/licenses/by/4.0/).

![Creative Commons CC BY 4.0 License](https://i.creativecommons.org/l/by/4.0/88x31.png)

## Installation Instructions

This is a documentation-only project. The current version of the document is
available as a [website](https://ite-org.github.io/ITS-open-source/) or as a
[pdf file](https://ite-org.github.io/ITS-open-source/pdf) that can be
downloaded. Contributors will need to
[fork](https://ite-org.github.io/ITS-open-source/contributor-responsibilities/#fork-the-repository)
and [clone](https://ite-org.github.io/ITS-open-source/contributor-responsibilities/#clone-the-repository)
the repository and
[establish the development environment](https://ite-org.github.io/ITS-open-source/contributor-responsibilities/#install-software)
on their local machine so that they can ensure that their edits are rendered as
expected.

This project uses the following tools:

- Git
- GitHub
- MkDocs
- Material for MkDocs

The proess to install the local environment is defined in the
[documentation conventions](https://ite-org.github.io/ITS-open-source/)
of the [ITS Open-Source Process](https://ite-org.github.io/ITS-open-source/)
with no exceptions or extensions.

## Project Summary

### Access

This project is available at currently at [https://github.com/ite-org/NTCIP-8008/](https://github.com/ite-org/NTCIP-8008/).

### Overview

The ITS Open-Source Process defines the process to be used to maintain
open-source resources of the NTCIP Joint Committee. This specification itself
is proposed to be an open-source resource, which is maintained by the process
defined by the specification. Anyone who wishes to contribute to or maintain an
NTCIP open-source resource project should start by familiarizing themselves with
[this process](https://ite-org.github.io/ITS-open-source/).

This specification is adapted from the
[OpenSauced Introduction](https://github.com/open-sauced/intro) and tailored to
meet the needs of the ITS community. While a product of NTCIP, it is envisioned
to be used in open-source efforts beyond the NTCIP community and it can be
further tailored to meet the needs of each ITS open-source resource project.

### Project Plan

#### Overview

At their May 2024 meeting, the NTCIP Joint Committee identified a need to
develop an alternative development path that could be followed to speed
standards development with the recognition that this development path might
result in a less mature standard. This document focuses on the ITS Open-Source Process, which is designed to allow
  documents to be defined in an open-source environment. It is closely related to a revised NTCIP Standardization Process, which is expected to be documented in NTCIP 8001 to reflect an approval
  process that is faster than the traditional NTCIP ballot process (e.g., an experimental specification). An early draft of this revised standardization process is included as Section 6 of this document.

In general, it is envisioned that the open-source process lends itself to the
faster experimental specification; however, the open-source process could be
used to develop a document that was then approved through the traditional
approval process. Likewise, the traditional standards development process could
be used to create an experimental specification that is approved through a
simplified approval process. As a result, the single request from the Joint
Committee for a streamlined process resulted in these two parts.

#### Features

The first version of the document needs to define the responsibilities for
commentors, contributors, maintainers, and WGs. It should also provide a set of
documentation and coding conventions along with a sample template for a new
GitHub project with all necessary files for basic operations.

#### Priorities

The document can be developed in any order but is expected to be developed in
the order of the items mentioned in the features list.

#### Release Schedule

- June 2025 V0.01: Section 1, 2.1 and Annex A complete
- Aug 2025 V0.02:  Section 2.2 and 3 complete
- Oct 2025 v00.03: Section 2.3, 4, and Annex B complete
- Dec 2025 v00.04: Section 2.4 and 5 complete
- Feb 2026 v01.00: Complete Section 6 (approval process)
- Sometime: Coding conventions in Annex C

### Acknowledgements

This project is sponsored by the Base Standards and Profiles 2 Working Group
(BSP2 WG) of the National Transportation Communications Interface Protocols
(NTCIP) Joint Committee (JC), a joint standardization committee of the American
Association of State Highway Transportation Officials (AASHTO), the Institute of
Transportation Engineers (ITE), and the National Electrical Manufacturers
Association (NEMA). It has benefited from funding from the US Department of
Transportation (USDOT).

## 🤝 Open-Source Development

Within traditional standards development processes, stakeholder concerns are
reported as comments, primarily during defined stages of the project. Within an
open-source environment, concerns are documented as issues and can be submitted
at any time.

All updates to the project are initiated by a stakeholder first reporting an
issue. Issues can be as minor as reporting a typo or as major as suggesting a
new section or complete rewrite of the document. If you have identified an
issue, please submit it on our
[Issues](https://ite-org.github.io/ITS-open-source/issues) page.

When submitting an issue, the commenter is required to identify the type of
issue and then provide specific information for that issue. Issue types that are
applicable to this project include:

- **Bug report:** used to report an issue or inaccuracy in the documentation
- **Documentation enhancement:** used to suggest improvements to the project documentation
- **New requirement request:** used to propose a new requirement to be added to
  the documentation
- **Requirement modification request:** used to suggest a modification to an
  existing requirement

If you identify a security issue, please report it using our [security process](SECURITY.md).

As with comments in the traditional standards process, issues are reviewed and
prioritized prior to being addressed. In the traditional process, the initial
review is performed by the editor; within the open-source process, the review is
performed by the maintainer. Depending on the impact of the issue, the
maintainer can either prioritize the issue directly or might seek guidance from
the working group.

Once an issue has been prioritized, it is made available for anyone in the
open-source community to make a contribution to address the issue.
