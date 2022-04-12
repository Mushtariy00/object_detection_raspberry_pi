# TensorFlow Lite Python object detection example with Raspberry Pi

This example uses [TensorFlow Lite](https://tensorflow.org/lite) with Python on
a Raspberry Pi to perform real-time object detection using images streamed from
the Pi Camera. It draws a bounding box around each detected object in the camera
preview (when the object score is above a given threshold).


## Download the example files

First, clone this Git repo onto your Raspberry Pi like this:

```
git clone https://github.com/Mushtariy00/object_detection_raspberry_pi.git
```

Then use our script to install a couple Python packages, and download the
EfficientDet-Lite model:

```
cd object_detection_raspberry_pi
```
# The script install the required dependencies and download the TFLite models.
```
sh setup.sh
```

In this project, all you need from the TensorFlow Lite API is the `Interpreter`
class. So instead of installing the large `tensorflow` package, we're using the
much smaller `tflite_runtime` package. The setup scripts automatically install
the TensorFlow Lite runtime.

# Run the object detection sample
```
python detect.py
```
####
### If you see an error running the sample:
ImportError: libcblas.so.3: cannot open shared object file: No such file or directory
you can fix it by installing an OpenCV dependency that is missing on your Raspberry Pi.
```
sudo apt-get install libatlas-base-dev
```
### Run the custom object detection 

```
python3 detect.py --model your_model.tflite
```
## Thank you


