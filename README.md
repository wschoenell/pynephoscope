# pynephoscope
A python software suite for cloud detection in all-sky camera images.

## requirements

- PyQt
- astropy
- pyephem
- scipy
- numpy
- pandas
- OpenCV
- pyserial

## run

- make sure you have dependencies installed
- run pyuic on the ui files:

```
    pyuic5 image_view.ui -o image_view_ui.py
    
    pyuic5 main.ui -o main_ui.py
    
    pyuic5 settings_view.ui -o settings_view_ui.py   
```

- grab a star catalog compatible with [XEphem EDB format](https://www.mmto.org/obscats/edb.html#mozTocId468501) like [this one](https://github.com/borogove/viewplan/blob/master/SKY2k65.edb).
- make a mask image for your camera, example:
![original](https://raw.githubusercontent.com/wschoenell/pynephoscope/master/docs/mask_original.jpg)
![mask](https://raw.githubusercontent.com/wschoenell/pynephoscope/master/docs/mask.png)

- edit the configuration in configuration.py
- calibrate (for Stars method) by running calibration.py
![calibration](https://raw.githubusercontent.com/wschoenell/pynephoscope/master/docs/calibrate.png)

- run main.py for the UI or any of the other scripts
![main](https://raw.githubusercontent.com/wschoenell/pynephoscope/master/docs/main.png)