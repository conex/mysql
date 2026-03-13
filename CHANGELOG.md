# Changelog

## [Unreleased]

### Changed
- Updated default image from `mysql:latest` to `mysql:8`
- Increased default `MySQLUpWaitTime` from 15 to 30 seconds (MySQL 8 takes longer to initialize)
- Added nil config check
- Updated to use Go modules
