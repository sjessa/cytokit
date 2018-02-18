[![Build Status](https://travis-ci.com/sjessa/cytokit.svg?token=ckZxkx4uN2RZSSwsdpLM&branch=master)](https://travis-ci.com/sjessa/cytokit)

# cytokit
Internal Kleinman Lab toolkit for analyzing single cell RNA-seq data


## Installation

#### Hydra/Cedar/Guillimin

To use `cytokit` on Hydra or Guillimin, you can simply load it with `library(cytokit)` in R,
as it's already installed in the Kleinman lab spaces. To update the version on the server, you can use the instructions below.

#### Locally

Since the repo is private, there are a couple steps to install `cytokit`:

1. Install [`devtools`](https://cran.r-project.org/web/packages/devtools/)
2. Generate a personal access token on Github here: https://github.com/settings/tokens  
    Generate new token > Type in "cytokit" in *Token description* > Tick the checkbox for "repo" > Generate token (green button)  
   Your token will be a string of letters and numbers, e.g. `abc123`. (For more details on these tokens, see the [GitHub documentation](https://help.github.com/articles/creating-a-personal-access-token-for-the-command-line/))
3. Install `cytokit` and include the token as an argument:

```r
devtools::install_github("sjessa/cytokit", auth_token = "abc123")

```

## Getting help

You can look up the documentation for any `cytokit` function from the R console:
```r
?cytokit::ggColours
```

Some functions will specify the author in the documentation.

## Contribution

#### The first time

Clone the repository and create a development branch:
```bash
git clone https://github.com/sjessa/cytokit.git
cd cytokit
git checkout -b dev-selin
```

Make changes locally on your branch and commit them. Then, push your changes:
```bash
git push -u origin dev-selin
```

5. On the GitHub website, create a pull request, to merge changes in your dev branch with the master branch.

### From now on

From now on, to continue working on the package, first merge the latest changes from the master branch:
```bash
git checkout dev-selin # This command switches to your dev branch
git merge master # Merge changes from master branch onto dev-selin
```

(There is a more sophisticated way of doing this, called rebasing: https://www.atlassian.com/git/tutorials/merging-vs-rebasing)
