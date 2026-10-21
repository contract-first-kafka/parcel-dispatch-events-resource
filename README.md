# events

This repository represents the `events` Resource in the
`parcel-dispatch` System. It uses the `kafka` implementation profile and
owns the Resource catalog identity and Resource-specific operational documentation.

## After Creation

1. Review and merge the Resource pull request in the parent System repository.
2. Wait for the Resource Application and operator-managed resource to become healthy.
3. Read [Resource operations](docs/index.md) for the generated object names, connection data, and
   credential discovery commands.

## Configuration and Ownership

| Concern | Owner and location |
| --- | --- |
| Resource identity and operations | This repository: `catalog-info.yaml` and `docs/index.md` |
| Common configuration | Parent System: `resources/kafka/events/values.yaml` |
| Environment configuration and provisioning | Parent System: `resources/kafka/events/environments/<environment>.yaml` |
| Physical implementation | Platform-owned chart selected by the `kafka` profile |

The platform owns the implementation chart and operator integration. The application team owns the
reviewed common and environment values in the System repository. Do not store connection
credentials in Git; discover the operator-managed Secret using the commands and naming contract in
[Resource operations](docs/index.md).
