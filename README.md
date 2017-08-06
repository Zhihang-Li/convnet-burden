convnet-burden
---

Estimates of memory consumption and FLOPS for various convolutional neural networks.    


### Image Classification Architectures

The numbers below are given for single element batches.

| model | input size | param memory | feature memory | flops |
|-------|------------|--------------|----------------|-------|
| alexnet | 227 x 227 | 233 MB | 3 MB | 727 MFLOPS|
| caffenet | 224 x 224 | 233 MB | 3 MB | 724 MFLOPS|
| squeezenet1-0 | 224 x 224 | 5 MB | 30 MB | 837 MFLOPS|
| squeezenet1-1 | 224 x 224 | 5 MB | 17 MB | 360 MFLOPS|
| vgg-f | 224 x 224 | 232 MB | 4 MB | 727 MFLOPS|
| vgg-m | 224 x 224 | 393 MB | 12 MB | 2 GFLOPS|
| vgg-s | 224 x 224 | 393 MB | 12 MB | 3 GFLOPS|
| vgg-m-2048 | 224 x 224 | 353 MB | 12 MB | 2 GFLOPS|
| vgg-m-1024 | 224 x 224 | 333 MB | 12 MB | 2 GFLOPS|
| vgg-m-128 | 224 x 224 | 315 MB | 12 MB | 2 GFLOPS|
| vgg-vd-16 | 224 x 224 | 528 MB | 58 MB | 16 GFLOPS|
| vgg-vd-19 | 224 x 224 | 548 MB | 63 MB | 20 GFLOPS|
| vgg-vd-16-reduced | 224 x 224 | 82 MB | 58 MB | 16 GFLOPS|
| googlenet | 224 x 224 | 51 MB | 26 MB | 2 GFLOPS|
| resnet-50 | 224 x 224 | 98 MB | 103 MB | 4 GFLOPS|
| resnet-101 | 224 x 224 | 170 MB | 155 MB | 8 GFLOPS|
| resnet-152 | 224 x 224 | 230 MB | 219 MB | 11 GFLOPS|
| resnext-50-32x4d | 224 x 224 | 96 MB | 132 MB | 4 GFLOPS|
| resnext-101-32x4d | 224 x 224 | 169 MB | 197 MB | 8 GFLOPS|
| resnext-101-64x4d | 224 x 224 | 319 MB | 273 MB | 16 GFLOPS|

See [here]() for more a detailed breakdown of feature extraction costs at different input image/batch sizes if needed.  

**References:**

