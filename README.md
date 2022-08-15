# Flir Image Extractor

This small Python library allows to extract the thermal sensor values converted to temperatures for every pixel in a FLIR thermal image.

## Installation

In addition to installing the package, this tool relies on `exiftool`.

```bash
apt-get update -y
apt-get install exiftool -y
pip install sparrow-flir
```

## Usage

```python
from sparrow_flir import ThermalExtractor

thermal = ThermalExtractor().process_image("examples/flir_example.jpg")
print(thermal.min(), thermal.max())

# Expected result
# 25.94827128142373 62.32026276916025
```

## Credits

Raw value to temperature conversion is ported from this R package: https://github.com/gtatters/Thermimage/blob/master/R/raw2temp.R
Original Python code from: https://github.com/Nervengift/read_thermal.py
