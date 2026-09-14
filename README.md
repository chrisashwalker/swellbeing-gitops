# Swellbeing GitOps

## Notes

- This GitOps repository contains a mixture of Helm charts and Kubernetes deployment.yaml files.

- Swellbeing apps have Helm charts, with service ports and hostnames defined and configured under a Traefik ingress.

- The apps are configured to run on a K3s cluster, utilising Argo CD for continuous deployment, under an "apps of apps" deployment pattern.

- The cluster is accessed via a Cloudflare tunnel - with routes pointing to the Traefik ingress container for each configured hostname.

- Apps are configured to selfHeal and prune outdated resources upon sync with their Git repositories.
