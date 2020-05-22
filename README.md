<p align="center"><font face="宋体" size=6> 2020MCM美赛数学建模-C题</font></p>

<p align="center"><font size=5><bold>Presented By R.G.</bold></font></p>

由于原本论文是用LaTeX编写并编译成pdf格式的，这里的README就只摘录一下摘要和目录部分了。详细论文思路相信阅读完summary应该大致也有了，目录主要展示一下论文的框架与布局。论文全文见仓库中的pdf文件，转载或引用望告知，谢谢！

## 摘要

<center> <bold>Summary</bold> </center>

To assist Sunshine Company in developing a scientific and reasonable online sales strategy, our team shall establish a SO-PMI based Review Quantization Model (RQ) and the Comprehensive Rating Model of Product Reputation (CRPR). Based on the data provided and the two models, we analyzed the influence of star rating, reviews and helpfulness rating on the sales of goods and the relationship among them.

After data processing (including index deletion, meaningless data elimination, etc.), we introduce an RQ model to quantify the text review. First, after text segmen- tation and elimination of stop words, we build a dictionary of positive and negative words as seed words. Then, we use the revised formula to calculate the SO- PMI value of each word in a review and obtain the quantified review.

To study the popularity of products, we introduce a CRPR model. First, we de- fine review values with the combination of quantified review and helpfulness ratings and define identity coefficient using vine and verified_purchase. Then, use the en- tropy weight method to determine the weight of the index, and obtain the reputation value after linear weighting. Taking the pacifier data as an example, and the weight are 0.49474 and 0.50526, respectively. Finally, the sensitivity analysis of the identity coefficient using hair_dryer data shows that both vine and verified_purchase have al- most the same impact on reputation. Moreover, our correlation analysis indicates that reviews are more important than star ratings.

To investigate the change of reputation with respect to time, we use the least square method and obtain the functional relationship of hair_dryer, microwave and pacifier. RMSE are 0.14, 0.16, and 0.09 for hair dryer, microwave, and pacifier, respec- tively.By analyzing the fitting curve, we conclude that the reputation of hair_dryer and microwave is stable in the later period, while pacifier fluctuates greatly.

To find potential successful products based on the functional relationship between product reputation and time, we establish an LDA(Latent Dirichlet Allocation) based product prediction model. First, we determine the reputation inflection points of 3 data set according to the fitting curves. Take hair_dryer as example, we obtain the cor- responding time period as: (2012.12-2013.1, 2015.3-4). Then, we use the LDA to extract keywords from the comment sets in these time periods and employ the PMI to cal- culate the semantic similarity between words, thereby predicting products success or failure by combining the semantic similarity and the sales volume. Taking hair_dryer set as an example, we find product_id =b003v264ww is a potential successful product.

Also, we conduct cross correlation analysis of star ratings and review values, which indicate that the rating will trigger more reviews. Based on the theme extraction and word frequency of each star levels review by LDA, we observe that some specific words in the comments will affect the star rating.

**Keywords:**  SO-PMI; LDA; Least Squares; Correlation analysis; Sales strategy

## 目录

**注：如果你的github无法看到图片的话，请参考我的这篇文章**

[解决Github无法显示图片以及README无法显示图片](https://blog.csdn.net/qq_41709370/article/details/106282229)

<img src="./contents.png" alt="contents" style="zoom:36%;" />



## 全文

全文见仓库的 [2020230.pdf](./2020230.pdf)

### 注：

今天发现github的README不能居中显示文字，经过一番尝试找到如下方法可以使得文字居中：

```html
<p align="center"><font face="宋体" size=6> 2020MCM美赛数学建模-C题</font></p>
```

之前一直用下面的语句居中，但是在github的README中无效：

```html
<center><font face="宋体" size=6> 2020MCM美赛数学建模-C题</font></center>
```

此外，README中按文件夹（仓库）路径添加图片不能显示图片：

```markdown
[imgname](./img_path.png)
```

查阅[资料](https://www.cnblogs.com/aretstchen/p/6550143.html)，发现github中README.md关联图片的图片地址是具有规范格式：

```html
https://github.com/用户名/repository仓库名/raw/分支名master/图片文件夹名称/***.png or***.jpg
```

但是依旧不能正常显示图片，然后我研究了一下，找到了解决方案并写了博客：

[解决Github无法显示图片以及README无法显示图片](https://blog.csdn.net/qq_41709370/article/details/106282229)

