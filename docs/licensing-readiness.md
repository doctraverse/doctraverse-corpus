# Dual-Licensing Readiness

Status: **Planning document, not a CLA or commercial license.**
Last updated: **2026-10-14**.

Doc Traverse Corpus repository materials currently use AGPL-3.0-only.
The intended commercial alternative depends on rights, contribution terms, and
a defined product scope. The work below prepares that model without granting
commercial permissions prematurely.

## Identify the licensor and rights

Before publishing a CLA or offering commercial terms:

- Identify the legal person or entity receiving contributor grants and entering
  commercial agreements. A GitHub organization or brand name alone does not
  identify that contracting party.
- Document ownership or applicable permissions for founder, employee, contractor,
  and previously written code. Commit authorship alone is not an ownership check.
- Decide how rights and agreements would transfer if the project moves to a
  company or changes its contracting entity.
- Define a contact channel, applicable jurisdiction, and recordkeeping process.

The project may initially contract through an individual and later through a
company registered in another country. The final contracting party, country,
governing law, and venue remain open decisions. Current planning information
does not select the law or venue of a future agreement.

If a company becomes the licensor, document the transfer or grant of founder
rights and check whether contributor grants can be assigned or sublicensed to
that entity. Incorporation alone does not transfer copyright or existing
agreements. Define successor and assignment provisions in the final agreements
as appropriate, while preserving existing AGPL grants.

## Prepare contribution terms

The proposed approach is a contributor license grant that leaves ownership with
the contributor and gives the identified licensor sufficient rights for both
AGPL and commercial distribution. Copyright assignment is a different option
and has not been selected.

The agreement needs to address:

- Contributions in scope: code, documentation, tests, and other supplied material.
- An explicit copyright grant covering use, modification, distribution,
  sublicensing, and the intended alternative commercial terms.
- Appropriate patent permissions and their scope, where relevant.
- Contributor authority, employer authorization, and disclosure of third-party
  material that the contributor cannot license as their own.
- Retained contributor rights, warranties or disclaimers, and the applicable law.
- Individual and corporate participation, agreement changes, and the evidence
  needed to prove acceptance of a particular version.

Choose and review an agreement suitable for the actual licensor and jurisdictions
before activating it. A DCO or an AGPL-only inbound license is not a substitute
for missing commercial distribution rights.

After the agreement is ready, publish its full text and configure an acceptance
process. A manual record can work initially; automation must check all relevant
contributors and preserve the accepted version. Do not merge external patches
while the required rights remain unresolved.

## Define code scopes and notices

Create a file or component inventory before adding differently licensed code.
Record the copyright holder, origin, version, license, required notices, and
whether each component can be included in the commercial offering.

- Keep [LICENSE](../LICENSE) as the unmodified AGPL text and
  [LICENSING.md](../LICENSING.md) as the scope explanation.
- Add accurate copyright notices and SPDX identifiers when source files appear.
  The current public default is `AGPL-3.0-only`.
- Retain original notices for any MIT MCP reuse or other third-party material.
- Use an explicit license notice for future Enterprise code before publishing it,
  or keep that code in an appropriately licensed private repository.
- Review the rights and compatibility of the complete distributed or hosted
  work. A separate folder, process, API, or feature flag does not settle that review.

A future SPDX expression such as
`AGPL-3.0-only OR LicenseRef-DocTraverse-Corpus-Commercial` would be appropriate
only for a scope actually offered under both licenses, with the commercial
license identified and available. It is not the current license expression.

Do not apply a proprietary restriction retroactively to copies already released
under AGPL. An approximate open/closed product ratio is a packaging idea, not
a grant of rights for specific files.

## Prepare the commercial offering

Define these separately before offering a paid contract:

| Arrangement | Terms to define |
| --- | --- |
| Alternative license for eligible core code | Covered code and versions, grant and restrictions, redistribution, term, fees, warranties, liability, and termination. |
| Enterprise functionality | Actual feature and code scope, applicable license, entitlement, deployment rights, updates, and support. |
| Managed SaaS | Service scope, tenant and data boundaries, model providers, retention, deletion, security commitments, and applicable service or data-processing terms. |

Review the resulting documents against the licensor's rights and chosen
jurisdictions. Set pricing and service commitments after product and operational
requirements are known.

For AGPL deployments, plan how a modified network-facing version offers its
Corresponding Source under section 13. Release packaging also needs the notices
and source obligations applicable to distribution, including relevant build and
installation material. The implementation will need to verify these paths.

## Reference implementations

These projects illustrate documentation patterns; their agreements have their
own parties, scope, and legal assumptions. They are not templates adopted by
Doc Traverse Corpus.

Checked **2026-10-14**:

- [Grafana licensing scope](https://github.com/grafana/grafana/blob/2cb8ce5c8296a9e24ac122d5789603d9cb13285a/LICENSING.md): a default AGPL-3.0-only license and explicit component exceptions.
- [Grafana contributor agreement](https://github.com/grafana/grafana/blob/2cb8ce5c8296a9e24ac122d5789603d9cb13285a/docs/sources/developer-resources/contribute/cla.md): retained contributor ownership, copyright and patent grants, and employer authority.
- [Documenso contributor agreement](https://github.com/documenso/documenso/blob/d4e6eeaf880dc2b3425dcb0242b9a4206ac10443/CLA.md): a named contracting entity and contributor rights provisions.
- [Documenso Enterprise license](https://github.com/documenso/documenso/blob/d4e6eeaf880dc2b3425dcb0242b9a4206ac10443/packages/ee/LICENSE): separately scoped Enterprise terms, illustrating open-core rather than proving that the entire AGPL core is commercially relicensable.

## Current Readiness

- Public license text and scope explanation: present.
- Contribution policy and rights requirements: documented.
- Possible transition from an individual to a future company: identified for planning.
- Final commercial licensor, jurisdiction, and verified ownership chain: pending.
- Reviewed CLA and agreement acceptance process: pending.
- Commercial agreement and defined Enterprise scope: pending.
- Dependency inventory and release compliance checks: pending implementation.
