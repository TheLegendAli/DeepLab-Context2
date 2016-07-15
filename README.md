## DeepLab v2

### Introduction

DeepLab is a state-of-art deep learning system for semantic image segmentation built on top of [Caffe](http://caffe.berkeleyvision.org).

It combines (1) *atrous convolution* to explicitly control the resolution at which feature responses are computed within Deep Convolutional Neural Networks, (2) *atrous spatial pyramid pooling* to robustly segment objects at multiple scales with filters at multiple sampling rates and effective fields-of-views, and (3) densely connected conditional random fields (CRF) as post processing.

This distribution provides a publicly available implementation for the key model ingredients reported in our latest [arXiv paper](http://arxiv.org/abs/1606.00915).
It also contains implementations for **all** methods reported in all our previous papers.

Please consult and consider citing the following papers:

    @article{CP2016Deeplab,
      title={DeepLab: Semantic Image Segmentation with Deep Convolutional Nets, Atrous Convolution, and Fully Connected CRFs},
      author={Liang-Chieh Chen and George Papandreou and Iasonas Kokkinos and Kevin Murphy and Alan L Yuille},
      journal={arXiv:1606.00915},
      year={2016}
    }

    @inproceedings{CY2016Attention,
      title={Attention to Scale: Scale-aware Semantic Image Segmentation},
      author={Liang-Chieh Chen and Yi Yang and Jiang Wang and Wei Xu and Alan L Yuille},
      booktitle={CVPR},
      year={2016}
    }

    @inproceedings{CB2016Semantic,
      title={Semantic Image Segmentation with Task-Specific Edge Detection Using CNNs and a Discriminatively Trained Domain Transform},
      author={Liang-Chieh Chen and Jonathan T Barron and George Papandreou and Kevin Murphy and Alan L Yuille},
      booktitle={CVPR},
      year={2016}
    }

    @inproceedings{PC2015Weak,
      title={Weakly- and Semi-Supervised Learning of a DCNN for Semantic Image Segmentation},
      author={George Papandreou and Liang-Chieh Chen and Kevin Murphy and Alan L Yuille},
      booktitle={ICCV},
      year={2015}
    }

    @inproceedings{CP2015Semantic,
      title={Semantic Image Segmentation with Deep Convolutional Nets and Fully Connected CRFs},
      author={Liang-Chieh Chen and George Papandreou and Iasonas Kokkinos and Kevin Murphy and Alan L Yuille},
      booktitle={ICLR},
      year={2015}
    }


Note that if you use the densecrf implementation, please consult and cite the following paper:

    @inproceedings{KrahenbuhlK11,
      title={Efficient Inference in Fully Connected CRFs with Gaussian Edge Potentials},
      author={Philipp Kr{\"{a}}henb{\"{u}}hl and Vladlen Koltun},
      booktitle={NIPS},
      year={2011}
    }

### Performance

*DeepLabv2* currently achieves **79.7%** on the challenging PASCAL VOC 2012 semantic image segmentation task -- see the [leaderboard](http://host.robots.ox.ac.uk:8080/leaderboard/displaylb.php?challengeid=11&compid=6). 

Please refer to our project [website](http://liangchiehchen.com/projects/DeepLab.html) for details.

### Pre-trained models

We have released several trained models and corresponding prototxt files at [here](http://liangchiehchen.com/projects/DeepLab_Models.html). Please check it for more model details.

### Python wrapper requirements

1. Install wget library for python
```
sudo pip install wget
```
2. Change DATA_ROOT to point to the PASCAL images

3. To use the mat_read_layer and mat_write_layer, please download and install [matio](http://sourceforge.net/projects/matio/files/matio/1.5.2/).

### How to run DeepLab
python run.py

please note you need to define the paths and interested model in run.py