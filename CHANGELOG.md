# Changelog

## v0.7

### Breaking Changes:
- `Style::new()` now takes an `Into<Cow<'static, str>` instead of
  `Into<String>` and returns `stylist::Error` instead of `String` when
  encountering an error.
- `Style::create()` now takes `AsRef<str>` for class prefix and
  `Into<Cow<'static, str>>` for css string and returns `stylist::Error`
  instead of `String` when encountering an error.

### Other Changes:
- Fixed a Bug where `.a-class-name` is after `@media` would cause parser
  to return an error.
- Removed Unnecessary Clones.
- Optimised for Performance.


## v0.6

### Breaking Changes:
- `style.get_class_name()` no longer consumes the style and returns a `&str`
  instead of an owned string.
- Seed Integration is Removed.

### Other Changes:
- Added `Style::new` which does not require a component name.
- Aesthetically pleasing Class Name.
- Replaced `lazy_static` with `once_cell`.
- Updated nom to `v6`.
- Updated Yew to `v0.18`.
- Removed Unnecessary Clones.
- Optimised for Performance.