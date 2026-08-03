Goal: Rework the hero section's color palette to a dark blue scheme.
Layout and animation only for now, the project catalog section
below stays as-is / gets skipped.

Context: Read AGENTS.md first. This is index.html, a black hole
hero with two orbiting stars, currently amber/gold. I want a dark
blue version instead.

Task:
- Deep indigo/navy void background, not pure black, not generic navy.
- Keep the two stars visually distinct from EACH OTHER, don't make
  them both the same blue, one cool ice-blue/white, one deeper
  violet-blue, so "two things orbiting" still reads at a glance.
- Event horizon stays dark, the disk glow shifts to blue/violet
  instead of gold/ember.
- Keep the existing orbit rings, animation timing, and layout
  structure. This is a recolor pass, not a rebuild.
- Skip the catalog section, just get the hero right, I'll wire in
  real project data later.

Constraints: No build tools, no frameworks. Use the existing CSS
custom properties in :root, don't hardcode new colors inline.
Respect prefers-reduced-motion, it's already implemented, don't
touch it.

Completion criteria: Open index.html in a browser. Hero reads as
dark blue/indigo, the two stars are distinguishable from each
other, orbit animation still runs, reduced-motion still disables it.
