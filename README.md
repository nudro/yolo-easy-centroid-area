# yolo-easy-centroid-area
Modification of ultralytics yolov5 script to draw centroids and find largest person on frame.

Largest person is in green, smaller detections are in orange. Blue centroids indicate center of the box.

<img src=./example.png width=500>

## Requirements

Head to the `ultralytics` Github repo: https://github.com/ultralytics/yolov5

```
git clone https://github.com/ultralytics/yolov5  # clone
cd yolov5
pip install -r requirements.txt  # install
```

This will install Yolov5.

## Run inference

Swap out `detect.py` for the existing `detect.py` in the official Yolo repo. Swap out `plots.py` under `utils/plots.py` for the current official `plots.py`.

Run detection as usual:

```
# set classes==0 for only persons, otherwise all classes will be detected
python detect.py --weights yolov5s.pt --source video.mp4 --classes 0
```
