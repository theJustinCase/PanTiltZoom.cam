# Changelog

All notable changes to the PanTiltZoom app are documented in this file.

## [2.0.5] - Unreleased

### Changed

- Improved camera discovery to include port.

## [2.0.4] - 2026-06-04

### Added

- New OTA update interface with options to view changelog and decline updates.
- Better update transparency with additional OTA information in app diagnostics and About.
- Snapshot retry option for preset images.
- Custom segmented switch UI with a wide-border variant for settings controls.

### Changed

- App config import confirmation now more clearly explains what will change.
- App config import now checks for invalid settings
- Camera communication handling improved for more reliable response matching and retries.
- Improved Sony VISCA-over-IP support with better response correlation, retry behavior, and command reliability.
- Motion command completion can now resolve on ACK for improved control responsiveness.
- Zoom and focus inputs now use feedback-based coalescing to reduce command flooding.
- Camera connection gating now relies on successful ping or camera response before marking a connection as healthy.
- Preset labels now add stronger text contrast over image backgrounds.
- Replaced the external segmented-control dependency with the in-app SegmentedSwitch implementation.

### Fixed

- Multiple startup and connection edge cases that could trigger duplicate camera connect attempts.
- Stability issues around discovery/network socket cleanup in error scenarios.
- Zoom and focus error-handling edge cases.
- Fixed bug that would create invalid presets if the camera didn't respond correctly
- Rare crash when rapidly tapping controls while switching cameras could tear down a connection mid-handshake.
- Suppressed spurious error reports when a camera was offline at app startup.
- Suppressed spurious error reports when a camera command timed out from a quick joystick, zoom, focus, or preset tap.
- Connection deadlock and write-command registration race conditions that could stall camera communication.
- Sony VISCA-over-IP setter reliability by serializing setters and safely absorbing late post-ACK frames.
- Unhandled ping failure exceptions and false-positive connect success when cameras did not actually respond.
- Control-flow edge case when accessing controls during camera switching.
- Simultaneous joystick + zoom toggle behavior and zoom polling limitations.
- Preset save/import robustness by rejecting invalid VISCA inquiry payloads and scrubbing invalid migrated preset data.

## [2.0.3] - 2026-04-08

### Changed

- Improvements to the import/export option for saved cameras and presets.

## [2.0.2] - 2026-04-05

### Added

- Import/export option for saved cameras and presets.

## [2.0.1] - 2026-03-07

### Changed

- Improved camera communication speed and responsiveness.

### Fixed

- Bug fixes across camera communication and control workflows.

## [2.0.0] - 2024-05-18

### Added

- Automatic scene snapshot or custom image for preset backgrounds.
- Control of camera settings like exposure and color.
- On-screen display menu control.
- Increased recall positions to 16.
- UDP protocol support for many more cameras.

### Changed

- Overall camera communication and compatibility improvements.

### Fixed

- Reliability fixes across camera discovery and control workflows.

## [1.1.2] - 2018-04-30

### Added

- Left/Right controls can now lock manual movement to horizontal for easier follow shots without accidental vertical movement.

### Changed

- Apple platform update to improve overall app functionality and stability.

### Fixed

- Manual focus for individual cameras now stays persistent when leaving the app or switching cameras and returning.
- Minor settings bug fixed when launching the app for the first time.
- Fixed a crash that could occur when closing Settings after starting new camera setup.
- Axis lock behavior finalized and made more reliable across camera switches and app background/foreground transitions.

## [1.1.1] - 2018-04-10

### Changed

- Updated compatibility with newer NDI firmware.

### Fixed

- Improved reliability when returning from background by reloading controls and handling connection state more cleanly.
- Improved preset behavior when selecting another preset before the first movement completes.
- Improved zoom command handling during active camera movement.

## [1.1.0] - 2018-03-13

### Added

- Control up to 8 cameras.
- Save up to 13 presets.
- iPhone X support.
- New option to specify the VISCA address.

### Changed

- Improved settings layout.
- Cleaner, simplified Settings button view.

### Fixed

- Additional bug fixes and control improvements.

## [1.0.2] - 2017-10-23

### Added

- Updated app artwork and control graphics.

### Changed

- Smoother gradual speed changes during manual control.
- Additional Settings polish for sliders and control buttons.

### Fixed

- Fixed crashes some users experienced after long periods of inactivity.

## [1.0.1] - 2017-06-12

### Added

- New options for customizing manual and preset camera speeds.
- Expanded touch area for camera controls to make operation easier without looking at the screen.

### Changed

- Improved iPad Pro UI.
- Better default values for newly added cameras.

### Fixed

- Additional bug fixes across settings and camera controls.
- Improved pause/resume behavior so movement can be stopped cleanly without resetting the control interface.
- Additional settings and controller default-value fixes.

## [1.0.0] - 2017-05-18

### Added

- Initial public release.
