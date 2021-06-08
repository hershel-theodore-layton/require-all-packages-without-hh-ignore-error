# require-all-packages-without-hh-ignore-error
This repository typechecks all packages every day with a very strict .hhconfig file.

All packages will typecheck without any settings that make Hack less sound. These projects do not depend on `HH_IGNORE_ERROR` or similar unsafe constructs. When a setting is announced that allows you to opt-in to future behavior, and this behavior is more strict than the default, this setting can be added to .hhconfig.

Typechecking only happens on hhvm-latest and hhvm-nightly. Previous versions of hhvm require hhvm/hsl from composer. These packages include `HH_IGNORE_ERROR` comments.