* [alexnet](http://papers.nips.cc/paper/4824-imagenet-classification-with-deep-convolutional-neural-networks) - *Krizhevsky, Alex, Ilya Sutskever, and Geoffrey E. Hinton. "Imagenet classification with deep convolutional neural networks." Advances in neural information processing systems. 2012.*  
* [squeezenet](https://arxiv.org/abs/1602.07360) - *Iandola, Forrest N., et al. "SqueezeNet: AlexNet-level accuracy with 50x fewer parameters and< 0.5 MB model size." arXiv preprint arXiv:1602.07360 (2016).*
* [vgg-m](https://arxiv.org/abs/1405.3531) -  *Chatfield, Ken, et al. "Return of the devil in the details: Delving deep into convolutional nets." arXiv preprint arXiv:1405.3531 (2014).*
* [vgg-vd-16/vgg-vd-19](https://arxiv.org/abs/1409.1556) -  *Simonyan, Karen, and Andrew Zisserman. "Very deep convolutional networks for large-scale image recognition." arXiv preprint arXiv:1409.1556 (2014).*
* [vgg-vd-16-reduced](https://arxiv.org/abs/1506.04579) - *Liu, Wei, Andrew Rabinovich, and Alexander C. Berg. "Parsenet: Looking wider to see better." arXiv preprint arXiv:1506.04579 (2015)*
* [googlenet](http://www.cv-foundation.org/openaccess/content_cvpr_2015/html/Szegedy_Going_Deeper_With_2015_CVPR_paper.html) - *Szegedy, Christian, et al. "Going deeper with convolutions." Proceedings of the IEEE conference on computer vision and pattern recognition. 2015.*
* [resnet](https://arxiv.org/abs/1512.03385) - *He, Kaiming, et al. "Deep residual learning for image recognition." Proceedings of the IEEE conference on computer vision and pattern recognition. 2016.*
* [resnext](https://arxiv.org/abs/1611.05431) - *Xie, Saining, et al. "Aggregated residual transformations for deep neural networks." arXiv preprint arXiv:1611.05431 (2016).*

### Object Detection Architectures

| model | input size | param memory | feature memory | flops |
|-------|------------|--------------|----------------|-------|
| faster-rcnn-vggvd-pascal | 600 x 850 | 523 MB | 600 MB | 172 GFLOPS|
| rfcn-res50-pascal | 600 x 850 | 122 MB | 1 GB | 79 GFLOPS|
| rfcn-res101-pascal | 600 x 850 | 194 MB | 2 GB | 117 GFLOPS|
| ssd-pascal-300 | 300 x 300 | 100 MB | 116 MB | 31 GFLOPS|
| ssd-pascal-512 | 512 x 512 | 104 MB | 337 MB | 91 GFLOPS|


The input sizes used are "typical" for each of the architectures listed, but can be varied.  *Anchor/priorbox* generation and *roi/psroi*-pooling are not included in flop estimates.

**References:**

* [faster-rcnn](http://papers.nips.cc/paper/5638-faster-r-cnn-towards-real-time-object-detection-with-region-proposal-networks) - *Ren, Shaoqing, et al. "Faster R-CNN: Towards real-time object detection with region proposal networks." Advances in neural information processing systems. 2015..*  
* [r-fcn](https://arxiv.org/abs/1605.06409) - *Li, Yi, Kaiming He, and Jian Sun. "R-fcn: Object detection via region-based fully convolutional networks." Advances in Neural Information Processing Systems. 2016.*
* [ssd](https://link.springer.com/chapter/10.1007%2F978-3-319-46448-0_2) - *Liu, Wei, et al. "Ssd: Single shot multibox detector." European conference on computer vision. Springer, Cham, 2016.*  


### Semantic Segmentation Architectures

| model | input size | param memory | feature memory | flops |
|-------|------------|--------------|----------------|-------|
| pascal-fcn32s | 384 x 384 | 519 MB | 423 MB | 125 GFLOPS|
| pascal-fcn16s | 384 x 384 | 514 MB | 424 MB | 125 GFLOPS|
| pascal-fcn8s | 384 x 384 | 513 MB | 426 MB | 125 GFLOPS|

**References:**

* [pascal-fcn](http://www.cv-foundation.org/openaccess/content_cvpr_2015/html/Long_Fully_Convolutional_Networks_2015_CVPR_paper.html) - *Long, Jonathan, Evan Shelhamer, and Trevor Darrell. "Fully convolutional networks for semantic segmentation." Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition. 2015..*  

### Keypoint Detection Architectures

| model | input size | param memory | feature memory | flops |
|-------|------------|--------------|----------------|-------|
| multipose-mpi | 368 x 368 | 196 MB | 245 MB | 134 GFLOPS|
| multipose-coco | 368 x 368 | 200 MB | 246 MB | 136 GFLOPS|


**References:**

* [multipose](https://arxiv.org/abs/1611.08050) - *Cao, Zhe, et al. "Realtime multi-person 2d pose estimation using part affinity fields." arXiv preprint arXiv:1611.08050 (2016)..*  
 

### Notes and Assumptions  


The numbers for each architecture should be reasonably framework agnostic. It is assumed that all weights and activations are stored as floats (with 4 bytes per datum) and that all relus are performed in-place.  Fused multiply-adds are counted as single operations. 

The numbers should be considered to be rough approximations -  modern hardware makes it very difficult to accurately count operations (and even if you could, pipelining etc. means that it is not necessarily a good estimate of inference time).

The tool for computing the estimates is implemented as a module for the [autonn](https://github.com/vlfeat/autonn) wrapper of matconvnet and is included in this [repo](core/burden.m), so feel free to take a look for extra details.  Matconvnet versionf of all of the models can be downloaded from either [here](http://www.vlfeat.org/matconvnet/pretrained/) or [here](http://www.robots.ox.ac.uk/~albanie/models.html)

For further reading on the topic, the 2017 ICLR submission [An analysis of deep neural network models for practical applications](https://openreview.net/pdf?id=Bygq-H9eg) is interesting.  If you find any issues, or would like to add additional models, add an issue/PR.
