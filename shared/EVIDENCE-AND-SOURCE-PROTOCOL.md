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
