# Lens: Cohesion & Boundaries (Reviewer Guide)

## When to Apply

After comments. Surface cleanup is done — now look at whether the contents of each unit belong together and whether boundaries are in the right places.

## What to Look For in Diffs

- Classes or modules split into more cohesive units
- Unrelated functions moved out of convenience groupings
- Files renamed to reflect their concept
- Code moved between files to create coherent units
- "utils" files eliminated or properly named

## First Pass

Worker should find obvious problems: classes that are hard to name, modules exporting unrelated functions, vague file names, concepts split across files.

## Second Pass

If cohesion or boundary issues remain:
- Try the "one sentence without and" test yourself on each class or module
- Look at which methods use which fields — if methods cluster into groups that use different fields, the class may want to split
- Look at imports — heavy cross-importing suggests wrong boundaries
- Check for modules named "utils" or "helpers" that have grown into grab-bags

## When Done

Move on when each unit can be described in one sentence and boundaries fall between ideas, not through them.
