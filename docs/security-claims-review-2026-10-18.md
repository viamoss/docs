# Security documentation scope correction

Prepared 18 October 2026. This is a Draft documentation review, not a new
security policy, deployment receipt or certification statement.

The English and Korean overview, data-protection, audit-logging and compliance
pages previously described universal organization filtering, credential hashing,
request capture, redaction, immutable logs and complete deletion. The revised
pages distinguish the supported paths and customer-operated deployments. They
preserve the Audit API examples and SDK collection controls. SOC 2 is an
examination in progress; ISO 27001 certification is in progress. No issued report,
certificate or universal GDPR/EU AI Act compliance is claimed.

Detailed request traffic is optional and can contain sensitive content. The
revision separates that traffic from audit events and infrastructure logs and
calls for proportionate collection, access and retention. Primary user deletion
does not establish deletion of knowledge, objects, vectors, recordings, backups
or external copies. Applicable notice and contract deadlines still govern.

## Source comparison

- Existing technical review of moss-platform at
  `88d962283860cbc87547d2c98423702dfba07a60`, including
  [audit and traffic logging](https://github.com/viamoss/moss-platform/blob/88d962283860cbc87547d2c98423702dfba07a60/docs/security/audit-and-traffic-logging.md)
  and [data lifecycle](https://github.com/viamoss/moss-platform/blob/88d962283860cbc87547d2c98423702dfba07a60/docs/security/data-lifecycle.md).
- Current recording source compared at dev
  `a72382a06cc55aed2af14fa873e700da03fb986a`: backend fallback enables recording,
  SDK fallback disables it, and rrweb uses `maskAllInputs: false` with the
  `data-recording-block` exclusion. These defaults do not establish actual
  customer enablement or complete masking.
- The retained 26-entry processing inventory and vendor assessments identify
  record/store-specific periods and customer-operated scope. They do not
  establish one configurable retention period or every recipient/transfer fact.
- Existing user-deletion, API access, credential-storage and production SDK
  authentication reviews are reused. No infrastructure or product setting is
  changed by these pages.

## Validation and publication

All eight MDX files compile with `@mdx-js/mdx`, frontmatter and GFM handling.
Relative page links resolve to repository pages, and `git diff --check` passes.
An independent bounded source/wording review found retained configurable-period,
universal-detailed-log and terms-link leftovers; these were corrected before
handoff. The current terms destination is `/legal-terms/terms-and-conditions/`.

This is a reviewable Draft PR. The communication owner must resolve actual
recipient, deployment, privacy-notice and applicable contractual facts and the
normal exact-body publication decision before merge/publication. The website
privacy candidate remains a separate PR. Do not infer completed controls or a
published notice from compilation or a Draft PR.
