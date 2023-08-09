<p align="center">
  <img width="800" height="500" src="./_images/lpr4m_example.png">
</p>

LPR4M is a large-scale live commerce dataset, offering a significantly broader coverage of categories and diverse modalities such as video, image, and text. 

Key Features
- Large-Scale: LPR4M is the largest LPR dataset to date. It contains 4M exactly matched 〈clip, image〉 pairs of 4M live clips, and 332k shop images. Each image has 14.5 clips with different product variations, e.g., viewpoint, scale, and occlusion.
- Expressivity: LPR4M draws data pairs from 34 commonly used live commerce categories rather than relying solely on clothing data. Additionally, LPR4M offers auxiliary clip ASR text and image title.
- Diversity: LPR4M promotes clip diversity while preserving the real-world data distribution, with a focus on three components: product scale, visible duration, and the number of products in the clip.

![statistic](/_images/statistic.png "xxx")

## Download dataset
### Download files
### Install ***img2dataset***
```bash
pip install img2dataset
```
***img2dataset*** can easily turn large sets of image urls to an image dataset. It can download, resize and package 100M urls in 20h on one machine. For example, [LAION-5B](https://laion.ai/blog/laion-5b/) contains 5B image/text pairs that can be downloaded by ***img2dataset*** in 7 days using 10 nodes. For better performance, it's highly recommended to set up a fast dns resolver, see [this section](https://github.com/rom1504/img2dataset#setting-up-a-high-performance-dns-resolver). You can refer
to [img2dataset](https://github.com/rom1504/img2dataset) for more details.


