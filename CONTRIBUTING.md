# Contributing to bwui

Before contributing, please familiarize yourself with the project's philosophy and concepts described in the README.

## Principles

All contributions should align with the core principles of bwui:

- Structure over aesthetics
- Sensible defaults
- Constraint over unlimited choice
- Consistency over novelty
- Accessibility by default
- Maintainability over convenience

## Abstractions

Abstractions form the public API of bwui.

Before introducing a new abstraction, ask:

- Is this a concept developers already recognize?
- Is this broadly applicable across applications?
- Can this be composed from existing abstractions?

### Adding new Abstractions

Before implementing a new abstraction, contributors should answer the following questions:

1. Is this a concept developers already recognize?
2. Is it broadly applicable across applications?
3. Can it be composed from existing abstractions?
4. Which layer does it belong to?
5. What is its public API?
6. Does it have state?
7. Does it have accessibility implications?

**Abstraction Checklist**

- [ ] Purpose is clearly defined
- [ ] Responsibilities are documented
- [ ] Non-responsibilities are documented
- [ ] Correct layer has been selected
- [ ] Public API is documented
- [ ] State model has been defined
- [ ] Accessibility implications have been considered
- [ ] Documentation has been updated

## Layers

bwui is organized into the following layers:

- Tokens
- Base
- Layout
- Components
- Patterns

Contributors should place code in the appropriate layer and avoid mixing responsibilities between layers.

## Naming Convention

bwui uses the BEM methodology.

Public classes:

```css
.bwui-button
.bwui-button__icon
.bwui-button--danger
```

Private classes:

```css
._bwui-focus-ring
```

Public classes form the API of bwui. Private classes may change without notice.

## State

When representing state, use the following order of preference:

1. Native HTML attributes
2. ARIA attributes
3. Custom data-\* attributes

## Accessibility

Accessibility is a first-class concern in bwui.

Contributors should prefer semantic HTML, preserve keyboard accessibility, maintain visible focus states, and avoid reducing accessibility for visual convenience.
