## 1.0.0

* Initial release

## 1.0.1

* Fixed issue when deleting a texture while binding a new one

## 1.0.2

* Fixed build issue when using without windowing enabled

## 1.0.3

* Fixed negative overflow issue where monitor size is misdetected or less than window size

## 1.0.4

* No longer specifies core profile for GL 2.0 (fixes issue on Macs)

## 1.0.5

* Setting multisampling level to 16 by default

## 1.0.6

* Ensure event loop gets woken up when redrawing on Windows

## 1.0.7

* Fix error on some platforms due to GL shader program validation

## 1.1.0

### New APIs

* `WindowCreationOptions::with_resizable()`
* `WindowCreationOptions::with_always_on_top()`
* `WindowCreationOptions::with_maximized()`
* `WindowCreationOptions::with_decorations()`
* `Graphics2D::create_image_from_file_path()`
* `Graphics2D::create_image_from_file_bytes()`
* `GLRenderer::create_image_from_file_path()`
* `GLRenderer::create_image_from_file_bytes()`
* `GLRenderer::new_for_gl_context()`, to create a `GLRenderer` from a GL loader function

### Other changes

* `Graphics2D::draw_image()` is now able to take a tuple as a position
* When creating an image from raw bytes, the number of bytes is checked
* Fixed texture load issues where the horizontal byte stride was not a multiple of 4

## 1.1.1

* Now works correctly in Wayland
* Fixed error when primary monitor is not found

## 1.1.2

* Fixed issue with lines under text when a dark background and antialiasing are used

## 1.2

### New APIs

Thanks to [Revertron](https://github.com/Revertron):

* `Graphics2D::set_clip()`
* `ModifiersState::default()`

## 1.3

* WebGL support introduced

### New APIs

* `WebCanvas`, providing full rendering and event handling for an HTML canvas
* `GLRenderer::new_for_web_canvas_by_id()`, for rendering only (no event handling)
* The `time` module, for access to the system clock in a cross-platform way.

### New callbacks

* `WindowHandler::on_mouse_grab_status_changed()`
* `WindowHandler::on_fullscreen_status_changed()`

## 1.3.1

* Ensure that mouse position is scaled using device pixel ratio

## 1.4.0

* Line breaks (`\n`) now handled when laying out text

### New APIs

* `WindowHandler::on_mouse_wheel_scroll()` (thanks to [GreatGodOfFire](https://github.com/GreatGodOfFire))
* `TextLayout::empty_line_vertical_metrics()`

## 1.5.0

* Ability to draw polygons (thanks to [chilipepperhott](https://github.com/chilipepperhott))