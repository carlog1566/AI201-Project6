# PR Response Doc — CineLog Watchlist Feature

## AI Usage
<!-- Fill in at the end — how you used AI tools during this project -->

## Comment 1 — Rename
**What I did:**
- Renamed `save_to_watchlist()` to `add_to_watchlist()` in the watchlist service and updated every import and call site.

**How I verified:**
- Ran the full test suite and confirmed there were no import or runtime errors.

## Comment 2 — Deduplication
**What I did:**
- Implemented a duplicate check before creating a new watchlist entry. The implementation follows the same pattern used by `add_to_collection()` so the behavior is consistent across services.

**How I verified:**
- Confirmed duplicate additions raise the expected exception and that only one database entry exists for a user/film pair.

## Comment 3 — Missing test
**What I did:**
- Created `tests/test_watchlist.py` and added a test that verifies adding a nonexistent film raises `FilmNotFoundError`.

**How I verified:**
- Ran the new watchlist test individually and then executed the complete test suite to ensure nothing else regressed.

## Comment 4 — Default visibility
**My position:**
**Reasoning:**
**Tradeoff acknowledged:**

## Comment 5 — Sort order
**My position:**
**Reasoning:**
**Engagement with reviewer's point:**

## Comment 6 — Rebase
**What conflicted:**
**How I resolved it:**
**How I verified no conflict remains:**

## PR Description
<!-- Written at the end — feature overview, design decisions, manual testing steps -->