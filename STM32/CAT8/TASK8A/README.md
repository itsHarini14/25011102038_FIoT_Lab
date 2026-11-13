# CAT8 — STM32 GPIO Bring-Up and Switch-Controlled LED

Board: STM32 development board (Blue Pill/Nucleo as permitted by the sheet). Configure the actual board pin mapping in CubeMX.

## Tasks
- TASKA — GPIO Input/Output: LED follows switch state.
- TASKB — Event-Based Control: one LED toggle per valid press; debounce.
- TASKC — Short Press vs Long Press: short press toggles LED; long press enters blinking mode; next short press stops blinking; long press again returns to blinking mode.

See each task folder for C starter code. The pin macros are intentionally left configurable because the sheet does not prescribe exact GPIO pins.
