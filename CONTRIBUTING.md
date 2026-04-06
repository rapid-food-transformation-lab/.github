# Contributing to Rapid Food Transformation Lab repositories

Thank you for your interest in contributing. This document covers how external contributors can work with repositories in this organisation.

## Who can contribute

Most repositories in this organisation are either private (active research) or public read-only archives (published reproduction packages). Direct write access is granted only to members of the lab's internal teams.

If you are a trusted long-term collaborator, you may be added to the `@external-collaborators` team — contact the lab to discuss. Short-term or one-off contributions are handled via outside collaborator access at the individual repository level.

## Raising issues

If you find a problem with a published reproduction package — a broken workflow, a missing dependency, an error in documented output — please open an issue in the relevant repository. Include:

- the repository name and a link to the specific file or step
- the error message or unexpected behaviour
- your operating system, R or Python version, and relevant package versions

For questions about the research itself, contact the lab directly through the [Oxford Martin School](https://www.oxfordmartin.ox.ac.uk).

## Submitting changes

If you have been given write access to a repository:

- Work on a feature branch; do not commit directly to `main`
- Keep commits small and descriptive
- Open a pull request with a brief explanation of the change and why it is needed
- One of the `@core-admin` or `@research-leads` team will review

For reproduction packages, changes that affect numerical outputs must include a note on whether and why results differ from the published paper.

## Code style

- R: follow the [tidyverse style guide](https://style.tidyverse.org)
- Python: follow [PEP 8](https://peps.python.org/pep-0008/); use `black` for formatting
- All documentation in UK English
- Each repository includes a `CLAUDE.md` at its root — read it before contributing, as it contains project-specific context, data locations, and pipeline entry points

## Licensing

Unless otherwise stated, code in public repositories is released under the MIT licence. Data and written content may carry separate licences — check the individual repository for details.
