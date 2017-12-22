The library is available in header conmanip.h in the conmanip namespace. There are various types and functions available that are described below.

# Enumerations
The following enumerations are defined:
* `console_text_colors` defines the available colors for the text
* `console_bg_colors` defines the available colors for the background. The colors for text and background are actually the same, however they are represented by different underlying values as defined by the console APIs.
* `console_type` defines the available (standard) consoles: input, ouput and error
* `console_modes` defines a set of console modes (used by the [SetConsoleMode](http://msdn.microsoft.com/en-us/library/windows/desktop/ms686033(v=vs.85).aspx) function). You can use any combination of
  * `echo`: when set (which is the default) characters typed are visible in the console; when disabled, they are not; the disabled mode is useful when a user needs to enter a password for instance.
  * `overwrite`: when enabled a new character typed in the console overwrites the last character (is displayed in the same position)
  * `hide_ctrl_c`: when enabled, CTRL+C is processed by the system and is not placed in the input buffer
  * `enable_mouse_selection`: enables selection in the console with the mouse
* `console_cleanup_options`: defines the options for restoring the (modified) settings of a console. You can use any combination of:
  * `none`: nothing is restore
  * `restore_pos`: only the position of the text is restored
  * `restore_attibutes`: only the text attributes (colors) are restored
  * `restore_mode`: only the console mode is restored
  * `restore_buffsize`: only the buffer size is restored
  * `restore_all_nopos`: all settings except for the position are restored
  * `restore_all`: all settings are restored
