Malte:

Forking https://github.com/javl/image2cpp to fit my personal style more better. I need a way to create header files that look like

//--------------------------------------------------------------
// Includes
//--------------------------------------------------------------
#include <inttypes.h>
#include "main.h"

//--------------------------------------------------------------
// Image-Daten
// erstellt von UB mit ImageGenerator 1.3
// Image-Settings : Farbe = 16bit [RGB565 - R5G6B5]
// Source-File    : Unbenannt.bmp
//--------------------------------------------------------------
const uint16_t picture_Image_Table[] = {
0xFFF....
}

//--------------------------------------------------------------
// Image-Struktur
//--------------------------------------------------------------
picture bild_Image = {
  picture_Image_Table, // Image-Daten
  222,         // width(in Pixel)
  284,         // height  (in Pixel)
  RGB565,       // colorspace
};

which uses a struct like
typedef struct picture_t
{
  const uint16_t *table; // Tabelle mit den Daten
  uint16_t width;        // Breite des Bildes (in Pixel)
  uint16_t height;       // Hoehe des Bildes  (in Pixel)
  uint8_t colorspace;
}picture;

I removed the original describtion. Please visit and support
http://javl.github.io/image2cpp/
Also check here the ppl thats

License is untouched:


### License
image2cpp is released under GPL v3. This means you can use the project in any way you want (use, adapt, distribute, etc.) as long as you share any changes and link back to this repo. See [LICENSE.md](https://github.com/javl/image2cpp/blob/master/LICENSE.md) for more info.
