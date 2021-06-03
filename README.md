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

## Features and bugs

Please file feature requests and bugs at the [issue tracker][tracker].

[tracker]: https://github.com/20fifty/20Fifty_linter/issues
