# Garoon Common Patterns for QA Planning

Use this as a checklist when writing the Impact section and Unknowns. Only include a pattern if the PBI touches that area — do not apply all patterns to every PBI.

---

## Cloud vs On-Premise

Garoon has two versions: cloud (.com) and on-premise (self-hosted). Some features are cloud-only.

- PBIs usually have a "Difference between .com and On-Premise" section — read it
- If cloud-only: add to Impact — test that the feature is blocked on on-premise
- If not mentioned in PBI → do not assume; put in Unknowns

---

## License / Trial Restriction

Cloud environments have two types: trial (free trial) and licensed (contracted).

- Some features are restricted to licensed domains only
- If PBI mentions license restriction → test that trial environments are blocked
- Reference: GTM-19588 pattern (licensed-domain restriction)

---

## Multi-language

Garoon supports 4 languages: Japanese (JA), English (EN), Chinese Traditional (ZH-TW), Chinese Simplified (ZH-CN).

- If the feature involves AI-generated or system-generated text: output language follows the **login user's language setting**, not the language of the input/query
- If the feature involves UI labels or notifications: check all 4 languages

---

## Permission Model

Garoon has multiple permission levels: system admin, app admin, regular user, organization, role.

- When a PBI changes data visibility or actions → consider which permission level is affected
- Common cases: private events (owner-only), calendar view permission (per-user), admin-only settings
- Do not add permission test points unless the PBI involves data access or user roles

---

## Audit Log

Some actions in Garoon are recorded in the audit log.

- If PBI does not mention audit log → do not add it to Impact
- Put it in Unknowns to confirm with Dev whether the new action should be logged
