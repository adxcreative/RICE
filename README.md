___Livestreaming Product Recognition (LPR)___ is to recognize products a salesperson presents in a live commerce clip (or video) through content-based video-to-image retrieval.
A livestreaming consists of many clips introducing different products, and a shop with hundreds of images.
This task is to retrieve the ground-truth images from the shop (gallery) for each clip (query).

<p align="center">
  <img width="800" height="500" src="./_images/lpr4m_example.png">
</p>

LPR4M is a large-scale live commerce dataset, offering a significantly broader coverage of categories and diverse modalities such as video, image, and text. 

__Key Features__
- Large-Scale: LPR4M is the largest LPR dataset to date. It contains 4M exactly matched〈clip, image〉pairs of 4M live clips, and 332k shop images. Each image has 12 clips with different product variations, e.g., viewpoint, scale, and occlusion.
- Expressivity: LPR4M draws data pairs from 34 commonly used live commerce categories rather than relying solely on clothing data. Additionally, LPR4M offers auxiliary clip ASR text and image title.
- Diversity: LPR4M promotes clip diversity while preserving the real-world data distribution, with a focus on three components: product scale, visible duration, and the number of products in the clip.

__Statistics__

<p align="center">
  <img width="740" height="150" src="./_images/statistics.png">
</p>

- Full training set: A <clip, image> pair is the basic unit of the trainging set. 
The full training set contains 4,013,617 clips and 332,438 images, which results in 4,013,617 pairs. Each image has 12 clips on average. We extract one frame every second for the training clips and obtain 473,402,226 frames.
- Detection training set: The product detection in the clip can promote the LPR accuracy. Thus, we sampled a subset from the full training set as the training set for the product detector. We extract 10 frames at even intervals for each clip and obtain 1,120,410 frames with 1,115,629 annotated product boxes.
- Test set: The query set contains 20,079 clips, the gallery set contains 66,358 shop images. We adopt rank-k accuracy as the retrieval performance metrics. In order to evaluation of the performances of product detector, we extract one frame every 3 seconds for each query clip and obtain 501,656 frames with 669,374 annotated product boxes.

We created a url for each clip frame and shop image for easy download.


## Download 
We organize the url data of the dataset into four *txt* files. One url one row.
- training_frame_url_full_473402226.txt: the 473,402,226 frame urls of the full training clips.
- training_image_url_full_332438.txt: the 332,438 shop image urls of the training set.
- test_frame_url_501656.txt: the 501,656 frame urls of the test clips.
- test_image_url_66358.txt: the 66,358 shop image urls of the test set.

#### Frame url example
```bash
https://js-ad.a.yximgs.com/bs2/ad-material-video/7b601b02-2c63-11ee-bb6d-b8cef60c2fd0-1667916122888-1667916252390-0081.jpg
```
An example of frame url, where *https://js-ad.a.yximgs.com/bs2/ad-material-video/* is the prefix, 

*7b601b02-2c63-11ee-bb6d-b8cef60c2fd0* is the livestreaming id (live_id), 

*1667916122888-1667916252390* indicates the start and end timestamp of the livestreaming. 

Thus, *live_id-start_timestamp-end_timestamp* represents a unique clip_id, which means that the clip is cropped from live_id, and the cropping starts from *start_timestamp* and ends at *end_timestamp*.

*0081* is the frame index in current clip_id, and *live_id-start_timestamp-end_timestamp-frame_index* represents a unique frame_id.

#### Shop image url example
```bash
https://js-ad.a.yximgs.com/bs2/ad-material-video/fff8b484-2eeb-11ee-b7bb-77cb20e634dc.jpg
```
An example of shop image url, where *fff8b484-2eeb-11ee-b7bb-77cb20e634dc* is the image id.

### Download the url files
To download the LPR4M data, please first xxx.
We will email you the download link of the four url files.

### Install *img2dataset*
```bash
pip install img2dataset
```
***img2dataset*** can easily turn large sets of image urls to an image dataset. :fire:It can download, resize and package 100M urls in 20h on one machine. :fire:For example, [LAION-5B](https://laion.ai/blog/laion-5b/) contains 5B image/text pairs that can be downloaded by ***img2dataset*** in 7 days using 10 nodes. For better performance, it's highly recommended to set up a fast dns resolver, see [this section](https://github.com/rom1504/img2dataset#setting-up-a-high-performance-dns-resolver). You can refer
to [img2dataset](https://github.com/rom1504/img2dataset) for more details.

### Download the full dataset

## Citation

```bibtex
@article{yang2023crossview,
  title={Cross-view Semantic Alignment for Livestreaming Product Recognition},
  author={Wenjie Yang and Yiyi Chen and Yan Li and Yanhua Cheng and Xudong Liu and Quan Chen and Han Li},
  journal={arXiv preprint arXiv:2308.04912},
  year={2023}
}
```
