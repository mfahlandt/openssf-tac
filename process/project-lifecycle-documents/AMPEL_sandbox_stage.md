## Application for creating a new project at Sandbox stage

### List of project maintainers

The project must have a minimum of three maintainers with a minimum
of two different organizational affiliations.

AMPEL currently has the following maintainers:

* Adolfo García Veytia, Carabiner Systems, @puerco
* Gabriel de Obieta, Upwork, @deobieta
* Carlos Panato, Chainguard, @cpanato

Adolfo García Veytia (@puerco) is the main developer of the project. Although
they are not checking in code, Gabriel and Carlos help the project
with non-code contributions, especially maintaining the relevant
repos but, more importantly, they help us ensure admin access is
granted to more than one maintainer to help the project's bus factor.

In addition to the core maintainers, the project has also received
minor contributions from other individuals across its repositories
including @arewm @InvariantSystems @qduanmu @knrc @ralphbean @staceypotter
@TomHennen @trumant.

### AMPEL Ecosystem

The project is currently hosted in the Carabiner Systems organization
where it was originally developed. The donation plan includes migrating
AMPEL and the other repositories to a new organization: github.com/policylabs.
This organization will be the final home of AMPEL and will go under the
OpenSSF/LF control.

In addition to the main AMPEL repository, the project depends on and
is developed alongside supporting repositories in the same ecosystem,
especially:

* `carabiner-dev/policies` - community policy library
* `carabiner-dev/collector` — attestation retrieval and parsing library used by AMPEL
* `carabiner-dev/attestation` — attestation framework
* `carabiner-dev/policy` - policy compiler
* `carabiner-dev/signer` - signer library, provides key management, identity and more

### Sponsor

Most projects will report to an existing OpenSSF Working Group, although in
some cases a project may report directly to the TAC. The project commits to
providing quarterly updates on progress to the group they report to.

* Supply Chain Integrity WG

### Mission of the project

AMPEL is a supply chain policy engine designed to be embedded across the
software development lifecycle to verify whether source code, build
environments, dependencies, and released artifacts can be trusted based
on signed, unforgeable metadata captured in attestations.

The project’s mission is to make supply chain security assertions
practical, composable, and automatable. AMPEL lets developers, security
teams, auditors, and downstream consumers express policies over software
supply chain evidence and continuously verify those policies in local
workflows, CI/CD systems, and other automation.

AMPEL is aligned with the OpenSSF mission because it helps secure the
development, maintenance, and consumption of open source software through
verifiable policy enforcement. It addresses an important gap in the
ecosystem: many projects produce security metadata such as SLSA provenance,
SBOMs, vulnerability scan outputs, and other attestations, but
organizations still need a portable engine to evaluate that evidence
consistently and map the results to security requirements and compliance
controls.

AMPEL is intentionally designed to complement, not replace, other OpenSSF
and adjacent ecosystem efforts. It consumes existing attestation formats
such as in-toto, supports Sigstore bundles for signature verification,
works with common supply chain evidence such as SLSA provenance and SBOMs,
and can evaluate custom JSON-based evidence. It also supports transformers
that normalize data into common forms to simplify policy authoring, currently shipping with an OpenVEX transformer and Protobom modules built in.

A distinguishing goal of the project is to let policies link directly to
controls in security frameworks and catalogs (like the OSPS Baseline),
including OSCAL catalogs and profiles, so that cryptographically verifiable
evidence can be evaluated as reusable checks for framework conformance. AMPEL
can also attest its own policy results, enabling downstream systems to rely
on verified evaluation outcomes instead of redoing the same checks repeatedly.

This makes AMPEL a novel and useful addition to the OpenSSF ecosystem: it
focuses on portable, attestable policy evaluation across the supply chain,
bridging producers of security metadata with the enforcement, reporting,
and compliance workflows that consume it.

The project is applying for Sandbox because it has been under development and
testing for over a year, it has a mature codebase with releases, CI
integrations, and ecosystem components. It is starting to roll into major Open
Source projects in the OpenSSF and other foundations. But AMPEL needs the OpenSSF
to thrive: it would benefit from the collaboration, governance maturity,
broader community participation, and alignment with related projects and
working groups as it grows. Not to mention setting it free from a single
organization's control to pursue its mission.

### IP policy and licensing due diligence

When contributing an existing Project to the OpenSSF, the contribution
must undergo license and IP due diligence by the Linux Foundation (LF).

* Yes: due diligence issue to be opened / linked here: TBD

AMPEL is released under the Apache License 2.0.

### Project References

The project should provide a list of existing resources with links to the
repository, and if available, website, a roadmap, contributing guide, demos
and walkthroughs, and any other material to showcase the existing breadth,
maturity, and direction of the project.

| Reference | URL |
|---------------------|-----|
| Main Repository | https://github.com/carabiner-dev/ampel |
| Supporting Repo: Collector | https://github.com/carabiner-dev/collector |
| Supporting Repo: Attestation Framework | https://github.com/carabiner-dev/attestation |
| Supporting Repo: Signer Library | https://github.com/carabiner-dev/signer |
| Supporting Repo: Actions | https://github.com/carabiner-dev/actions |
| Supporting Repo: Policy Compiler | https://github.com/carabiner-dev/policy |
| Supporting Repo: Community Policy Library | https://github.com/carabiner-dev/policies |
| Contributing guide | https://github.com/carabiner-dev/ampel/blob/main/CONTRIBUTING.md |
| Security.md | https://github.com/carabiner-dev/ampel/blob/main/SECURITY.md |
| Releases | https://github.com/carabiner-dev/ampel/releases |
| Demos | Presentations: [Builds You (and Others) Can Trust: Meet the AMPEL Policy Engine](https://www.youtube.com/watch?v=ERXgZNLHnpA&list=PL2KXbZ9-EY9Qvfxh3i9YtiGLqNFHId1qM&index=25) [Unforgeable Baseline Compliance](https://www.youtube.com/watch?v=_Na_R1IY-5c&t=11s&pp=ygUWYWRvbGZvIGdhcmNpYSBiYXNlbGluZQ%3D%3D) [KubeCon NA 2025 Keynote](https://www.youtube.com/watch?v=OdGxWBK8Jpc&pp=ygUWYWRvbGZvIGdhcmNpYSBiYXNlbGluZQ%3D%3D) [How Hot Can Your SLSA Be?](https://www.youtube.com/watch?v=mwfSXuIGxBw) [Securing AI Pipelines End-To-End](https://www.youtube.com/watch?v=yvLZTYp5BeI&list=PLVl2hFL_zAh_nTZ19ucfezDcXN0wYU3yV&index=2) [Building an E2E SLSA Implementation](https://www.youtube.com/watch?v=AtnWCob8M1E&list=PLVl2hFL_zAh_nTZ19ucfezDcXN0wYU3yV&index=5) |
| Other | AMPEL supports in-toto attestations, Sigstore bundle and key verification, policy-to-OSCAL control mappings, and attestable policy results as VSAs and SVRs. |
