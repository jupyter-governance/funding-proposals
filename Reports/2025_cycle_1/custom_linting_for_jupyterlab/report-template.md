# Report Template
---
## Summary of Work Completed

- ESLint plugin with custom rules was created https://github.com/Darshan808/eslint-plugin-jupyter
- ESLint upgrade to v9 is in progress https://github.com/jupyterlab/jupyterlab/pull/18434

## Deliverables/Milestones

- Goal: develop and maintain custom ESLint rules tailored to the JupyterLab/Notebook codebase.
   - The plugin now exists, is pending transfer to JupyterLab-governed repository
- Impact Metric: Adoption of the additional rules by the community
    - Multiple community members expressed interest in adopting the eslint
      plugin during the Feb 25th 2026 Jupyter Community Call

## Challenges or Risks

- Security vulnerabilities in ESlint v8 forced an early migration to v9.
  As a consequence the early work aimed at making the plugin compatible with
  both versions was shelved in favour of prioritising migration of JupyterLab
  codebase to the newer version.

## Budget Update

As of 20th Feb 2026 we used 330 USD out of 17,496 USD budget.

## Next Steps

- Transition the ESLint plugin to the JupyterLab organization
- Expansion of new bespoke rules based on the discussions tracked in JupyterLab repository issues
- Tightening of existing rules in JupyterLab, extension-template and Notebook repositories