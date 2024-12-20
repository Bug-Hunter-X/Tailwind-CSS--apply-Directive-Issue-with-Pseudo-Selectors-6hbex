# Tailwind CSS @apply Directive Issue with Pseudo-Selectors

This repository demonstrates a bug related to Tailwind CSS's `@apply` directive when used with pseudo-selectors like `:hover` or `:focus`. The issue is that styles are applied unconditionally, regardless of the pseudo-selector state.  This leads to incorrect styling in the default state.

## Bug Description

When using `@apply` with a class containing pseudo-selectors, the styles from that class are applied in all states, not only when the pseudo-selector condition is true.  This contradicts the expected behavior of conditional styling using pseudo-selectors.

## Reproduction

The `bug.css` file demonstrates the issue.  Observe the unexpected styling and how it differs from the expected outcome. 

## Solution

The `bugSolution.css` file demonstrates a solution that uses standard Tailwind directives to achieve conditional styling without the use of `@apply` in this context. This is recommended practice when using pseudo-selectors.