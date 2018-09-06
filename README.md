
# Computer Vision Bootstrap for Raspberry Pi

This is a default environment for computer vision applications written in Python. It wraps OpenCV and PiCamera for a quick start into into image analysis.

##### IMPORTANT -  This package is under construction, feel free to contribuite, open issues or contact.

### Prerequisites

* PiCamera
* OpenCV
* Matplotlib

### Usage

### Documentation
The documentation pattern is: 
- Class
 - __init__ | Class constructor
 - Methods

Classes:
- Camera
  - __init__() | This class is a singleton
  - takePhoto() | Returns an OpenCV formatted image
  - togglePreview() | Opens a window for camera image previewing
- Image
  - __init__(image, path) | If a path is inputed as parameter it loads the image from the path. Image parameter is an OpenCV image array pattern. This class is a singleton
  - show() | Plots a image for image previewing
  - save() | Saves the photo in a folder named with the current date (31/12/2018) named with the hour (21:15:24) with the extension .png
  - rotate(degrees) | Rotates an image 
- IO
  - __init__() | Setup the GPIO board, should be instanciated before other IO classes 
- Servo
  - __init__(pin) | Instanciates the servo on the pin passed as parameter
  - rotate(dutyCycle) | Rotates the servo to the according dutyCycle
- Input
  - __init__(pin, name, function) | If signal is received on pin it will trigger the function passed as parameter
- OutputClock
  - __init__(pin, name, frequency) | Instanciates the OutputClock on the pin passed as parameter with a certain frequency. This sends a square wave to simulate external input signals.
  - stop() | Stops the signal.

## Authors

* [**Leonardo Dalcin**](https://github.com/leonardodalcin) - *Initial work*

See also the list of [contributors](https://github.com/leonardodalcin/cvbootstrap/graphs/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details
