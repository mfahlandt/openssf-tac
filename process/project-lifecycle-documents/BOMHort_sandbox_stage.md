# Application for BOMHort at Sandbox Stage

> **Note:** This project was formerly known as SeeBOM. It has been renamed to BOMHort to avoid confusion with BOM-type naming conventions (CBOM, XBOM, etc.) in the supply chain security ecosystem. The project mission, codebase, and team remain unchanged.

## Application for creating a new project at Sandbox stage

### List of project maintainers
The project has 2 maintainers across 1 organizations:

* Mario Fahlandt, Kubermatic, @mfahlandt
* Koray Oksay, Kubermatic, @koksay


### Sponsor

Supply Chain Integrity Working Group — BOMHort (formerly known as SeeBOM) was presented to the WG on June 3, 2026 and received their endorsement as a sandbox project sponsor. The project commits to providing quarterly updates on progress to the Supply Chain Integrity WG.

* [Supply Chain Integrity WG](https://github.com/ossf/wg-supply-chain-integrity)

### Mission of the project

BOMHort is a standalone, Kubernetes-native SBOM visualization and governance platform. It ingests SPDX and CycloneDX SBOMs from S3-compatible storage, detects vulnerabilities via the OSV API, enforces license compliance policies, and applies VEX statements — all presented through an interactive dashboard with analytics.

BOMHort addresses an unfulfilled need in the supply chain security ecosystem: the ability to **consume, visualize, and govern** large volumes of SBOMs at scale. While tools exist to generate SBOMs (Syft, Trivy) and to verify their integrity (SBOMit), there is no open source platform focused on operationalizing SBOM consumption — making thousands of SBOMs searchable, surfacing actionable vulnerability and license compliance insights, and enabling VEX-driven suppression of false positives at enterprise scale.

Specific goals include:

* Ingest and normalize SBOMs in both SPDX and CycloneDX formats from S3-compatible storage
* Provide interactive visualization and search across large SBOM inventories
* Detect known vulnerabilities by querying the OSV API against SBOM components
* Enforce configurable license compliance policies with pass/fail governance decisions
* Apply OpenVEX statements for vulnerability suppression and false positive management
* Deliver ClickHouse-powered analytics for trends, dependency graphs, and compliance reporting
* Deploy natively on Kubernetes via Helm charts with production-grade observability

BOMHort complements existing OpenSSF projects:

* Integrates [protobom](https://github.com/protobom/protobom) as an optional backend for extended SBOM format coverage, avoiding duplication of format parsing
* Enriches and creates a Single Plane of Glass for SPDX SBOMs for all CNCF projects (the [cncf/sbom](https://github.com/cncf/sbom) project, is the origin use case that motivated BOMHort)
* Consumes OSV vulnerability data and supports OpenVEX statements for vulnerability suppression

Differentiation from existing projects:

* **SBOMit** (OpenSSF Sandbox): Focuses on verifiable SBOMs using in-toto attestation. BOMHort focuses on consumption and governance. Complementary, not competing.
* **protobom** (OpenSSF Sandbox): Format translation layer. BOMHort uses protobom as an optional backend for format coverage. Complementary.
* **GUAC** (OpenSSF Incubating): Graph-based supply chain aggregation. BOMHort focuses on Kubernetes-native deployment, ClickHouse analytics, and license governance with policy enforcement — different architecture and primary use case.
* **Dependency-Track** (OWASP): Similar governance focus but Java-based, not Kubernetes-native, and lacks ClickHouse-scale analytics or native license policy enforcement.

Non-Goals:

* BOMHort does NOT generate SBOMs — that is the job of tools like Syft, Trivy, and mikebom
* BOMHort does NOT pick a winning SBOM format — it supports both SPDX and CycloneDX natively
* BOMHort does NOT replace vulnerability scanners — it consumes and visualizes vulnerability data from OSV


### Alignment with the OpenSSF MVVSR

The mission of BOMHort is aligned with the [Mission, Vision, Values, Strategy, and Roadmap (MVVSR)](https://openssf.org/about/) of the OpenSSF.

**Strategies:**

* **i) Catalyst for Change**: BOMHort provides open source tooling that enables organizations to operationalize SBOM consumption and governance at scale, driving practical adoption of supply chain transparency beyond SBOM generation.
* **ii) Educate and Empower the Modern Developer**: BOMHort offers a user-friendly platform that helps developers and security teams understand and manage their software supply chain risks through SBOM visualization, license compliance, and VEX-driven vulnerability management.
* **iii) Ecosystem Leader**: BOMHort is a Kubernetes-native, cloud-native platform that integrates with existing supply chain security standards (SPDX, CycloneDX, VEX, OSV) and OpenSSF projects (protobom), promoting interoperability and adoption.

**Pillars:**

* **i) Programs & Projects**: BOMHort is a technical tool that directly advances the operational use of SBOMs and vulnerability intelligence within the software supply chain.
* **ii) Education**: Through intuitive visualization, BOMHort makes SBOM data accessible to developers, security analysts, and compliance teams — not just SBOM experts.

### IP policy and licensing due diligence

When contributing an existing Project to the OpenSSF, the contribution must undergo license and IP due diligence by the Linux Foundation (LF).

* Yes — the project is licensed under Apache-2.0
* LF IP review to be initiated upon TAC approval

### Project References

| Reference              | URL                                                              |
|------------------------|------------------------------------------------------------------|
| Repo                   | https://github.com/seebom-labs/BOMHort                           |
| Documentation          | https://docs.bomhort.dev                                         |
| Architecture           | https://docs.bomhort.dev/docs/architecture/                      |
| Roadmap                | https://docs.bomhort.dev/docs/roadmap/                           |
| Contributing guide     | https://github.com/seebom-labs/BOMHort/blob/main/CONTRIBUTING.md |
| Security policy        | https://github.com/seebom-labs/BOMHort/blob/main/SECURITY.md     |
| OpenSSF Best Practices | https://www.bestpractices.dev/projects/12903                     |
| OpenSSF Scorecard      | https://scorecard.dev/viewer/?uri=github.com/seebom-labs/BOMHort |
| License                | Apache-2.0                                                       |
