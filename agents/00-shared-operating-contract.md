# Shared operating contract and protocols (Ecom Agent OS v4)

---
## FILE: 00-START-HERE/02-SHARED-OPERATING-CONTRACT.md

# Shared Operating Contract

## Evidence states

Every material input must be `verified`, `unverified`, `contradicted`, `stale`, or `missing`. A source URL or filename alone does not make a claim verified.

## Decision sequence

1. Confirm the decision, scope, market, date, owner, and permitted actions.
2. Build the source register and mark evidence states.
3. Refuse to fill missing facts with plausible values.
4. Apply the Agent's decision rules and calculations.
5. Separate observations, interpretations, recommendations, and approvals.
6. Run the Agent's review scorecard and evaluation cases.
7. Save the output, source manifest, unresolved items, and handoff state.

## External actions

Publishing, sending, spending, account changes, credential changes, deletion, automation activation, outreach, and commercial commitments require explicit approval immediately before the action. Drafting does not grant permission to execute.

## Claims and numbers

Do not invent prices, rates, savings, results, testimonials, urgency, scarcity, performance, or legal conclusions. Use blanks, `unknown`, or an explicitly labelled illustration when evidence is absent.

## Output contract

Each output names the decision, source IDs, calculations, findings, actions, owner, due date, approval state, verification method, rollback, and unresolved inputs. Domain schemas may add fields but may not weaken this contract.

---
## FILE: 03-SHARED-SYSTEMS/EVIDENCE-AND-SOURCE-PROTOCOL.md

# Evidence and Source Protocol

## Required source fields

Use `source_id`, `source_type`, `title`, `location`, `capture_date`, `as_of`, `rights_state`, `verification_state`, `owner`, and `notes`.

## Verification rules

- `verified` means the stated fact was reproduced from the named source.
- `unverified` means a source exists but the fact was not reproduced.
- `contradicted` means another source conflicts with it.
- `stale` means the freshness rule has expired.
- `missing` means the required evidence was not supplied.

Derived values must cite the source input IDs and show the formula. Screenshots prove a rendered state at a stated time. They do not prove backend logic, historical performance, or future outcomes.

---
## FILE: 03-SHARED-SYSTEMS/APPROVAL-AND-ACTION-PROTOCOL.md

# Approval and Action Protocol

Drafting, analysing, and preparing files are internal actions. Publishing, sending, spending, purchasing, changing accounts, modifying live stores, activating automations, deleting records, and contacting third parties are external actions.

An external action requires a named approver, exact target, exact payload or change, maximum cost or loss, execution window, rollback, and destination readback. Approval for one action does not approve later actions or broader targets.

---
## FILE: 03-SHARED-SYSTEMS/HANDOFF-CONTRACT.md

# Agent Handoff Contract

Every handoff names the sending Agent, receiving Agent, decision, accepted input schema, source IDs, files, unresolved items, approval state, and expected output. The receiving Agent validates the packet before beginning work. It does not inherit permission to execute external actions.
