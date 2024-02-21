# Change log

All notable changes to the project will be documented in this file. For full release notes for the projects that depend on this project, see their respective changelogs. This file describes changes only to the common code. This project adheres to [Semantic Versioning](http://semver.org).

## [1.1.0](https://github.com/launchdarkly/dotnet-logging-adapter-nlog/compare/1.0.1...1.1.0) (2024-02-21)


### Features

* Raise minimum .NET Framework version to 4.6.2 ([#10](https://github.com/launchdarkly/dotnet-logging-adapter-nlog/issues/10)) ([912e244](https://github.com/launchdarkly/dotnet-logging-adapter-nlog/commit/912e244698a8cca75d3dce9d632676d64f747f00))
* Update dependencies to allow using NLog v5. ([f6ba29d](https://github.com/launchdarkly/dotnet-logging-adapter-nlog/commit/f6ba29ded2e8b817db796b5c2edd87b7a0c88dc2))
* Update dependencies to allow using NLog v5. ([d817628](https://github.com/launchdarkly/dotnet-logging-adapter-nlog/commit/d8176289d12a46b82ae3402694b858aa0b5f607e))

## [1.0.1] - 2021-05-20
### Changed:
- Updated dependencies on `LaunchDarkly.Logging` to version 1.0.1.

After the 1.0.1 release, the code was moved out of the previous monorepo into its own repository at https://github.com/launchdarkly/dotnet-logging-adapter-nlog. There were no code changes to the package, and the NuGet package name (`LaunchDarkly.Logging.NLog`) is unchanged.

## [1.0.0] - 2021-02-02
Initial release of this package.
