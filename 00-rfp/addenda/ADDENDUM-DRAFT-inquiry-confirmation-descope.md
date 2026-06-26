# DRAFT Addendum — Remove `page-inquiry-confirmation.php` from M1

**Status:** DRAFT — not yet folded into the canonical RFP. Pending operator approval.
**Date raised:** 2026-06-26 · **Origin:** wht-figma **OD-47** (descope of Figma template 05.21).

## Change

The post-submit **inquiry confirmation** is delivered as an **inline state of the inquiry form**, not
as a dedicated page/template. `page-inquiry-confirmation.php` is therefore **removed as a standalone
M1 deliverable**. There is no separate confirmation page in the design (Figma stub `2842:27547` is
being archived; it was never built).

## RFP edits to apply on acceptance

| Location | Current | After |
|---|---|---|
| `00-rfp/RFP-2026-path-d-block-theme-retheme.md` §2 deliverables | `Inquiry confirmation — page-inquiry-confirmation.php` | remove line; note confirmation is an inline form state |
| same, M1 schedule rows (§9 / matrix) | "Private tour PDP + **inquiry confirmation** (production)" | "Private tour PDP (production)"; confirmation handled inline in the inquiry form |
| same, test matrix | "Inquiry confirmation → `tests/20-forms/` (post-submit path)" M1 | keep the **post-submit assertion** but as part of the form flow test, not a page template |
| `01-reference-files/figma-crosswalk.md` | `page-inquiry-confirmation.php  —  M1` | remove the row |
| `04-templates/commercial-submission-template.md` M1 line | "Private tour PDP + inquiry confirmation (production)" | "Private tour PDP (production)" |

## Why a draft, not a direct edit

Vendors have already **priced M1 against "PDP + inquiry confirmation."** The canonical RFP stays
unchanged until this is accepted, so the change is auditable and can be bundled with the pending
**batched RFP-cleanup** (05.22 single-tour-landing ghost, 05.25 sidebar layouts, `page-search`) rather
than landing piecemeal. The matching procurement-side **scope-reduction credit** is drafted in
`wht-2026-retheme-procurement`.

## Note

The **post-submit behavior is still required** — a successful inquiry must still confirm to the user.
What is removed is only the *dedicated page template*; the confirmation is a state within the form
system (`20.01 - windhorsetour_form_system_handoff.html`). The acceptance test for "inquiry → success
confirmation" remains in scope under the forms test path.

_Ref: wht-figma OD-47; reverses OD-45/Q2._
