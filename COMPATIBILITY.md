# Compatibility policy

What one EG OS edition promises the next. This document exists so the promise can be *checked* rather than assumed — a compatibility claim nobody can test is a claim nobody has to keep.

## Scope

This policy governs **editions of EG OS** — dated, cut weekly (`2026.08.1`, `2026.08.2`, …). It does not govern the upstream development repository, which moves several times a day by design and makes no such promise. If you track upstream directly, you are opting out of this policy, and that is a legitimate choice.

## Promised — will not break without a migration note

| Surface | What is promised |
|---|---|
| **Seed markers and tier names** | The tier vocabulary (Master / Lite / Compact) and the marker format stay readable by an agent that learned them from an older edition. A change here ships a migration note. |
| **Plugin ids and skill names** | An id or a `/skill-name` that exists in one edition is not removed in the next without at least one edition of deprecation notice. Renames ship both names for one edition. |
| **Board wire contract** | Frame names and required fields are **additive only**. Adding an optional field is free; adding a required field, removing a field, or changing what a field means ships a migration note. |
| **Marketplace plugin ids** | Stable, so an existing install keeps resolving. |

A **migration note** is a section in the edition's release notes that names what changed, what breaks, and what to do. "It's in the changelog" is not a migration note.

## Not promised

| Surface | Why not |
|---|---|
| **Section numbers inside specifications** | Numbering is sparse on purpose so cross-references from older commits stay stable, but the numbers themselves are not an interface. |
| **Internal runtime structure** | File layout, function names and module boundaries inside the reference runtime are implementation. Adapters bind to the wire contract, not to the code. |
| **Checker names and counts** | The verification suite changes as defects are found. Depending on a specific checker existing is depending on a defect having been found in a particular order. |
| **Dashboard markup and styling** | Presentation. |

## Removal is first-class

An edition that cannot remove anything accumulates into the thing a cleaner successor has to carry. This policy exists to make removal **possible and legible**, not to prevent it:

- Anything in the promised table can still be removed. It costs one edition of notice and a migration note.
- Anything in the not-promised table can be removed in any edition.
- Every removal is listed in the edition's release notes under its own heading, so an adopter reading only the headings sees it.

If you have adopted something in the not-promised column and want it promised, say so — the boundary is meant to move with real use, not to be defended.

## How to check what you are on

`EDITION.md` in this repository records the edition name, the upstream commit it was composed from, the exact version of every module, and the seed markers. That file is generated, not written, so it cannot drift from the contents around it.
