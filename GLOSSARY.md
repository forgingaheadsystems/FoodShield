# FoodShield Glossary

This file is the FoodShield terminology source of record. It governs FoodShield project language; it does not replace definitions owned by regulators, funders, standards bodies, carriers, warehouses, food banks, pantries, or produce-trade organizations.

Each entry records its status, project meaning, relevant aliases, evidence, and limits. An unresolved entry is preserved for review but is not an approved implementation definition.

## Terminology provenance rule

This rule is owner-directed. The four category labels below were drafted by
Codex and accepted for FoodShield on 2026-11-12:

- **Source terminology:** wording used by an identified external or project
  source.
- **Agent-proposed terminology:** wording introduced by an agent, including an
  adaptation, compound, conjugation, normalization, or renamed form of an
  established expression.
- **Owner-approved FoodShield terminology:** wording the owner has accepted for
  project use. Its earlier origin is still recorded.
- **Unresolved terminology:** wording or meaning awaiting an owner decision or
  authoritative verification.

The [FoodShield-to-Industry Terminology Map](TERMINOLOGY-MAP.md) preserves
external role and nomenclature distinctions that should not be collapsed into
the project glossary.

## FoodShield

**Status:** Canonical
**Designation origin:** Owner-approved project name; historical misspellings
were observed in the imported handoff.
**Concept:** The project and software suite being established in this repository.
**Aliases:** `FoodSheild` and `foodshielf` are observed misspellings only.
**Limit:** No technical architecture or module structure is implied by the name.

## food pantry

**Status:** Canonical; context-qualified
**Designation origin:** Established sector and regulatory term. The FoodShield
project definition is a Codex-drafted adaptation accepted during the glossary
bootstrap.
**Project meaning:** An organization or program that distributes food directly to people or households.
**Distinction:** A food pantry is not synonymous with a food bank.
**External limit:** When a pantry participates in The Emergency Food Assistance Program (TEFAP), the exact definition and eligibility conditions in 7 CFR 251.3 control.

## food bank

**Status:** Canonical; context-qualified
**Designation origin:** Established sector and regulatory term. The FoodShield
project definition is a Codex-drafted adaptation accepted during the glossary
bootstrap.
**Project meaning:** An upstream organization that receives, stores, and distributes food to food pantries or other feeding organizations and may also conduct direct distribution.
**Distinction:** A food bank may perform warehousing, shipping, receiving, or funding functions, but those functions do not make the terms interchangeable.
**External limit:** Program-specific definitions, including the TEFAP definition in 7 CFR 251.3, control when that program is in scope.

## survey feature

**Status:** Canonical project term
**Designation origin:** Agent-proposed normalization of the paper's expressions
for use during the audit; owner-approved for FoodShield.
**Concept:** A digital-tool feature requested or desired by respondents in the Sundermeir et al. nationwide food-pantry survey.
**Alias:** `ask` is accepted as owner shorthand.
**Source expression:** The paper uses expressions including “desired digital tool feature.”
**Limit:** A survey feature is evidence of reported interest, not by itself an approved implementation requirement or a complete specification.

## client choice

**Status:** Canonical source term
**Designation origin:** Source terminology from the Sundermeir et al. paper.
**Concept:** A model in which people receiving food can choose foods based on their needs, preferences, and cultural appropriateness.
**Distinction:** Client choice is not synonymous with online ordering; online ordering can be one way to support choice.
**Limit:** The future user-facing label for people receiving food remains unresolved.

## online ordering

**Status:** Canonical source term
**Designation origin:** Source terminology from the Sundermeir et al. paper.
**Concept:** A digital process for selecting or requesting pantry food before distribution.
**Distinction:** The survey discusses online ordering and client choice together in one overall result but lists them separately in its pantry-size table. FoodShield must preserve that distinction until an approved design relates them.

## pantry statistics

**Status:** Canonical term; definition incomplete
**Designation origin:** Agent-proposed shortening of source expressions such as
`tracking pantry statistics` and `pantry numbers`; owner-approved as the current
FoodShield label, with its measures unresolved.
**Concept:** Recorded figures used to describe pantry activity or operations.
**Alias:** `pantry numbers` is a source expression.
**Limit:** No specific measures, reporting periods, funder reports, or government data fields have been selected.

## module

**Status:** Canonical planning term
**Designation origin:** Owner-selected planning terminology. The definition
below is a Codex-drafted normalization of the owner's three-to-five-module
direction.
**Concept:** A coherent user-facing grouping of related FoodShield capabilities.
**Owner constraint:** The suite is intended to contain three to five modules, with fewer preferred.
**Limit:** `Front Desk`, `Shelf`, `Helpers`, `Notices`, and `shared core` were Grok proposals and are not canonical names or approved boundaries.

## 100% no cost

**Status:** Unresolved operational term
**Designation origin:** The no-charge goal came from the owner. The exact phrase
`100% no cost` was introduced in agent-drafted website copy and accepted for
publication; its testable operational meaning remains unresolved.
**Observed intent:** FoodShield has been described as available to users without charge.
**Distinction:** User price, source-code license, hosting cost, messaging cost, support cost, integration cost, and third-party fees are separate concepts.
**Owner decision needed:** Define which users, services, transactions, and operating costs the phrase covers before it becomes a testable requirement.

## open source

**Status:** Canonical licensing concept
**Designation origin:** Established licensing terminology used by the owner.
**Concept:** Source code distributed under an open-source license.
**Current repository fact:** The repository currently contains an MIT license.
**Distinction:** Open-source licensing does not prove that a hosted service or third-party integration is free of charge.

## staff and volunteer communication

**Status:** Unresolved scope
**Designation origin:** Agent-proposed normalization of several source
expressions. The label is accepted for audit use; the participant scope is not
approved.
**Observed expressions:** `communicating with volunteers and staff`, `communicating with staff, volunteers and clients`, and `staff and volunteer messaging`.
**Conflict:** The source materials do not consistently name the same participant groups.
**Owner decision needed:** Decide whether the FoodShield feature includes communications with clients.

## emergency-services communication

**Status:** Unresolved concept
**Designation origin:** Agent-proposed compound and grammatical normalization of
the source phrase `communicating with nearby emergency services`. The label is
accepted for audit use; the underlying workflow is not approved.
**Observed expressions:** `communicating with nearby emergency services`, `contact with nearby emergency services`, and `connect with emergency services in my area`.
**Known limit:** The survey does not define the intended organization, message, trigger, channel, or workflow.
**Owner decision needed:** Define the concept before it becomes an implementation requirement.

## External terminology under audit

**Heading origin:** Agent-proposed audit heading; accepted for the current
glossary task.

The following groups are being audited but are not yet incorporated as FoodShield definitions:

- TEFAP and charitable-food-program actors;
- Federal funding and award relationships;
- Food transportation, trucking, loading, receiving, and warehousing roles;
- Produce trade, donation, food safety, and traceability terms; and
- Supply-chain identifiers and exchange standards.

The initial distinctions and unresolved applicability questions are recorded in
[TERMINOLOGY-MAP.md](TERMINOLOGY-MAP.md).
