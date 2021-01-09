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

## 5. Git: General Guidelines

- Follow the [Conventional Commits](https://conventionalcommits.org/)
- Commit [often](https://sethrobertson.github.io/GitBestPractices/#sausage_metaphor)
- Keep commits small and [atomic](https://www.freshconsulting.com/atomic-commits/)
- Write [S.O.L.I.D.](https://youtu.be/e9K1gHYIE2c) commits
- Write meaningful titles targeting for non-technical readers
- Write commits that would help the [Code Review](#8-code-reviews)
- Add any extra information that would help the [Code Review](#8-code-reviews)
- Reference the [issue](https://help.github.com/en/articles/autolinked-references-and-urls) that originated the commit

## 6. Git: Commit Messages

- Follow the [How to Write a Git Commit Message](http://chris.beams.io/posts/git-commit/) tips
- Follow the [5 Useful Tips For A Better Commit Message](https://robots.thoughtbot.com/5-useful-tips-for-a-better-commit-message) tips
- Consider using [Commitizen cli](http://commitizen.github.io/cz-cli/)

### 1. Follow [The seven rules of a great Git commit message](https://chris.beams.io/posts/git-commit/)

1. [Separate subject from the body with a blank line](https://chris.beams.io/posts/git-commit/#separate)
2. [Limit the subject line to 50 characters](https://chris.beams.io/posts/git-commit/#limit-50)
3. [Capitalize on the subject line](https://chris.beams.io/posts/git-commit/#capitalize)
4. [Do not end the subject line with a period](https://chris.beams.io/posts/git-commit/#end)
5. [Use the imperative mood in the subject line](https://chris.beams.io/posts/git-commit/#imperative)
6. [Wrap the body at 72 characters](https://chris.beams.io/posts/git-commit/#wrap-72)
7. [Use the body to explain what and why vs how](https://chris.beams.io/posts/git-commit/#why-not-how)

## 7. Git: Tools

- Use [Commit Lint](https://commitlint.js.org/#/) to lint the commit messages
- Must configure rules on [`.commitlintrc.yml`](https://commitlint.js.org/#/reference-configuration)
- Rules must contain the following types:
  - **feat**: A new feature
  - **fix**: A bug fix
  - **docs**: Documentation only changes
  - **style**: Changes that do not affect the meaning of the code _(white-space, formatting, missing semi-colons, etc)_
  - **ref**: A code change that neither fixes a bug nor adds a feature
  - **test**: Adding missing tests or correcting existing tests
  - **revert**: A commit that reverts a previous commit
  - **chore**: Changes to the build process or auxiliary tools and libraries such as documentation generation
  - **ci**: Changes to our CI configuration files and scripts _(example scopes: Circle, BrowserStack, SauceLabs)_
  - **build**: Changes that affect the build system or external dependencies _(example scopes: gulp, broccoli, npm)_
  - **perf**: A code change that improves performance
  - **git**: Changes on git files, such as [`.gitignore`](https://git-scm.com/docs/gitignore)
 
## 8. Git: Pull Requests

One would say that some of the primary purposes of Pull Requests are:

- Add a product increment
- Remove obsolete code/behaviour
- Fix a product problem
- Enhance product behaviour
- Refactor code to improve quality
- Add/change some architecture requirement
- Update libraries or improve security
- Discuss the better approach to specific issues

### 1. The ideal PR should be:

1. As smallest as possible
2. Defects free
3. Easy to be reviewed and validated
4. Reviewed and validated as soon as possible
5. Merged as quickly as possible
6. Have been approved by at least one reviewer

### 2. Best Practices

1. Prefer one feature/fix/refactoring per PR
2. Estimate the PR before starting it
3. Link the PR to an Issue before starting it
4. Comment any consideration/doubt/problem/discussion/definition on the PR`s Issue;
5. Try to have, at least, one Unit Tests per change, when applicable
6. Try to make a PR that you would enjoy reviewing
7. Remember, the next reviewer can be you

### 3. Before sending the PR to Code Review ensures that

1. Any implementation follows the Coding Best Practices and any team `Style Guide.`
2. Any commit follows the Commit Best Practices
3. Any change has been tested at least once. That is:
   - Running the program
   - Checking if the changes work properly
4. All project's Unit Tests are keeping running
5. There are no linter violations on the project
6. You have reviewed your own code

### 4. To Get Better Code Reviews ensures that

1. The PR has:
   - The minimum changes necessary to accomplish the PR's goal
   - The minimum essential commits to achieving the PR's goal
   - A clear, short and concise title that summarizes the changes
   - A clear description that contextualizes the problem you're solving
2. Any relevant explanation or reference is present on the PR's description or commits;
3. Whenever necessary, the PR describes how it must be validated
    - Adding any relevant data to the validation, such as: 
      - username, environment, password, deadline, etc.
4. Avoid refactoring not related to the PR's goal
   - Because it might difficult the Code Review
   - However, if the refactoring is inevitable
     - It should be adequately isolated and justified
