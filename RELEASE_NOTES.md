### 3.1.0

	General:

	* Fixed problem where OpenGL 3.2 contexts where created using the wrong flags, causing renderdoc error (#790).
	* Fixed problem where Vector3.Transform(Quaternion) returned incorrect results ( #776 ).
	* SDL backend no longer handles exceptions thrown in input events ( #735 #737 )
	* Updated gamepadd mappings for SDL (#927).
	* Alt + numpad now results in correct data being passed to OnKeyPress (f17fa4b).

	Windows:

	* Keypress events are using CharSet.Unicode to allow for UTF characters.
	* If GetMouseMovePointsEx returns "access denied" we fall back to the old mouse move handling ( #883 ).
	* Detect joysticks which declare no valid controls & ignore (Cherry-picked from #819 ).
	* Fix where an invalid joystick axis overwrites the first joystick axis. (Cherry-picked from #819 ).
	* Makes the ArbCreateContext return valid settings ( #754 ).

	MacOS:

	* Unprocessed events no longer put the application into a partially-activated state ( #732 ).
	* Multiple fixes under PR #914:
	* NativeWindow.CursorVisible no longer resets the mouse position ( #668 ).
	* Custom cursors should work now ( e598ab2 ).
	* Command key is now a valid modifier ( 286119e ).
	* Fix where KeyDown events would trigger KeyPress when they shouldn't, e.g. when pasting ( ea3dd48 ).
	* KeyPress now receives the correct keycodes even if modifiers where held when typing ( 91b03dd ).

  	Internal:

	* Generator.Build now uses invariant culture for parsing avoiding an exception when the local system uses comma as decimal separator ( #750 ).
	* Removed weird assembly version check fixing #710.
	* Fixed Xamarin project so that it compiles ( See #725 and b16e7fa ).
	* Matrix4 uses unsafe to invert for performace ( #719 ).
	* Removed link to gitter chat, discord is where it's at ( #770 ).

### 3.0.1
    * Hotfix release
    * Fixed an issue with vector transformation

### 3.0.0
    * Final .NET Framework release
    * Numerous bug fixes

### 3.0.0-pre
	* Support for OpenGL 4.6
	* Replaced JoystickButton enum with simple long. (breaking API change)
	* Increase available joystick buttons to 64.
	* Add support for OpenGL ES3 through Angle + DIrect3D.
	* Fix 2 crashes on android
	* Move to built-in System.Diagnostics.Debug for Android + iOS
	* Fix for certain joysticks returning invalid HID pages.
	* Fix for certain joysticks with negative axis range being inverted.
	* Fix Xbox controller D-pad on windows
	* Fix joystick hat position sticking on Linux
	* Enhance xbox button detection to include GUIDE button.
	* Fix iOS GL bindings issue introduced by 2ea8334
	* Fix crash on setting time to <= 0 for iOS + Android.
	* Several minor XML documentation fixes and enhancements
	* Fix for angle backbuffer size issue on window resize
	* Possible fix for broken GLControl package.

### 2.0.0
	* Moved to new FAKE/Paket based build system
	* Removed superfluous release configurations
	* Numerous other fixes and enhancements
