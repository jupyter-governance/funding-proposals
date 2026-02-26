# Report Template
---
## Summary of Work Completed

- Sharding for faster visual regression/integration tests ([merged](https://github.com/jupyterlab/jupyterlab/pull/18427))
- Fixes to many flaky tests and tests which were failing locally (many PRs merged), but more work to be done
- Workflow for updating visual regression snapshots from artifacts ([merged](https://github.com/jupyterlab/jupyterlab/pull/18559))

We track some of the issues and pull requests associated with this proposal in [this public GitHub project](https://github.com/orgs/jupyterlab/projects/12/views/4?sliceBy%5Bvalue%5D=visual+testing).

## Deliverables/Milestones

> Metric 1. The time to run playwright tests on the JupyterLab repo should reduce from current 45 minutes down to ~20 minutes.

Achieved: the runtime is now on the order of 15 mintues.

> Metric 2. The snapshot updates should no longer require a multi-step manual process that can be performed only by maintainers but instead allow every contributor to trigger an update of the snapshots. It should be near instantaneous (<5 minutes) once the regression testing is completed by reusing the published artifacts.

Achieved, although:
- the documentation snapshots are not yet coevered
- the workflow runs require approval while it matures

> Metric 3. >90% of tests should pass when run on a non-Ubuntu machine

Work in progress. >95% tests pass on CI between different Ubuntu versions.

## Challenges or Risks

We did not find a way to make snapshots identical without requiring an update to the existing ones.
This means that while the goal can be achieved, there will be an initial cost to migrate (update all snapshots).
This should not be too difficult and would be required when migating to new Ubuntu runners anyways.

## Budget Update

As of 20th Feb 2026 we used 7,507.50 USD out of 16,182 USD budget.

## Next Steps

- Fixing the fonts to ensure cross-platform reproducibility
- Further fixes to snapshot differences caused by local installation differences
- Merging snapshot jobs for documentation with the sharded jobs for other packages
