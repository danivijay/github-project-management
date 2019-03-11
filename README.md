# My Project Management Conventions and Guidelines

This project coveys complete guidelines to setup a development environment and project management from scratch.

## Workflow: GitFlow

- Install and use `gitflow` plugin for VSCode to create branches
- `master` branch should be production ready
- `feature` branch should be merged only to `develop` branch

Read more: https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow

## Naming Conventions

### Common Prefixes

- `feat`: feature
- `bug`: bug
- `chore`: no production code change
- `test`: tests
- `refactor`: refactor
- `try`: experimental
- `junk`: temporary, or should be removed

**Commits and Pull Requests should use Common Prefixes**

_Inspired by: <http://karma-runner.github.io/3.0/dev/git-commit-msg.html>_

### Labels

These are default labels available,
- `bug`: Something isn't working
- `good first issue`: good for newcomers
- `help wanted`: Extra attention is needed
- `invalid`: This doesn't seem right
- `question`: Further information is requested
- `wontfix`: This will not be worked on

Plus, 
- `feature`: New feature or request (renamed `enhancement`)
- `ui`: UI and styling changes

### Issues

- Should be in **Title Case**
- Should add `Project`, `Labels`, `Assigned to`, and `Milestones`(if available)
- Description should contain sufficient information and images

_Eg: feat(about-us): Add About Us Page_

### Projects

- Automated Kanban with Reviews (fully automated, no manual intervension needed)

### Branches

- Always use `gitflow` plugin for vscode to create branches
- Create a new branch for each and every feature and fixes, as instructed in `GitFlow`
- Use **lisp-case** _Eg: `about-us`_

### Commits

- Use prefix followed by `(<scope>)`, if available
- `(scope)` should be followed by `: ` (colon and space)
- Should be in `lisp case`
- Should be self descriptive
- May contain title, body and footer
- Title should not be greater than 72 charactors
- Always add title and footer, body is optional
- In footer, add `contributes` or `fixes` accordingly and followed by issue name with `#` as prefix, _Eg: `fixes #123`
- Use imperative, present tense: "change" not "changed" nor "changes"

_Eg:_
```
feat(about-us): add about us design

add body and images, responsive design

fixes #123
```

### Pull Requests (PR)

- Use prefix followed by `(<scope>)`, if available
- `(scope)` should be followed by `: ` (colon and space)
- Should be in small letters
- Should add `Assigned to`, `Labels` and `Milestones`
- Don't add `Projects`
- Use imperative, present tense: "change" not "changed" nor "changes"
- In description, add `contributes` or `fixes` accordingly and followed by issue name with `#` as prefix, _Eg: `fixes #123`

_Eg: `feat(about-us): add about us page`_

## Additional Information

### Code editor: VSCode

Download: https://code.visualstudio.com/

#### Configuration:
```
{
      "editor.minimap.enabled": false,
      "prettier.tabWidth": 6,
      "prettier.singleQuote": true,
      "prettier.arrowParens": "always",
      "prettier.trailingComma": "all",
      "prettier.eslintIntegration": true,
      "prettier.printWidth": 150,
      "editor.formatOnSave": true,
      "editor.renderWhitespace": "none",
      "breadcrumbs.enabled": true,
      "editor.formatOnSaveTimeout": 1000000,
      "window.zoomLevel": 0,
      "workbench.startupEditor": "newUntitledFile",
      "workbench.sideBar.location": "right",
      "todo-tree.defaultHighlight": {},
      "javascript.updateImportsOnFileMove.enabled": "always",
      "javascript.preferences.importModuleSpecifier": "non-relative",
      "typescript.updateImportsOnFileMove.enabled": "always",
      "typescript.preferences.importModuleSpecifier": "non-relative"
}
```

_Project specific configurations : <https://gist.github.com/danivijay/fce3ae8d44c88fcbfbd313a86f3fa002>_

#### Extensions:

- Bracket Pair Colorizer
- ES7 React/Redux/GraphQL/React-Native snippets
- ESLint
- Git Extension Pack
- gitflow
- Highlight Matching Tag
- Live Server
- npm intellisense
- Path intellisense
- Prettier - Code formatte
- TODO Highlight
- VS Live Share
