# ESP-IDF SSD1306 Component

This repository refactors [nopnop2002/esp-idf-ssd1306](https://github.com/nopnop2002/esp-idf-ssd1306) into a standalone ESP-IDF component. The goal is to enable the use of the SSD1306 OLED display driver as a git submodule for ESP-IDF projects.

## Prerequisites

Make sure that you have the ESP-IDF environment set up. If you don't, you can follow the steps provided by Espressif at the [official ESP-IDF documentation](https://docs.espressif.com/projects/esp-idf/en/latest/esp32/get-started/index.html).

## Installation

To use the SSD1306 driver as a submodule in your ESP-IDF project, perform the following steps:

1. Navigate to your project's directory.

```
cd YOUR_PROJECT_DIRECTORY
```

2. Add the SSD1306 repository as a submodule.
```
git submodule add https://github.com/Krzyshio/esp-idf-ssd1306 components/ssd1306
```

3. Initialize and update your submodules.
```
git submodule init
git submodule update
```

4. Include the SSD1306 driver in your code:
```
#include "ssd1306.h"
```

## Usage
To use the SSD1306 driver, refer to the header file ssd1306.h for the API documentation. Here is an example:
````
SSD1306_t dev;
ssd1306_init(&dev, 128, 64); // Initialize the SSD1306 device with 128x64 resolution.
ssd1306_display_text(&dev, 0, "Hello, world!", 13, false); // Display text on the screen.
````
## Contributing
Please feel free to submit issues and pull requests, we welcome all contributions.

## License
This project is licensed under the MIT License. See the LICENSE file for details.
Acknowledgements

This driver is based on the work by [nopnop200](https://github.com/nopnop2002)