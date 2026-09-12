# Compatibility Policy

Advanced Fabrics uses semantic versioning for released APIs, CLI behavior, configuration and provider protocols.

- A GA contract is backward compatible throughout a major version.
- Deprecations remain supported for at least two minor releases and six months, whichever is longer.
- Kubernetes conversion may bridge versions within `networking.advfab.org`; the retired `networking.re8ch.com` group is migration input only and is not served by v1 runtime components.
- Unknown optional fields must be ignored when the containing schema permits extension. Unknown required capabilities must produce a structured incompatibility error.
- A provider declares its protocol versions and capabilities before any observation or mutation request.

Compatibility claims are verified by the public conformance suite. Documentation alone is not evidence of compatibility.
