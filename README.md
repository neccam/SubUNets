# SubUNets
These are the caffe models, prototoxts and evaluation script from Camgoz et al's ["SubUNets: End-to-end Hand Shape and Continuous Sign Language Recognition"](http://www.cihancamgoz.com/pub/camgoz2017iccv.pdf) (ICCV'17).

## Requirements
* Download and compile the custom caffe-ctc developed by [ChWick](https://github.com/ChWick/caffe/tree/ctc). 
* Download and extract [One-Million-Hands](https://www-i6.informatik.rwth-aachen.de/~koller/1miohands-data/) dataset.
* Download and extract [RWTH-PHOENIX-Weather 2014: Continuous Sign Language Recognition Dataset](https://www-i6.informatik.rwth-aachen.de/~koller/RWTH-PHOENIX/) dataset.

## Usage
python evaluate.py --model <model_name> --hand_path <phoenix2014 resized hand images path> --fullframe_path <full_frame_path>

model_names:
HandSubUNets: 
WordSubUnets-


## Reference
Please cite the paper below if you use this code in your research:

    @inproceedings{camgoz2017subunets,
      author = {Necati Cihan Camgoz and Simon Hadfield and Oscar Koller and Richard Bowden},
      title = {SubUNets: End-to-end Hand Shape and Continuous Sign Language Recognition},
      booktitle = {IEEE International Conference on Computer Vision (ICCV)},
      year = {2017}
    }
