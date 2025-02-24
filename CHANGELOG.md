<!-- markdownlint-disable no-duplicate-heading -->

# Change Log

<!-- KEEP-THIS-COMMENT -->

## v1.0.0

### Minor Changes

- Add auto-detection of Ansible files based on their content (#617) @priyamsahoo

### Bugfixes

- Update ALS to 0.10.3 (3 bugs) (#632) @ssbarnea
- Bump vscode-languageclient from 7.x to 8.x (#626) @ajinkyau
- Change extension status-bar icon (#627) @ssbarnea
- fix hyphenation README (#611) @akira6592

## v0.14.0

### Minor Changes

- Add feature to dynamically associate yaml files to `ansible` language (#600)
  @priyamsahoo

### Bugfixes

- Use new location of ansible-lint config JSON Schema (#608) @ssbarnea
- Fix the display of double `Ansible` in status-bar text (#605) @priyamsahoo
- Disable python debugger when running external commands (#603) @ssbarnea

## v0.13.0

### Minor Changes

- Allow jinja brace autocompletion (#593) @ganeshrn
- Add feature to show ansible meta data (#586) @priyamsahoo

### Bugfixes

- Update test dependencies (#577) @ssbarnea
- Update ansible-language-server (#574) @ssbarnea

## v0.12.0

### Minor Changes

- Add command to re-sync ansible inventory file (#522) @priyamsahoo

### Bugfixes

- Update ansible-language-server to 0.9.0 (#548) @ssbarnea

## v0.11.0

### Minor Changes

- Add command to re-sync ansible inventory file (#522) @priyamsahoo
- Require vscode 1.63 or newer (November 2021) (#567) @ssbarnea

### Bugfixes

- Update ansible-language-server to 0.9.0 (#548) @ssbarnea

## 0.10.0

### Minor Changes

- Add EE settings for volume mounts, container options and pull arguments (#499)
  @ganeshrn

### Bugfixes

- Upgrade ansible-language-server to 0.7.2 (#506) @ssbarnea
- Fix auto-completion for modules when documentation is not displayed
  ([ansible/ansible-language-server#330](https://github.com/ansible/ansible-language-server/pull/330))
  @fredericgiquel
- add ee service plugin path logs
  ([ansible/ansible-language-server#331](https://github.com/ansible/ansible-language-server/pull/331))
  @ganeshrn

## 0.9.0

### Minor Changes

- Add e2e test-cases for execution-environment (#459) @ganeshrn
- Change client extension entry point (#461) @ganeshrn

### Bugfixes

- Update URL of external resources (#480) @ssbarnea
- Remove Zuul schema definition from extension config (#470) @ssbarnea
- Fix e2e testing (#469) @priyamsahoo

## 0.8.1

## Bugfixes

- Add language configuration files in vsix package (#454) @ganeshrn

## 0.8.0

## Minor Changes

- Update ansible-language-server version (#434) @ganeshrn
- Add support for meta/runtime.yml and execution-environment.yml (#379)
  @ssbarnea
- Add schema for ansible-navigator configuration (#365) @ssbarnea

## Bugfixes

- Restore webpack archive (#437) @ssbarnea
- Fix jsonValidation and yamlValidation extension point (#432) @yaegassy
- Fix extension broken debug capability (#431) @ganeshrn
- Declare lextudio.restructuredtext ext as conflicting (#366) @ssbarnea

## 0.7.1

### Bugfixes

- Fixed inline encryption of multiline strings (#337) @jeinwag
- Prevented throwing an unhandled exception caused by the undefined linter
  arguments settings
  ([ansible/ansible-language-server#142](https://github.com/ansible/ansible-language-server/pull/142))
  @ssbarnea
- Implemented opening standalone Ansible files that have no workspace associated
  ([ansible/ansible-language-server#140](https://github.com/ansible/ansible-language-server/pull/140))
  @ganeshrn

## 0.7.0

### Removals

- Dropped the option to configure ansible-vault path (#318) @ssbarnea
- Dropped the option to configure ansible-playbook location (#317) @ssbarnea

### Minor Changes

- Upgraded the `@ansible/ansible-language-server` dependency to 0.3.0 (#333)
  @ssbarnea
  - Added support for nested module options (suboptions) @tomaciazek
  - Updated container cleanup logic for execution environment @ganeshrn
- Switched the default execution environment to `ansible/creator-ee:latest`
  (#331) @ganeshrn @ssbarnea
- Enabled auto-selection of the only vault-id (#298) @jeinwag

### Bugfixes

- Corrected some unspecified configurable settings (#307) @ssbarnea
- Started invoking inactive extension when running ansible-vault (#296) @jeinwag

### Documentation

- Documented the need to have an open workspace for the extension to work
  @ssbarnea

## 0.6.1

### Bugfixes

- Fix indentation when using inline vault encrypt (#288) @jeinwag

## 0.6.0

### Minor Changes

- **Feature**: Restored client-side support for working with ansible vaults
  (#177) @jeinwag
- Exposed the `ansibleServer.trace.server` option for tracing language server
  activity (#263) @yaegassy
- Upgraded language server to 0.2.6 (#284) @ssbarnea

### Bugfixes

- Fixed autocompletion of the built-in modules with EE
  (ansible/ansible-language-server#94) @ganeshrn
- Corrected `pullPolicy` setting type to string (#279) @ganeshrn
- Enabled editor suggestions for `ansible` files by default (#274) @ssbarnea

## 0.5.1

### Hotfixes

- Increased the minimum required `@ansible/ansible-language-server` version to
  0.2.5. It has added a guard for linting only playbook files with the Ansible's
  built-in syntax-check when `ansible-lint` is unavailable. This is used for
  providing the diagnostics information to the client (VS Code editor instance)
  (#259) @ganeshrn

## 0.5.0

### Major changes

The most notable change that happened was the migration to using
`@ansible/ansible-language-server` v0.2.4 via PR #142 by @tomaciazek. In
particular, this:

- Added the brand new Ansible Language Server
- Removed the support for working with the vaulted content

### Changes

- Decreased the minimal required version of VS Code to v1.48.0 (July 2020)
  (#206) @ssbarnea
- Added setting options for working with execution environments (#200) @ganeshrn
- Added a prompt to uninstall incompatible extensions (#170) @ssbarnea
- Updated the default setting value to use FQCN in autocompletion (#196)
  @priyamsahoo
- Added context menus and commands for running playbooks via `ansible-playbook`
  and `ansible-navigator run` (#137) @webknjaz

### Misc

- Made sure that the path-related settings are not being synchronized (#235)
  @ssbarnea
- Reintroduced the schema verification for the part of the known file paths
  that's been lost with the initial introduction of ansible language server in
  extension (#169) @ssbarnea
- Stopped including the unused files to vsix artifacts (#239) @ssbarnea
- Switched the debug listening port for ansible language server in the
  development mode to `6010` effectively fixing the support for unbound
  breakpoints when coding two connected projects (#212) @tomaciazek

### Docs

- Added a link to the language server repository into README (#173) @ganeshrn
- Added descriptions for the configuration settings section in README (#242)
  @ganeshrn

## 0.4.5

- Clean old violations when running the linter again

## 0.4.4

- Revalidate documents on save (#95) @ssbarnea

## 0.4.3

- Auto-add missing Ansible YAML tags like `!vault`
- Recognize Ansible files using `.yaml` extension in addition to `.yml`

## 0.4.2

- Reduce minimal version of vscode that is required (#90) @ssbarnea

## 0.4.0

- Added vaults encryption and decryption support via `ansible-vault` command
  (#78) @FlorianLaunay

## 0.3.2

- Use ansible-lint severity for VSCode diagnostics (#68) @FloSchwalm
- Match found problems to source files (#70) @FloSchwalm
- docs: added instructions on how to integrate `ansible-lint` in venv w… (#67)
  @stopendy

## 0.3.1

- docs: mention YAML tags configuration (#61) @ssbarnea
- [pre-commit.ci] pre-commit autoupdate (#55) @pre-commit-ci
- feat: add logging information (#62) @ssbarnea
- fix: advertise Microsoft Python extension as required (#54) @ssbarnea
- Create LICENSE (#52) @ssbarnea
- chore: fix pre-commit eslint dependencies (#53) @ssbarnea
- Add an explicit extension dependency on vscode-yaml (#45) @JPinkney
- Fix typo in README.md (#46) @fgierlinger

## 0.3.0

- Added file associations for common files found on Ansible and Python repos
- Added schema verification for galaxy.yml files

## 0.2.0

- Add JSON schema for Zuul CI config files
- Add JSON schema for ansible-lint config files
- Add JSON schema for molecule scenarios
- Fix badge urls for marketplace

## 0.1.0

- Enable schema verification
- Fixed screenshot markdown image url
