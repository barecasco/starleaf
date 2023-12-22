# starleaf
trying to count some palm crowns

## Installation
- pip install -U ultralytics
- pip install pandas

Ultralytics will bring along cv2 and numpy.

## Assets download

OneDrive link:
https://1drv.ms/f/s!AhpCTMCuij4fmzkZrrlJnQ0NqwP4?e=JiLxtt

- please find the model "model_last.pt" in OneDrive and put it in the root.
- please find the test movie "drone_trim.mov" in OneDrive and put it in test_data folder.


## Quickstart

The notebook predict.ipynb will take a truncated movie file (of drone.mov) from test_data folder and generate two things:

- A movie called result.avi contained bounding round and the count of trees for each frame.
- A csv consisting of the counted trees is stored in count_history.csv is generated.


## The Model

- The YOLO model was trained using separate environment where CUDA is available.
- The training images are splitted images from drone.mov frames, approximated to 640 x 640 per slice.
- The training used polygonal annotation to get better separation performance.
- We used 100 epochs where obtained mAP is about 0.7.
