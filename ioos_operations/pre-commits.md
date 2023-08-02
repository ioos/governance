# pre-commit hooks

We recommend the use of pre-commit hooks and pre-commit-ci to reduce the burden on the maintainers.
The steps to implement both are:

1. Add a configuration `.pre-commit-config.yaml` to your project. We recommend the one from the [IOOS skeleton package](https://github.com/ioos/ioos-python-package-skeleton/blob/main/.pre-commit-config.yaml);
2. The final list of pre-commits is up to the developers but we highly recommend the use of black and ruff at least;
3. When setting pre-commit-ci the configuration should be with `no autofix` and monthly updates, to reduce merge conflicts and avoid increasing the bar for contributors.
4. The project will get monthly PRs updating the pre-commits, if it is all green anyone with merge rights can merge them b/c no code change is required or was applied. However, if they fail it may require a simple `pre-commit-ci autofix` or a more complex PR to work out that is broken due to the new versions of the pre-commits.