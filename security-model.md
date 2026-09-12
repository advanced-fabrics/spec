# Security Model

AdvFab separates observation, planning and mutation. Observation is the default. Mutation requires all of: an advertised provider capability, an explicit AdvancedFabric policy, Kubernetes RBAC authorization and an authenticated workload identity.

Trust boundaries include users to API server, controller to provider, provider to managed network, release workflow to registry, and registry to consumer. The reference runtime uses mutual TLS with short-lived cert-manager certificates and supports SPIFFE identities through a replaceable identity provider.

Threat analysis follows STRIDE. Implementations must address spoofed provider identity, tampered observations, repudiation of apply operations, disclosure of topology or credentials, resource-exhaustion attacks and privilege escalation. Secrets must not appear in CRD status, logs, conformance results or support bundles.
