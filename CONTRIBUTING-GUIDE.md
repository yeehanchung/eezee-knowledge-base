## Contributing Guide

It's 2022. Who doesn't like things short and simple? Thus, this guide is kept as concise as possible. Feel free to contribute.

## Code Conventions

1. Do follow naming and formatting conventions in your projects.
2. High readability.

## Semantic Commit Messages

> A better programmer writes commit messages with high clarity.

### Example

```
# A commit message:

feat(navbar): add shopping list

# Breakdown:

1. feat:                    > Type of commit
2  (navbar)                 > Scope (omit this if changes are to more than two components)
3. add                      > Present tense
4. add shopping list        > Summary of the commit
5. feat: add shopping list  > All are lowercase

# Notes:

- Do not use TITLE CASE or PAST TENSE.
```

- `build`: build related changes. E.g. adding new dependencies; npm.
- `chore`: update grunt tasks (no production code change).
- `docs`: changes to any documentation.
- `feat`: new feature for users, not a new feature for build script.
- `fix`: bug fix for users, not a fix to build script.
- `perf`: codes that improve performance.
- `refactor`: refactoring production code. E.g. renaming variables.
- `style`: formatting, missing semi colons (no production code change).
- `test`: add missing tests, refactoring tests (no production code change).

## Pull Request

- If PR does more than one thing, please split it.
- Keep PR small with clear and concise commit message.
- Your teammates appreciate them as PR is easier to be reviewed.

### New PR?

- All PR should be opened against the `main`/`master` branch.

## References

- [Conventional commits](https://www.conventionalcommits.org/en/v1.0.0/)
- [Docusaurus](https://github.com/facebook/docusaurus)
- [Git commit message convention that you can follow](https://dev.to/i5han3/git-commit-message-convention-that-you-can-follow-1709)

## License

MIT license