# FabGL — Roy Antaw’s fork

## About this fork and repository navigation

This is Roy Antaw's fork of [fdivitto/FabGL](https://github.com/fdivitto/FabGL), an ESP32 library. The original project description and attribution follow below. Treat board support and examples as belonging to this snapshot; consult upstream before assuming support for a newer ESP32 variant or Arduino core.

## Getting started

Install this checkout as an Arduino library using the workflow supported by your Arduino environment. The [library.properties](library.properties) and [library.json](library.json) files contain package metadata. Select a compatible ESP32 board, then open an example and follow its wiring notes before compiling/uploading. VGA, PS/2 and audio examples depend on the appropriate external hardware.

| Location | Purpose |
| --- | --- |
| [src/](src/) | Library implementation and headers |
| [examples/](examples/) | Arduino sketches and example-specific instructions |
| [docs/](docs/) | Bundled documentation |
| [tools/](tools/) | Supporting utilities |
| [images/](images/) | Documentation images |
| [CONTRIBUTING.md](CONTRIBUTING.md) | Existing placeholder; no contribution procedure is documented |
| [LICENSE](LICENSE) | Project licence |

Keep `src/`, `examples/` and package metadata in their current positions: the Arduino/library packaging tools expect this structure.

---

## Original project guide
### VGA Controller, PS/2 Mouse and Keyboard Controller, Graphics Library, Sound Engine, Graphical User Interface (GUI), Game Engine and ANSI/VT Terminal for the **ESP32**

**[Please look here for full API documentation](http://www.fabglib.org)**

If you would like to **support FabGL's development**, please see the [**Donations page**][Donations].


This library works with ESP32 revision 1 or later. See [**Compatible Boards**][Boards].

VGA output requires a digital-to-analogue converter (DAC): three 270-ohm resistors provide 8 colours, or six resistors provide 64 colours.

Three fixed-width fonts are included for 80×25 or 132×25 text screens at 640×350 resolution. Other fonts are also included, including variable-width fonts.

Sprites can have up to 64 colors (RGB, 2 bits per channel + transparency).
A sprite has one or more associated bitmaps, which may have different sizes. Bitmaps (frames) can be selected in sequence to create animations.
There is no fixed limit on the number of sprites. Large sprites or large numbers of sprites reduce the frame rate and may cause flickering.

When sufficient memory is available, for example at 320×200 resolution, two screen buffers can be allocated for double buffering.
In this case drawing primitives always draw on the back buffer.

Except for double buffering or when explicitly disabled, all drawings are performed on vertical retracing, so no flickering is visible.
If the drawing queue is not processed before vertical retracing ends, processing resumes at the next retrace.

There is a graphical user interface (GUI) with overlapping windows and mouse handling and a lot of widgets (buttons, editboxes, checkboxes, comboboxes, listboxes, etc..).

Finally, there is a sound engine, with multiple channels mixed to a mono output. Each channel can generate sine waveforms, square, etc... or custom sampled data.



### Space Invaders Example (click for video):

[![Everything Is AWESOME](https://img.youtube.com/vi/LL8J7tjxeXA/hqdefault.jpg)](https://www.youtube.com/watch?v=LL8J7tjxeXA "")

### Graphical User Interface - GUI (click for video):

[![Everything Is AWESOME](https://img.youtube.com/vi/84ytGdiOih0/hqdefault.jpg)](https://www.youtube.com/watch?v=84ytGdiOih0 "")

### Sound Engine (click for video):

[![Everything Is AWESOME](https://img.youtube.com/vi/RQtKFgU7OYI/hqdefault.jpg)](https://www.youtube.com/watch?v=RQtKFgU7OYI "")

### Altair 8800 emulator - CP/M text games (click for video):

[![Everything Is AWESOME](https://img.youtube.com/vi/y0opVifEyS8/hqdefault.jpg)](https://www.youtube.com/watch?v=y0opVifEyS8 "")

### Simple Terminal Out Example (click for video):

[![Everything Is AWESOME](https://img.youtube.com/vi/AmXN0SIRqqU/hqdefault.jpg)](https://www.youtube.com/watch?v=AmXN0SIRqqU "")

### Network Terminal Example (click for video):

[![Everything Is AWESOME](https://img.youtube.com/vi/n5c27-y5tm4/hqdefault.jpg)](https://www.youtube.com/watch?v=n5c27-y5tm4 "")

### Modeline Studio Example (click for video):

[![Everything Is AWESOME](https://img.youtube.com/vi/Urp0rPukjzE/hqdefault.jpg)](https://www.youtube.com/watch?v=Urp0rPukjzE "")

### Loopback Terminal Example (click for video):

[![Everything Is AWESOME](https://img.youtube.com/vi/hQhU5hgWdcU/hqdefault.jpg)](https://www.youtube.com/watch?v=hQhU5hgWdcU "")

### Double Buffering Example (click for video):

[![Everything Is AWESOME](https://img.youtube.com/vi/TRQcIiWQCJw/hqdefault.jpg)](https://www.youtube.com/watch?v=TRQcIiWQCJw "")

### Collision Detection Example (click for video):

[![Everything Is AWESOME](https://img.youtube.com/vi/q3OPSq4HhDE/hqdefault.jpg)](https://www.youtube.com/watch?v=q3OPSq4HhDE "")




[Donations]: https://github.com/fdivitto/FabGL/wiki/Donations
[Boards]: https://github.com/fdivitto/FabGL/wiki/Boards
