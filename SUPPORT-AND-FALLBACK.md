# L6 — Support and fallback record

**Project:** More Than Words: Keeping the Diné Language Alive  
**MDN pages checked:** 14 November 2026  
**Note:** MDN's Baseline labels describe broad availability, not a guarantee for every embedded browser or assistive-technology combination. The project also includes feature queries and non-enhanced layouts so the story remains readable if an effect is unavailable or disabled.

| Feature | MDN reference and support note | How this project uses it | Fallback / disabled behavior |
|---|---|---|---|
| `position: sticky` | [MDN: `position`](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Properties/position) — MDN marks the property Baseline Widely available; sticky requires a non-auto inset and is constrained by its containing block and nearest scrolling ancestor. | `.story-guide` is sticky only at 52rem and wider, with `inset-block-start: 1.25rem`. | At smaller widths it is static. If sticky is unsupported or CSS is disabled, it remains in normal flow and all navigation links remain available. Avoid adding overflow scrolling ancestors around the grid. |
| `clip-path: polygon()` | [MDN: `clip-path`](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Properties/clip-path) — MDN marks the property Baseline Widely available; basic-shape support is documented separately in browser compatibility data. | A polygon crop is applied only to the feature illustration inside `@supports`. | The image is a complete rectangular image by default. The figure caption and all article text are outside the clipped image. Disable the declaration in DevTools to confirm. |
| `shape-outside: circle()` | [MDN: `shape-outside`](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Properties/shape-outside) — MDN marks the property Baseline Widely available; the property defines the float shape around which inline content wraps. | At 52rem and wider, the portrait illustration floats inline-start with `circle(50%)` and `shape-margin: 1rem`, inside a `@supports` block. | Without support, the image is a centered block and prose remains full-width normal flow. The float itself is also omitted when the feature query fails. |
| Basic shape `circle()` | [MDN: Basic shapes with `shape-outside`](https://developer.mozilla.org/en-US/docs/Web/CSS/Guides/Shapes/Using_shape-outside) — MDN describes `circle()` as a basic shape and demonstrates it with a float. | Defines the circular text-wrap boundary around the abstract portrait illustration. | If the shape is disabled, content returns to the ordinary float/normal-flow layout; this stylesheet's `@supports` grouping ensures the float is not applied without shape support. |


## Reference links

- https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Properties/position
- https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Properties/clip-path
- https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Properties/shape-outside
- https://developer.mozilla.org/en-US/docs/Web/CSS/Guides/Shapes/Using_shape-outside
