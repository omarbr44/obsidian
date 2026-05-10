# Problem: Sidebar height exceeded viewport when combined with header, causing unwanted scrollbars.

**Date:** {{date}}

## Context
Sidebar height exceeded viewport when combined with header, causing unwanted scrollbars.

## Problem
Sidebar height exceeded viewport when combined with header, causing unwanted scrollbars.

## Solution
Replaced `height: 100vh` with a Grid layout that accounts for the header. Alternatively, `position: fixed` worked but was less flexible.

## Lessons Learned
- `100vh` ignores other elements in flow → leads to overflow.
- `position: fixed` takes out the element out of the normal document flow (so will be in the viewport edges)
- `overflow: hidden` only hides _internal_ overflow, not page overflow.
- Flexbox/Grid is the cleanest way to make layouts that adapt to headers/footers.

## Tags
#problem #fix #css
