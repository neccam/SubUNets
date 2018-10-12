## TODO
* ~~Upload Models to Dropbox and update the download model link~~
* ~~Upload Prototxt Files~~
* Write unified evaluation script.

# SubUNets
This repo contains the caffe models, prototoxt files and the evaluation scripts from Camgoz et al's ["SubUNets: End-to-end Hand Shape and Continuous Sign Language Recognition"](http://www.cihancamgoz.com/pub/camgoz2017iccv.pdf) (ICCV'17).

## Requirements
* Download and compile the custom caffe-ctc developed by [ChWick](https://github.com/ChWick/caffe/tree/ctc) including pyCaffe. 
* Download and extract [One-Million-Hands](https://www-i6.informatik.rwth-aachen.de/~koller/1miohands-data/) dataset.
* Download and extract [RWTH-PHOENIX-Weather 2014: Continuous Sign Language Recognition Dataset](https://www-i6.informatik.rwth-aachen.de/~koller/RWTH-PHOENIX/) dataset.
* Download and install [TensorFlow](https://www.tensorflow.org/) 1.3.0+ (TF is used for beam search decoding. Tested with TF 1.3) 
* Download models using the script `Models\download_models.sh`

## Usage
`python evaluate.py --model <model_name> --phoenix_dir </path/to/phoenix/2014/> --one_mil_dir </path/to/one/mil/hands/>`

Models which require `phoenix_dir` to be set
* `WordSubUNet-FullFrame-SingleLayer`
* `WordSubUnet-FullFrame-TwoLayer`
* `WordSubUnet-HandFrame-TwoLayer`
* `SignSubUNets-Expert`
* `SignSubUNets-Generic`

Models which require `one_mil_dir` to be set
* `HandSubUNets` 

## Reference
Please cite the paper below if you use this code in your research:

    @inproceedings{camgoz2017subunets,
      author = {Necati Cihan Camgoz and Simon Hadfield and Oscar Koller and Richard Bowden},
      title = {SubUNets: End-to-end Hand Shape and Continuous Sign Language Recognition},
      booktitle = {IEEE International Conference on Computer Vision (ICCV)},
      year = {2017}
    }
