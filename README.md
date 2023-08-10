![image](https://github.com/adxcreative/RICE/assets/50560933/5bc9987e-d979-4a22-ad96-3a2e481db0cd)![image](https://github.com/adxcreative/RICE/assets/50560933/64a49a52-e0be-4fe6-9bd8-b99cb0c0a8b7)Livestreaming Product Recognition (LPR) is to recognize products a salesperson presents in a live commerce clip (or video) through content-based video-to-image retrieval.
A livestreaming consists of many clips introducing different products, and a shop with hundreds of images.
This task is to retrieve the ground-truth images from the shop (gallery) for each clip (query).

<p align="center">
  <img width="800" height="500" src="./_images/lpr4m_example.png">
</p>

LPR4M is a large-scale live commerce dataset, offering a significantly broader coverage of categories and diverse modalities such as video, image, and text. 

Key Features
- Large-Scale: LPR4M is the largest LPR dataset to date. It contains 4M exactly matched〈clip, image〉pairs of 4M live clips, and 332k shop images. Each image has 12 clips with different product variations, e.g., viewpoint, scale, and occlusion.
- Expressivity: LPR4M draws data pairs from 34 commonly used live commerce categories rather than relying solely on clothing data. Additionally, LPR4M offers auxiliary clip ASR text and image title.
- Diversity: LPR4M promotes clip diversity while preserving the real-world data distribution, with a focus on three components: product scale, visible duration, and the number of products in the clip.

<p align="center">
  <img width="650" height="150" src="./_images/statistics.png">
</p>

A <clip, image> pair is the basic unit of the trainging set. 
The full training set contains 4,013,617 clips and 332,438 images, which results in 4,013,617 pairs. Each image has 12 clips on average. We extract one frame every second for the training clips and obtain 473,402,226 frames. We created a url for each frame for easy download.



## Download 
To download the LPR4M data, please first download the 

### Download files
### Install ***img2dataset***
```bash
pip install img2dataset
```
***img2dataset*** can easily turn large sets of image urls to an image dataset. It can download, resize and package 100M urls in 20h on one machine. For example, [LAION-5B](https://laion.ai/blog/laion-5b/) contains 5B image/text pairs that can be downloaded by ***img2dataset*** in 7 days using 10 nodes. For better performance, it's highly recommended to set up a fast dns resolver, see [this section](https://github.com/rom1504/img2dataset#setting-up-a-high-performance-dns-resolver). You can refer
to [img2dataset](https://github.com/rom1504/img2dataset) for more details.


