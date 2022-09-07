# My Personal Blog

## Summary
This project uses [MkDocs](https://www.mkdocs.org/) to build a static site in a ["Read the Docs"](https://docs.readthedocs.io/en/stable/intro/getting-started-with-mkdocs.html) style/format.

## About the CI/CD Pipeline
Uses GitHub Actions to orchestrate the following flow:
1. PRs will be held for review, where changes to file(s) will be visually checked.
2. Once approved, a staging instance will become available for previewing via a web browser.
3. Once approved, updates will be pushed to the production environment, where changes will be made live and viewable at [https://blog.kevinharper.com](https://blog.kevinharper.com)

## Contributing
### Dev Environment
The development environment is a simple Python setup that requires:
* Python 3+
* pip
* pipenv

To contribute:

1. Fork this repository to your personal GitHub account.
2. Clone your repository.
3. cd into the repository's directory.
4. Set this repository as the upstream (keeping your fork as the origin).
5. Create a branch that follows naming convention defined in "Branches" section below.
6. pipenv shell
7. Make your changes and test/verify all looks good (mkdocs serve)
	- Ctrl-C to kill server
8. When satisfied with your edits, generate the static pages: mkdocs build
9. Push your commit to your fork.
10. Initiate a PR from your forked repository.

### Branches
* \<issue-id\>-feature-\<feature-slug\>
	- ex: 3-feature-site-search
	- for developing new features
	- exists as long as feature is in development
* \<issue-id\>-bugfix-\<bugfix-slug\>
	- ex: 3-bugfix-pagination
	- used when fixing bugs
* \<issue-id\>-hotfix-\<hotfix-slug\>
	- ex: 3-hotfix-update-title-fonts
	- for unplanned production updates
*\<issue-id\>documentation-\<documentation-slug\>
	- ex: 3-documentation-readme
	- used when updating project-related documentation
