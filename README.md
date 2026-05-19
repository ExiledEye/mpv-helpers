# mpv-helpers

![License: MPL 2.0](https://img.shields.io/badge/License-MPL_2.0-brightgreen.svg)
![Lua](https://img.shields.io/badge/Language-Lua-blue.svg)
![MPV](https://img.shields.io/badge/Player-MPV-purple.svg)

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
