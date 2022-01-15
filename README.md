# EEZEE - Learnings

The learnings are not limited to through code reviews.

## Table of Contents

- [Advice](#advices)
- [Code Quality](#code-quality)
- [Git](#git)
- [Quotes](#quotes)
- [React.js](#reactjs)
- [styled-jsx](#styled-jsx)
- [Contributors](#contributors)

## Advice

- Always good to remind the pair programmer where the last code review left off.
- 3 principles by Jasper:
  - Do not repeat yourself
  - Feel fast using `contentHidden` to improve user-experience. E.g. Grey screen when navigating on eezee.sg.
    - Tips: contentHidden is a **contextType** we use on React to hide content as we want.
  - Re-use functions
- Align with UI/UX designers is the most important in creating a robust design system and user-interface components. e.g. no abnormal paddings and sizes.
- Design system is the most important stuff for Frontend Engineers.
- Do not [premature optimization](https://ubiquity.acm.org/article.cfm?id=1513451).
  > "It simply means that trying to optimize before knowing WHERE you need to optimize will hurt you."
- Learning posture is important during pair programming as there are a lot of signals interchanging during the process.
- Shortcuts on **VSCode** improve productivity by miles.
  - Navigating around files, functions, codes, windows, etc.
  - Fold/Unfold functions: [Link](https://stackoverflow.com/questions/30067767/how-do-i-collapse-sections-of-code-in-visual-studio-code-for-windows)
  - Focus mode: Ctrl + K -> Z
  - **Search/review functions**: Ctrl + Shift + O
  - Open terminal: Ctrl + ` (tilde)
- When code refactoring, let the errors come out, and not to be afraid. We can solve the errors step-by-step by checking out the right bar.

## Code Quality

- Removing codes shouldn't be an afterthought.
- Be careful of when naming anything.
  - e.g. component, variable, type, prop, etc.
- Do not put comments unless is really necessary or complex.
- `is` **versus** `get` when naming functions:
  - isExpanded = boolean flag.
  - getProductTitle = get data.
- Keep the logics at the top of components instead of doing them inside **OR** create function to do complex logics, and call the functions when needed.
- Must fix TypeScript errors before moving on.
- Official comments must be in all-caps.
- Reason of naming functions alphabetically is important because **IntelliSense** provides us the pattern, so we can get and use the functions conveniently.
- Sometimes we need more time to look into code in detail, so no worries.

### Implementation

We have to follow this pattern of writing clean React components. Notice the parenthesis.

```js
/* Without newline */
<>
  {this.state.isExpanded && <Drawer>...</Drawer>}
</>

/* With newline */
<>
  {this.state.isExpanded && (
    <Drawer>
      {this.props.children}
    </Drawer>
  )}
</>
```

## Git

- Branch frequently, commit often.
- Make small, single-purpose commits.
- Preserve history and traceability.
- Write short, detailed commit messages.

> [vcs/git-best-practices-git-commit](https://www.perforce.com/blog/vcs/git-best-practices-git-commit)

### Quotes

> "If the only tool you have is a hammer, you tend to see every problem as a nail."

## React.js

### General

- Do not pass props down the component tree.
  - props dwelling causes debugging more challenging because certain props might change during midway.
    - e.g. try passing 2 props down 4 components. When any of the 2 props has to be modified, we have to repeatedly update the 4 components.
    - Therefore, the solution is to use controllers to get data and use them inside components without passing down so many levels of component tree.
- Do not pass style prop into component.
  - To create constraints/rules for engineers to follow to keep design system pure.
- Name props using English, and not number.
  - e.g. `size="s"` instead of `size={4}`

## `styled-jsx`

- Aware of unused CSS styling.
- Design system `<Row>` & `<Col>` are sufficient, do not use `margin left & right`, or `display: flex`;
- When to use `:global`?
  - situation like `.ctn :global(.count-ctn)` inside a component because `.ctn` will have its unique jsx class name as the parent element to specifically target its child element.

> [vercel/styled-jsx](https://github.com/vercel/styled-jsx)

## Contributors

- Jasper Yap
- Yee Han
