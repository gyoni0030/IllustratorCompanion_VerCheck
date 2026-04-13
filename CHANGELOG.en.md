# Changelog - Illustrator Companion / Illustrator Companion EX

## [0.9.4] - 2026-04-13
### Changed
- Changed the global hotkey combination for switching Adobe apps to avoid potential misbehavior in Illustrator

## [0.9.3] - 2026-04-13
### Added
- Added a tooltip to the main menu button that displays update details when an update is available
- Added a link to the author's X profile in the About window
### Changed
- Improved support to ensure the app functions correctly with the active (foreground) Illustrator window, even when multiple versions of Illustrator are running simultaneously
- Improved stability when the app cannot communicate with Illustrator. The app now retries the connection internally and notifies the user when recovery is not possible
- Refactored the internal processing for app switching to improve stability and optimize memory management
### Fixed
- Fixed an issue where update notifications were sometimes displayed even though the app was already up to date
- Fixed an issue where the caret could move to an incorrect XYWH field when the XYWH caret target was set to the Control panel and shape information was visible
- Fixed an issue where script execution notifications were not displayed on the correct display in multi‑display setups
- Fixed an issue where Illustrator's foreground detection could become inaccurate when switching apps via Task View
- Fixed an issue where clicking the main menu button to close the menu caused it to reopen instead
- Fixed an issue where pressing Esc or Enter in the search box caused an unexpected system beep
- Fixed an issue where clicking the launcher's search box or main menu button while Illustrator was not in the foreground did not bring Illustrator to the front
- Fixed an issue where pressing ESC in the search field after launch, before changing the category, always caused the category to revert to the default
- Fixed an issue where the category edit dialog opened in an inactive state
- Fixed an issue where selecting "> Edit Categories..." from the category list sometimes failed to open the category edit dialog and instead inserted the item text into the search box
- Fixed an issue where the Options or About windows could be opened multiple times from the notification area icon menu

## [0.9.2] - 2026-03-31
### Added
- Added partial-match search (live filter) for script names in the category box
- Added an option to choose whether to delete script files when removing a registered script or performing an app reset
- Added a dialog accessible from the main menu to view script execution logs (up to 100 entries, with copy support)
- Added a feature that displays the script name and note text as a tooltip
- Extended the script comment tag system to support min/max numeric values and tooltips for argument descriptions
### Changed
- Changed the behavior for long script names so they now show an ellipsis when truncated
- Removed the script caching feature as it provided little practical benefit
- Updated bundled sample scripts to reflect the latest tag specifications and fixed minor issues
### Fixed
- Fixed an issue where some jsxbin scripts could produce errors at runtime due to the method used to send scripts from the launcher to Illustrator
- Fixed an issue where scripts could be dragged to invalid positions when category filtering was active
- Fixed an issue where the original shortcut could remain active after assigning a new one
- Fixed an issue where only the category header was restored at startup and the script filter was not applied
- Fixed an issue where windows created by a script would appear behind the launcher when the script was executed by double-clicking
- Fixed an issue where this app's shortcuts could trigger on other applications if Illustrator failed to become active right after this app started

## [0.9.1] - 2026-03-23
### Added
- Added automatic character encoding detection for script files (.jsx), enabling correct loading in UTF-8 or Shift_JIS
- Added an optional script execution cache
- When re‑registering (overwriting) a script, user‑defined argument values are now preserved
- Scripts that include the #include directive can now run as long as their dependent files exist in the correct relative paths
- Added links to the official website, privacy policy, and changelog on the About screen
### Fixed
- Fixed an issue where scripts saved in Shift_JIS could appear garbled when loaded

## [0.9.0] - 2026-03-21
### Added
- Added support for dragging and dropping folders when registering scripts
- Added support for the “.jsxbin” extension when registering scripts
- The auto-restore maximization feature now also works when the Illustrator window is unintentionally restored from maximized state by slightly dragging its title bar
- Added a confirmation message when removing scripts from the launcher
### Changed
- Improved performance and state detection accuracy of the auto-restore maximization option
- Reorganized the options UI
- Improved wording of some messages
### Fixed
- Fixed an issue where the window would be automatically maximized when resizing it while not maximized with the auto-restore maximization option enabled
- Fixed an issue where, when the XYWH caret target was set to the Control panel, caret movement shortcuts could become unresponsive or move to an incorrect field
- Fixed an issue where argument UI for scripts not included in the selected category would remain visible after changing categories
- Fixed an issue where the current category would reset to default after editing categories
- Fixed an issue where execution results and other information could disappear at inappropriate timing
- Fixed an issue where the launcher size would become smaller on the next launch if the app was closed in window shade state
- Fixed an issue where unregistered scripts in the managed script folder could not be added to the launcher

## [0.8.0] - 2026-03-15 Preview Release
