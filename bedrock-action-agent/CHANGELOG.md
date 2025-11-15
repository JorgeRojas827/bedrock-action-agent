# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added
- ESLint and Prettier configuration for code quality
- CI/CD pipeline with GitHub Actions
- Input validation for all required parameters
- File size limits to prevent token limit issues
- Prompt size limits with truncation warnings
- Better error handling and logging
- Security improvements and dependency management
- CHANGELOG.md for tracking changes
- SECURITY.md for security policy

### Fixed
- Fixed undeclared `comments` variable bug
- Fixed .gitignore excluding source JavaScript files
- Improved error handling for file content fetching
- Better handling of edge cases (empty responses, invalid chunks)

### Changed
- Enhanced error messages with more context
- Improved logging with timestamps
- Better handling of large files and prompts

## [0.6.0] - Previous Release

### Features
- Initial release with basic Bedrock Agent integration
- Support for PR and push event analysis
- Memory support for cross-session context
- File ignoring patterns
- Customizable prompts

