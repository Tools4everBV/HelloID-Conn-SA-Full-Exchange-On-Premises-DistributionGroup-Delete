# Changelog

All notable changes to this project will be documented in this file. The format is based on [Keep a Changelog](https://keepachangelog.com/), and this project adheres to [Semantic Versioning](https://semver.org/).

## [2.0.0] - 2026-08-21

### Changed

- Improved naming consistency: Changed "Exchange On-Premise" to "Exchange On-Premises" throughout all resources
- Enhanced error handling with detailed line-by-line error reporting and action context tracking
- Refactored code structure with improved parameter splatting for better readability
- Optimized session management with explicit command imports to reduce overhead
- Updated form category from "Exchange On-Premise" to "Exchange On-Premises"

### Added

- TLS 1.2 explicit configuration for secure communications
- Selective property loading in data source to optimize performance and reduce memory usage
- SkipRevocationCheck parameter in session options for improved session reliability
- Enhanced search functionality supporting SamAccountName in addition to existing criteria
- Action message context for better error tracking and debugging
- Comprehensive inline documentation and comments
- Functions region placeholder for future extensibility

### Fixed

- Corrected inconsistent naming between form and task resources
- Improved credential object creation with explicit type casting

## [1.0.0] - 2023-08-18

### Added

- Initial release for deleting Exchange On-Premises Distribution Groups
- Basic search functionality for distribution groups by name, alias, and display name
- Connection to Exchange On-Premises using remote PowerShell
- Audit logging for create, delete, and error operations
- All-in-one setup script for automated form deployment
- Support for global variables (ExchangeConnectionUri, ExchangeAdminUsername, ExchangeAdminPassword)
