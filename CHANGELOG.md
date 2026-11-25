
# Changelog

All notable changes to the VFAT Linux Filesystem Diagnostic
Journaling project are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

## [Unreleased]

### Added

- Conceptual system architecture diagram.
- Structured technical documentation for filesystem instrumentation.
- Documentation of inode and FAT metadata collection.
- Documentation of persistence and synchronization mechanisms.
- Functional validation and performance evaluation methodologies.
- Technical references and academic documentation links.
- Development roadmap.
- Documentation of project limitations and verification requirements.
- GNU General Public License, version 2.

### Changed

- Restructured the README to improve technical clarity and readability.
- Corrected the repository description and technology classification.
- Consolidated build and integration instructions.
- Clarified the distinction between diagnostic journaling
  and transactional filesystem recovery.
- Standardized academic attribution and author information.
- Refined technical documentation to improve readability and consistency.

### Licensing

- Preserved the original MIT licensing notice in `LICENSE-MIT`.
- Introduced the GPL version 2 license in `LICENSE`.
- Documented existing upstream SPDX license declarations.
- Clarified the scope of upstream and original project licensing.
- Identified outstanding licensing and attribution verification requirements.

## [1.0.0] - Initial public version

### Added

- Experimental VFAT filesystem extension implemented in C.
- Integration with the Linux Kernel Library (LKL).
- Diagnostic logging of selected filesystem activity.
- Inode timestamp and FAT metadata collection.
- Append-based diagnostic journal operations.
- Storage synchronization using persistence-related operations.
- Modified FAT and VFAT filesystem source files.
- Modified LKL user-space filesystem utility.
- Original academic project specification and technical report.
- Project documentation and contribution guidelines.

### Known Limitations

- Compatible upstream LKL revision requires verification.
- Reproducible builds require further validation.
- Complete filesystem operation coverage has not been established.
- Crash-recovery guarantees have not been established.
- Automated regression testing is not yet established.
- Quantitative performance results require further validation.
- Upstream source-code licensing requires further review.

---

## References

- [Keep a Changelog](https://keepachangelog.com/)
- [Semantic Versioning](https://semver.org/)
- [Linux Kernel Documentation](https://docs.kernel.org/)
- [Linux Kernel Library](https://github.com/lkl/linux)
- [GNU General Public License v2](https://www.gnu.org/licenses/old-licenses/gpl-2.0.html)