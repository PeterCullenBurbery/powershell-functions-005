# Changelog

All notable changes to this project will be documented in this file.

## [2.0.0] - 2025-007-025@002.029 PM

- I moved PowershellFunctions005 from https://github.com/PeterCullenBurbery/powershell-modules to https://github.com/PeterCullenBurbery/powershell-functions-005. URL has been updated accordingly.

## [1.9.0] - 2025-007-024@002.021 PM

- Added Clean-Path function to normalize and deduplicate the system PATH. This function expands environment variables, removes blank entries, removes case-insensitive duplicates, and broadcasts the updated environment block. Clean-Path complements Add-ToPath and Remove-FromPath by ensuring overall cleanliness of the PATH variable.

## [1.8.2] - 2025-007-021@001.044 PM

- Updated GUID. GUID was the same as PowershellFunctions@https://www.powershellgallery.com/packages/PowershellFunctions/.

## [1.8.1] - 2025-007-021@11.38 AM

- Adds enforcement to block PowerShell 7+ from importing the module. A PSEdition and version check was added to the top of the .psm1 file to prevent accidental usage in PowerShell Core (Powershell 7).

## [1.8.0] - 2025-007-021@11.04 AM

- This release locks the module to Windows PowerShell 5.1 only. Fixes an issue with 0 bytes files. Before, Get-FileSizeHumanReadable "C:\empty-folder" would return " bytes". Now Get-FileSizeHumanReadable "C:\empty-folder" returns "0 bytes".

## [1.7.3] - 2025-007-018@10.06 PM

- Removed C# components. StartProcessLongFilePath was not working so I removed it.

## [1.7.2] - 2025-007-018@3.35 PM

- Update release notes.

## [1.7.1] - 2025-007-018@3.30 PM

- Removed Start-ProcessLongFilePath from the module. The DLL-based cmdlet was deemed too complex.

## [1.7.0] - 2025-007-018@1.51 PM

### Added

- Added Start-ProcessLongFilePath, a wrapper for a C#-based cmdlet that launches processes using paths exceeding Windows MAX_PATH limitations. Useful for deeply nested folders or long file names. Includes support for optional arguments.

## [1.6.0] - 2025-007-017@5.19 PM

### Added

- Added Enable-LongFilePaths to programmatically enable support for file paths longer than 260 characters. The function checks the current registry value and only modifies it if necessary.

## [1.5.0] - 2025-007-015@4.22 PM

### Added

- Add-ToPath and Remove-FromPath now automatically call `refreshenv` if available, updating the current session immediately after modifying the system PATH.

## [1.4.0] - 2025-007-015@2.08 PM

### Added

- Added Get-PowershellPath to display the PATH environment variable in a zero-padded, indexed table. Uses Format-Table for clear formatting and supports inspection of system path entries.

## [1.3.0] - 2025-007-015@10.50 AM

### Added

- Added Add-DefenderExclusion to exclude folders from Microsoft Defender. Automatically excludes the parent folder if a file is specified. Requires administrator privileges.

## [1.2.0] - 2025-007-015@8.59 AM

- Fixed Add-ToPath and Remove-FromPath to correctly resolve relative paths (e.g., ".") using Resolve-Path. Improves reliability when modifying system PATH from any location.

## [1.1.0] - 2025-007-014@8.26 PM

### Added

- Added Bring-BackTheRightClickMenu and Use-Windows11RightClickMenu to toggle classic and default context menus in Windows 11. Improved tagging and documentation.


## [1.0.0] - 2025-007-014@4.16 PM

- Initial release: includes time zone resolution, ISO week and ordinal date formatting, File Explorer restart, and PowerShell version capability detection.