# mpv-helpers

![Lua](https://img.shields.io/badge/Lua-2C2D72?style=flat&logo=lua&logoColor=white)
![MPV](https://img.shields.io/badge/MPV-703e79?style=flat&logo=data:image/svg+xml;base64,PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0idXRmLTgiPz4KPCEtLSBMaWNlbnNlOiBBcGFjaGUuIE1hZGUgYnkgbGF3bmNoYWlybGF1bmNoZXI6IGh0dHBzOi8vZ2l0aHViLmNvbS9sYXduY2hhaXJsYXVuY2hlci9sYXduaWNvbnMgLS0+Cjxzdmcgd2lkdGg9IjgwMHB4IiBoZWlnaHQ9IjgwMHB4IiB2aWV3Qm94PSIwIDAgMTkyIDE5MiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIiB4bWw6c3BhY2U9InByZXNlcnZlIiBpZD0iTGF5ZXJfMSIgeD0iMCIgeT0iMCIgc3R5bGU9ImVuYWJsZS1iYWNrZ3JvdW5kOm5ldyAwIDAgMTkyIDE5MiIgdmVyc2lvbj0iMS4xIj48c3R5bGU+LnN0MCwuc3Qxe2ZpbGw6bm9uZTtzdHJva2U6IzAwMDAwMDtzdHJva2Utd2lkdGg6MTI7c3Ryb2tlLW1pdGVybGltaXQ6MTB9LnN0MXtzdHJva2Utd2lkdGg6Nn08L3N0eWxlPjxjaXJjbGUgY3g9Ijk2IiBjeT0iOTYiIHI9Ijc0IiBjbGFzcz0ic3QwIi8+PHBhdGggZD0iTTExMi44IDk0LjEgODUuNSA3OC40Yy0xLjQtLjktMy40LjItMy40IDEuOXYzMS41YzAgMS42IDEuOSAyLjggMy40IDEuOUwxMTIuNyA5OGMxLjUtMSAxLjUtMy4xLjEtMy45eiIgY2xhc3M9InN0MCIvPjxjaXJjbGUgY3g9Ijk2IiBjeT0iOTYiIHI9IjM5IiBjbGFzcz0ic3QxIi8+PGNpcmNsZSBjeD0iOTgiIGN5PSI5Mi40IiByPSI1Mi41IiBjbGFzcz0ic3QxIi8+PC9zdmc+)

Collection of lua helpers I use in my MPV scripts.

## confhelper.lua

Config file installer and loader helper.

### What it does:

This helper installs automatically for the user the relative .conf file for the script in the correct script-opts directory.  
If .conf file is present, it loads it.

The scripts also does a bit of error handling and supports Windows, Mac and Linux systems.

### Usage:

1. Place the helper in your script directory.
2. Place the "your_script_name".conf in that same directory: this will act as the default template for the script config file which will be copied in the correct script-opts directory by the helper.
3. In your script:
```lua
local options = require("confhelper").run(""your_script_name"", {
    example_option1 = example_value1,
    example_option2 = example_value2,
    ...
})
```
**Note**: You only need the options table you create using the helper in step 3: The helper will also load it so no need to manually use `require("mp.options").read_options`.

## Support

If you encounter any problems or have suggestions, please [open an issue](https://github.com/ExiledEye/mpv-helpers/issues).

## License

Copyright (c) 2026 Exiled Eye  
This project is licensed under the MPL-2.0 License.  
Refer to the [LICENSE](LICENSE) file for details.
