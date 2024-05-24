# WP.org Plugin/Theme Validator Action
[![GitHub Workflow Status](https://img.shields.io/github/actions/workflow/status/pantheon-systems/action-wporg-validator/plugin-test.yml?label=plugin%20vulnerability%20scanner&logo=wordpress)](https://github.com/pantheon-systems/action-wporg-validator/actions) [![GitHub Workflow Status](https://img.shields.io/github/actions/workflow/status/pantheon-systems/action-wporg-validator/theme-test.yml?label=theme%20vulnerability%20scanner&logo=wordpress)](https://github.com/pantheon-systems/action-wporg-validator/actions) [![MIT License](https://img.shields.io/github/license/pantheon-systems/action-wporg-validator)](https://github.com/pantheon-systems/action-wporg-validator/blob/main/LICENSE) [![GitHub release (latest by date)](https://img.shields.io/github/v/release/pantheon-systems/action-wporg-validator)](https://github.com/pantheon-systems/action-wporg-validator/releases)

A GitHub Action that runs the [WP.org Code Analysis Tool](https://github.com/WordPress/wporg-code-analysis) on your plugin or theme.

## What's this do?

The (experimental) WP.org Code Analysis Tool includes, at its core, a PHPCS ruleset that can be run on WordPress plugins or themes to validate whether the code should be accepted into the WordPress.org repository. However, the ruleset cannot simply be installed and added as a PHPCS standard because it was never built as a standalone standard. This GitHub Action installs the WP.org Code Analysis Tool and its dependencies, then simply runs the PHPCS checks with the appropriate ruleset on your plugin or theme.

## Why should I use it?

If you have a plugin or theme in the WordPress.org repository, you can add this to your build pipeline to validate your plugin or theme before cutting a release and deploying the update to WP.org. This can be used alongside and independent of any other PHPCS or code quality checks you may already have in place.

## Inputs

### `type`

**Required** The type of code to scan. Either `plugin` or `theme`.

## Example usage

```yaml
uses: pantheon-systems/action-wporg-validator@v1
with:
  type: 'plugin'
```
