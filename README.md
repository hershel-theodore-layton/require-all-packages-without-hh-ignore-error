# require-all-packages-without-hh-ignore-error
This repository typechecks all packages every day with a very strict .hhconfig file.

All packages will typecheck without any settings that make Hack less sound. These projects do not depend on `HH_IGNORE_ERROR` or similar unsafe constructs. When a setting is announced that allows you to opt-in to future behavior, and this behavior is more strict than the default, this setting can be added to .hhconfig.

Typechecking only happens on [hhvm version 4.128](https://hhvm.com/blog/2021/09/21/hhvm-4.128.html), hhvm-latest, and hhvm-nightly. Previous versions of hhvm either require hhvm/hsl from composer (which includes `HH_IGNORE_ERROR` directives) or do not work out of the box with composer 2.2.
