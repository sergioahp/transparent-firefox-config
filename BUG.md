# BUG: Mouse cursor trail on semitransparent context menus

## Description
Mouse cursor leaves a trail of barely darker squares around the cursor when hovering over semitransparent context menus.

## Reproduction
1. Right-click to open context menu (with semitransparent theming)
2. Move mouse cursor around the menu area
3. Observe faint darker squares trailing the cursor

## Behavior
- Trail appears as just barely darker squares
- Only visible on semitransparent context menu surfaces
- Trail disappears quickly but is noticeable during cursor movement
- Could not capture in screenshot - visual artifact dissipates too quickly

## Possible Cause
Likely related to compositor blur effects interacting with cursor rendering on semitransparent surfaces.

## Context
- Context menu uses `var(--uc-surface)` (0.80 alpha transparency)
- Compositor blur is enabled and working on these menus
- Trail does not appear on opaque UI elements