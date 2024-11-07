# Install FixedIT CLI action for Github Actions
An action for Github Action that installs the FixedIT CLI tool to make Axis ACAP development and CI/CD easier.

This tool can be used to build ACAP applications, inspect/verify `.eap` package files and create new applications from templates.

For use in GitHub Actions, see also:
* [build-eap-action](https://github.com/fixedit-ai/build-eap-action)
* [test-eap-action](https://github.com/fixedit-ai/test-eap-action)

If no version of FixedIT CLI is specified, the latest release version will be used. To make builds deterministic, we recommend pinning both the action version and the FixedIT CLI package version, e.g.:
```yml
- name: Install FixedIT CLI and login
  uses: fixedit-ai/install-fixeditcli-action@v2
  with:
    token: ${{ secrets.FIXEDIT_TOKEN }}
    fixeditcli-version: "0.5.0"
```
