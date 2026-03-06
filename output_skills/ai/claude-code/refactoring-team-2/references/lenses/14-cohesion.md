# Lens: Cohesion & Boundaries

A unit that contains things that do not belong together, or boundaries that cut through concepts instead of between them.

## The Question

Does everything inside each unit belong together? Do the boundaries between units reflect the boundaries between ideas?

## How to Spot

- A class whose methods split into groups that use different fields
- A module that exports unrelated functions grouped only by convenience
- Files named "utils," "helpers," "misc" — concepts hiding behind vague containers
- Concepts split across files that belong together, or crammed into one file that should split
- A class or module that is hard to name because it does many unrelated things

## Process

For each unit — class, module, file — try to describe what it does in one sentence without using "and." If you need "and," the unit likely has multiple responsibilities that could be separated. Then look at the boundaries: does each file represent one complete concept, or are concepts scattered?

## Trade-off

Cohesion is a spectrum. Over-splitting creates tiny units that are hard to navigate. The goal is units where everything inside genuinely belongs together and boundaries fall between ideas, not through them.

## Go Deeper

Where are "and" hiding in class or module descriptions? What files should be split, merged, or renamed? Where do heavy cross-imports between files suggest the boundaries are in the wrong place?
