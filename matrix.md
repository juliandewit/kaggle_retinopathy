# Diabetic retinopathy - Manual screening vs algorithms
Last few months I've been participating in the [Kaggle Diabetic Retinopathy challenge](https://www.kaggle.com/c/diabetic-retinopathy-detection). For a quick introduction see [Wikipedia](https://en.wikipedia.org/wiki/Diabetic_retinopathy).
We had to find an algorithm to grade the level of the disease given the images of the eyes of diabetic patients.


<!--
First of all this was a GREAT competition that was helping to come up with a solution that might improve the quality of life for millions of people. For a quick introduction see [Wikipedia](https://en.wikipedia.org/wiki/Diabetic_retinopathy). -->

<!--At the time of writing the team of [me](https://www.kaggle.com/juliandewit) and [Daniel Hammack](https://www.kaggle.com/dhammack) are doing quite well.
The question that keeps coming back to me was how practical an algorithm would be for retinal screening. 
-->

As the competition progressed I became more and more convinced that automatic screening would really be very helpful. The scoring system is [quadratic weighted kappa](https://en.wikipedia.org/wiki/Cohen%27s_kappa) What is interesting to note a few teams scored 85 or higher. According to the literature about Kappa, 85 means that our algorithm is VERY good. [look here](http://virtualhost.cs.columbia.edu/~julia/courses/CS6998/Interrater_agreement.Kappa_statistic.pdf) [and here](https://www.medcalc.org/manual/kappa.php).

Now we come at the main issue. The algorithms had to match the labels provided by doctors.. However.. Doctors make mistakes.. and it turned out that sometimes the algorithm gets "downscored" while actually doing the right predictions.

That's why I dicided to put the [confusion matrix](https://en.wikipedia.org/wiki/Confusion_matrix) online.
The idea would be to allow people to comment on the predictions made by the algorihtm and the labels given by the docters. All in all we might get a better feel about the practical use of automatic screening. Perhaps github is not ideal for this. if you got a better platform.. Please feel free to fork it an make a better experience !


*Rows : Labels given by doctors*<br>
*Columns : Predicted labels by algorithm*<br>

|   |Pred 0|Pred 1|Pred 2|Pred 3|Pred 4|
|:-------|:----:|:----:|:----:|:----:|:----:|
|Doctor 0|[24502](https://github.com/juliandewit/kaggle_retinopathy/blob/master/lists/00/list.md)|[1116](https://github.com/juliandewit/kaggle_retinopathy/blob/master/lists/01/list.md)|[186](https://github.com/juliandewit/kaggle_retinopathy/blob/master/lists/02/list.md)|[5](https://github.com/juliandewit/kaggle_retinopathy/blob/master/lists/03/list.md)|[1](https://github.com/juliandewit/kaggle_retinopathy/blob/master/lists/04/list.md)|
|Doctor 1|[1175](https://github.com/juliandewit/kaggle_retinopathy/blob/master/lists/10/list.md)|[829](https://github.com/juliandewit/kaggle_retinopathy/blob/master/lists/11/list.md)|[437](https://github.com/juliandewit/kaggle_retinopathy/blob/master/lists/12/list.md)|[2](https://github.com/juliandewit/kaggle_retinopathy/blob/master/lists/13/list.md)|[0](https://github.com/juliandewit/kaggle_retinopathy/blob/master/lists/14/list.md)|
|Doctor 2|[490](https://github.com/juliandewit/kaggle_retinopathy/blob/master/lists/20/list.md)|[791](https://github.com/juliandewit/kaggle_retinopathy/blob/master/lists/21/list.md)|[3212](https://github.com/juliandewit/kaggle_retinopathy/blob/master/lists/22/list.md)|[771](https://github.com/juliandewit/kaggle_retinopathy/blob/master/lists/23/list.md)|[28](https://github.com/juliandewit/kaggle_retinopathy/blob/master/lists/24/list.md)|
|Doctor 3|[8](https://github.com/juliandewit/kaggle_retinopathy/blob/master/lists/30/list.md)|[18](https://github.com/juliandewit/kaggle_retinopathy/blob/master/lists/31/list.md)|[140](https://github.com/juliandewit/kaggle_retinopathy/blob/master/lists/32/list.md)|[565](https://github.com/juliandewit/kaggle_retinopathy/blob/master/lists/33/list.md)|[142](https://github.com/juliandewit/kaggle_retinopathy/blob/master/lists/34/list.md)|
|Doctor 4|[3](https://github.com/juliandewit/kaggle_retinopathy/blob/master/lists/40/list.md)|[3](https://github.com/juliandewit/kaggle_retinopathy/blob/master/lists/41/list.md)|[50](https://github.com/juliandewit/kaggle_retinopathy/blob/master/lists/42/list.md)|[146](https://github.com/juliandewit/kaggle_retinopathy/blob/master/lists/43/list.md)|[506](https://github.com/juliandewit/kaggle_retinopathy/blob/master/lists/44/list.md)|

Perhaps the biggest problem is where the doctor scores a 2 and the computer a 0.
This is problably due to the fact that one small symptom might at once make it a level 2.
Examples are [big bleedings] (https://www.google.nl/search?q=hemorrhages&espv=2&biw=1920&bih=1055&source=lnms&tbm=isch&sa=X&ved=0CAYQ_AUoAWoVChMImp_m27L7xgIVBpQsCh28NgzO#tbm=isch&q=hemorhages+retinopathy) and [Cotton wool spots](https://www.google.nl/search?q=hemorrhages&espv=2&biw=1920&bih=1055&source=lnms&tbm=isch&sa=X&ved=0CAYQ_AUoAWoVChMImp_m27L7xgIVBpQsCh28NgzO#tbm=isch&q=cotton+wool+spots+)

###Some examples that I encountered. There are many more of them!.
- [Image quality](https://github.com/juliandewit/kaggle_retinopathy/blob/master/quality.png)
- [Cotton wool spots that are actually artefacts]( https://github.com/juliandewit/kaggle_retinopathy/blob/master/lists/20/10/10501_right.md)
- [Another](https://github.com/juliandewit/kaggle_retinopathy/blob/master/lists/20/10/10616_left.md)
- [Bleedings that are actually artefacts](https://github.com/juliandewit/kaggle_retinopathy/blob/master/lists/20/10/10671_right.md)
- [Eyes that cleary suffer from someting else if its not DR](https://github.com/juliandewit/kaggle_retinopathy/blob/master/lists/03/list.md)










