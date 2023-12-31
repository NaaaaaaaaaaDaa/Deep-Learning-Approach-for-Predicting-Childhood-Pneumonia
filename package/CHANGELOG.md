## [5.0.0] - 2023-02-10
### BREAKING CHANGES
- run and runString now return a promise instead of a using a callback.
- You will need to 1) check the return value, 2) remove the callback argument, and 3) change to a promise
- see readme for usage examples

### Other notes
- I confirmed that python-shell works with python 3.11 and node v18.

## [4.0.0] - 2023-02-10
### Changed
- run and runString now return a promise instead of a using a callback.
- This is somewhat backwards compatible with previous behavior

## [3.0.1] - 2021-10-09
### Fixed
- Previously when you called the kill method the terminated attribute was always set to true, regardless of whether the process was actually killed. Now the terminated boolean is set to true if kill succeeds, false otherwise. [#255](https://github.com/extrabacon/python-shell/issues/255)

## [3.0.0] - 2021-03-07
### Changed
- **BREAKING** Default python path changed back to `python` on Windows. [#237](https://github.com/extrabacon/python-shell/issues/237)
- **BREAKING** `error` event renamed to `pythonError` event. [#118](https://github.com/extrabacon/python-shell/issues/118)
- **BREAKING** `receive` methods removed in favor of `splitter` arguments in the constructor. This lets the default splitting logic reside in a reuseable stream transformer. Now if you have extra pipes you can reuse `newlineTransformer` to split incoming data into newline-seperated lines.

### Added
- `error` event that is fired upon failure to launch process, among other things. [#118](https://github.com/extrabacon/python-shell/issues/118)

## [1.0.8]
### Fixed
- @joaoe fixed a bug with pythonshell not working with unset std streams
- https://github.com/extrabacon/python-shell/milestone/9

## [1.0.7]
### Changed
- default python path updated to py on windows

## [1.0.4]
### Added
- added getVersionSync

## [0.0.3]
### Fixed
- fixed buffering in `PythonShell.receive`, fixing [#1](https://github.com/extrabacon/python-shell/issues/1)

## [0.0.2]
### Changed
- improved documentation

## [0.0.1]
### Added
- initial version
- independent module moved from [extrabacon/pyspreadsheet](https://github.com/extrabacon/pyspreadsheet)

