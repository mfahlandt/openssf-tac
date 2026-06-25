# 2026 Q2 Sigstore

## Post-quantum cryptographic readiness

Following the community's [timeline and plan](https://docs.google.com/document/d/15wQW5RCk55_CrIOYEtzJ0IyazbBGdMK8KsaI8S8oJ7U/edit?pli=1&tab=t.0#heading=h.o3tezvh8snap)
to create and rollout infrastructure and clients that support post-quantum cryptographic signatures, we have now
authored a [design document](https://docs.google.com/document/d/1g3WQk4JSwQ26MGwB-Kkhu8ylrPF5JnE4v62d2tDC2xY/edit)
(please join [sigstore-dev](https://groups.google.com/g/sigstore-dev) to view)
with technical details on the infrastructure and client changes. We're excited
to get started and will have much to demo in the coming months. We welcome
any community feedback, particularly from those with private Sigstore deployments
to better understand their operational requirements.

## Adoption highlights

* [Pixi](https://pixi.prefix.dev/latest/) is leveraging sigstore-rust to create attestations
* [mise](https://github.com/jdx/mise) is using sigstore-rust to verify GitHub artifact attestations

## Rekor v2 as the default paused

Given our focus has shifted to supporting PQC, we will not pursue making Rekor v2
the default log, as this would be a breaking change for ecosystems. The public instance
will still remain up, clients just won't write to it by default.

We have an upcoming [blog post](https://github.com/sigstore/sigstore-blog/pull/95)
with more details, including how to use Rekor v2 and benefits to clients that do
choose to switch over.

## Cosign v3.1

[Cosign v3.1](https://github.com/sigstore/cosign/releases/tag/v3.1.0) was recently released,
which deprecates a significant number of flags as we continue our efforts around signature
standardization with the [Bundle](https://blog.sigstore.dev/cosign-verify-end-user/) format.

Cosign v4, which will remove all deprecated flags, will follow shortly. Clients can stay on
v3.x if needed.

## OpenSSF TI-funded log monitoring website

[Through OSSF TI funding](https://github.com/ossf/tac/issues/536), work continues to
build a website for monitoring the Rekor transparency log, akin to https://www.gopherwatch.org/.
See [an early version](https://github.com/trailofbits/rekor-watch), which will be merged
into [sigstore/rekor-monitor](https://github.com/sigstore/rekor-monitor) shortly. We will
work with the broader community to identify an organization to stand up an instance of the monitor.

## Funding requests and updates

We are not planning any additional funding requests at this time.

Updates for existing funding requests:

* [Log monitoring website](https://github.com/ossf/tac/issues/536) - Funds have been fully allocated with monthly invoicing, work is wrapping up
* [Rust client audit](https://github.com/ossf/tac/issues/574) - Trail of Bits will be completing this audit starting early Q3.
