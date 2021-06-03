# 20Fifty Linter

This is the linter package used for 20Fifty Flutter projects, 
this project relies in [pedantic](https://pub.dev/packages/pedantic) internally and is simply the 
implementation of it used within our projects to more easily 
maintain standards across projects.

## Using the Lints

To use the lints add a dev_dependency in your `pubspec.yaml`:

```yaml
dev_dependencies:
  twentyfifty_linter:
      git:
       url: git@github.com:20fifty/20Fifty_linter.git
       ref: main
```

then, add an include in your `analysis_options.yaml`. If you want to always
use the latest version of the lints, add a dependency on the main
`analysis_options` file:


```yaml
include: package:twentyfifty_linter/analysis_options.yaml
```

If your continuous build and/or presubmit check lints then they will likely
fail whenever a new version of `package:twentyfifty_linter` is released. To avoid this,
specify a specific version of `analysis_options.yaml` instead:

```yaml
include: package:twentyfifty_linter/analysis_options.[VERION_NUMBER].yaml
```

# Updating

When updating the lint rules, please ensure to create a versioned `analysis_options.[VERSION_NUMBER].yaml` file,
this allows us to use version pinning in projects mor easily to minimize the impact on other
projects, also this ensure that should we had projects over to clients, they are then not impacted
by updates in our process, we can then pin them to the latest version that project was using
and they can choose weather or not to update or abandon our preferences.

Also ensure to update `CHANGELOG.md` with what has changed to make it easier 
for those implementing to gauge the impact of updating.

## Features and bugs

Please file feature requests and bugs at the [issue tracker][tracker].

[tracker]: https://github.com/20fifty/20Fifty_linter/issues
