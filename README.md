# Trying to Suck Less (WIP)

Describe some best practices used in my projects.

## 1. Workflow

- Follow the [Github Flow](https://guides.github.com/introduction/flow/).
- Follow the [Git Rebase Workflow](https://randyfay.com/content/rebase-workflow-git).
- Follow the [Successful Git Branch Model's](http://nvie.com/posts/a-successful-git-branching-model/) branch naming conventions.

## 2. Coding Best Practices

- Use [Yarn](http://yarnpkg.com) to manage dependencies.
- Use English on the codebase.
- Write [readable](https://youtu.be/56mETnrByBM) and [S.O.L.I.D.](https://scotch.io/bar-talk/s-o-l-i-d-the-first-five-principles-of-object-oriented-design) code.

## 3. Code Style

- Use [EditorConfig](https://editorconfig.org/)
  - helps maintain consistent coding styles for multiple developers working on the same project across various editors and IDEs.
  - Rules are configured on [`.editorconfig`](https://editorconfig-specification.readthedocs.io/)
- Use [Prettier](https://prettier.io/)
  - Takes care of code formatting
  - Rules are configured on [`.prettierrc.yml`](https://prettier.io/docs/en/configuration.html)
- Use [ESLint](https://eslint.org/)
  - Takes care of linting rules
  - Rules are configured on [`.eslintrc.yml`](https://eslint.org/docs/developer-guide/shareable-configs)
- Use [Saas Lint](https://www.npmjs.com/package/sass-lint)
  - Linter for both sass and scss syntax
  - Rules are configured on [`.sass-lint.yml`](https://github.com/sasstools/sass-lint/tree/master/docs/options)
- Use [LintHTML](https://www.npmjs.com/package/@linthtml/linthtml)
  - An unofficial html5 linter and validator
  - Rules are configured on [`.linthtmlrc.yml`](https://github.com/linthtml/linthtml#rules)
- Use [Markdown Lint](https://www.npmjs.com/package/markdownlint-cli)
  - Style checker and lint tool for Markdown/CommonMark files
  - Rules are configured on [`.markdownlint.yml`](https://github.com/DavidAnson/markdownlint#configuration)

### Code Style Changes

1. To propose a new rule or a code style change, firstly open a pull request
2. On the PR title:
   - A summary of the change
3. On the PR description:
   - Describe the problem you want to solve.
   - Your take on the correct solution to the problem.
   - Any relevant resource that would endorse such a change
4. Add a commit providing 2-3 examples for the proposed solution
   - Preferably on a real code
5. Request the review for the change for teammates
6. Being approved by 51% of the teammates:
   - Configure the rule properly;
   - Apply the rule on the whole codebase on the project;
   - And the PR follows the regular Pull Request flow; YAY!

## 4. Testing

- Write unit tests with [Jest](https://jestjs.io/).
- Write E2E tests with [Cypress](https://www.cypress.io/).
- Apply the [Better Specs](http://www.betterspecs.org/) best practices for testing - as much as possible.

## 5. GIT

### 1. General Guidelines

- Follow the [Conventional Commits](https://conventionalcommits.org/)
- Commit [often](https://sethrobertson.github.io/GitBestPractices/#sausage_metaphor)
- Keep commits small and [atomic](https://www.freshconsulting.com/atomic-commits/)
- Write [S.O.L.I.D.](https://youtu.be/e9K1gHYIE2c) commits
- Write meaningful titles targeting for non-technical readers
- Write commits that would help the [Code Review](#8-code-reviews)
- Add any extra information that would help the [Code Review](#8-code-reviews)
- Reference the [issue](https://help.github.com/en/articles/autolinked-references-and-urls) that originated the commit
