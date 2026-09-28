# Code report

The code report gives a short, sourced summary of a project.

## Inputs

- A repository link from GitHub, GitLab or Bitbucket.
- An optional npm or PyPI package name.
- An optional code excerpt (up to 20.000 characters) for code observations.

## Sources

| Source    | What is collected                                                                                                               |
| --------- | ------------------------------------------------------------------------------------------------------------------------------- |
| GitHub    | Description, stars, forks, open issues and pull requests, licence, languages, top contributors, recent releases, recent commits |
| GitLab    | Description, stars, forks, languages, recent releases, recent commits (public projects)                                         |
| Bitbucket | Description, main language, dates, recent commits (public repositories)                                                         |
| npm       | Latest version, licence, number of versions, downloads in the last month                                                        |
| PyPI      | Latest version, number of versions, downloads in the last month                                                                 |

Results are cached for 10 minutes. When a source cannot be reached, the report says so instead of filling the gap.

## Report structure

1. **Verified facts**: written by the studio from source data, never by the AI. Each line links to its source.
2. **Interpretation**: written by AI from those facts: summary, activity and maintenance, code observations and suggested next steps.

Dates use DD/MM/YYYY and numbers use European formatting.
