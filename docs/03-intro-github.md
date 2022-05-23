# Intro to GitHub



- GitHub is a Git web server, there are others e.g., [GitLab](https://about.gitlab.com/)
- Your repositories will be stored on GitHub, and you will clone them to your machine to work on them (or work on them in Gitpod)
- Under your user account you see the repos you are owner of

- On GitHub OpenSAFELY is an organization
  - The repos are owned by the organization so they show up under the organisation [here](https://github.com/opensafely)
    <img src="img/os-github-org.png" width="771" />

## GitHub PAT for R

- To create a GitHub Personal Access Token (PAT) to be allowed more downloads from GitHub per hour run in R  

```r
install.packages("usethis")
library(usethis)
create_github_token()
```

## GitHub CLI

- GitHub CLI stands for command line interface for operating GitHub
- Installation instructions are [here](https://github.com/cli/cli#readme)
- But I don't recommend using this
