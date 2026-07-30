# habit

A Mon–Sun grid that **records what happened**. Nothing else.

Rows are grouped: *Body* (runs, weights, mobility, stretching) · *Mind* (breath,
wind-down) · *Nutrition* (protein, water, supplements, alcohol). Tap a cell to
advance it, long-press to clear it, browse weeks with ‹ ›.

At the top: readiness plus exactly one do/don't line, computed by rule from the
Garmin data `garmin_sync.py` already produces. No model call — it has to be
instant and identical every time.

## Deliberately absent
No streaks, no badges, no chains, no gamification. Accountability here is the
coach reading the data, not the app congratulating you. If a future version
grows a streak counter, that's the bug.

No planning either. Runs are planned in Outlook; this grid records them
afterwards. Rebuilding a planner here is how the diary failed.

## How it's built
One vanilla HTML file, no framework, no build step. Writes the `daily_habits`
table in the hosted `astrid-efficiency` Supabase project — the same table the
coach already reads, so history is continuous. The anon key is public by design.
