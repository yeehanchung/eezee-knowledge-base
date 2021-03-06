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

<<<<<<< HEAD
Example 1: fix(design/navbar): incorrect marketplace redirect
Example 2: feat(components/cart-dashboard): new interface v2
Example 3: refactor(app-shell/app-shell-eezee): minor refactoring

> Include `prefix` of path level 1 is sufficient. 
> E.g. the paths configured inside `tsconfig.json`. 

# Breakdown:

1. feat:                    > Type of commit
<<<<<<< HEAD
2  ([prefix]/navbar)        > Scope (omit this if changes are to more than two components)
=======
2  (components/navbar)      > Scope & Type (omit this if changes are related to more than 2 things). **Not limited to components**.
>>>>>>> dbb13d42d2bd1d3422a97242401d716a472c24a1
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
- PR could be created to fix issues that come from **Canny**.
- Your teammates appreciate them as PR is easier to be reviewed.

## Tips

- Linking a PR to an issue using a keyword.

You can link a pull request to an issue by using a supported keyword in the pull request's description or in a commit message (please note that the pull request must be on the default branch).

- `close`, `closes`, `closed`, `fix`, `fixes`, `fixed`, `resolve`, `resolves`, `resolved`

## References

- [Linking a PR to an issue using a keyword](https://docs.github.com/en/issues/tracking-your-work-with-issues/linking-a-pull-request-to-an-issue#linking-a-pull-request-to-an-issue-using-a-keyword)
- [Conventional commits](https://www.conventionalcommits.org/en/v1.0.0/)
- [Docusaurus](https://github.com/facebook/docusaurus)
- [Git commit message convention that you can follow](https://dev.to/i5han3/git-commit-message-convention-that-you-can-follow-1709)

## License

MIT license