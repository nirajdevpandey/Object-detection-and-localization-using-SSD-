# Single Shot MultiBox Detector implemented by Keras


## Introduction

SSD(Single Shot MultiBox Detector) is a state-of-art object detection algorithm, brought by Wei Liu and other wonderful guys, see [SSD: Single Shot MultiBox Detector @ arxiv](https://arxiv.org/abs/1512.02325), recommended to read for better understanding.

Also, SSD currently performs good at PASCAL VOC Challenge, see [http://host.robots.ox.ac.uk:8080/leaderboard/displaylb.php?challengeid=11&compid=3](http://host.robots.ox.ac.uk:8080/leaderboard/displaylb.php?challengeid=11&compid=3)

## References

My work is just playing with this fantastic algorithm, and see the detection result of my own. Many many thanks goes to the author of the SSD paper. 

## Guides

The code structures looks like below:

```
1. Aseets - Prior boxes  (prior_boxes_ssd300.pkl is the model pre-defined static prior boxes)
2. Data-set - VOC-2007
3. SSD Model - The training and the test scripts 

  - ssd_v2.py # main model architecture using Keras
	- ssd_layers.py # Normalize and PriorBox defenition
	- ssd_training.py # MultiboxLoss Definition
	- ssd_utils.py # Utilities including encode,decode,assign_boxes
  
4.  data-generator  # customrized generator, which return proper training data structure
				            # including image and assigned boxes(similar to input boxex)
  - get_data_from_XML.py # parse Annotations of PASCAL VOC, helper of generator
  
  ```

## Resources

dataset can be downloaded from [http://host.robots.ox.ac.uk/pascal/VOC/, use The VOC2007 Challenge in this example

Weights can be downloaded at [https://drive.google.com/file/d/0B5o_TPhUdyJWWEl5WG1lcUxCZzQ/view?usp=sharing](https://drive.google.com/file/d/0B5o_TPhUdyJWWEl5WG1lcUxCZzQ/view?usp=sharing)


## Hint

The folder called Data-set has just 5-10 samples of the VOC-2007. to train your own model please download the entire data set by clicking on the link above. Thanks 
