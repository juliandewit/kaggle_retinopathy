# Diabetic retinopathy - Manual screening vs algorithms
Last few months I've been participating in the [Kaggle Diabetic Retinopathy challenge](https://www.kaggle.com/c/diabetic-retinopathy-detection).

First of all this was a GREAT competition that was helping to come up with a solution that might improve the quality of life for millions of people. For a quick introduction see [Wikipedia](https://en.wikipedia.org/wiki/Diabetic_retinopathy).

We had to find an algorithm to grade the level of the disease given the images of the eyes of diabetic patients.
At the time of writing the team of [me](https://www.kaggle.com/juliandewit) and [Daniel Hammack](https://www.kaggle.com/dhammack) are doing quite well.

The question that keeps coming back to me was how practical an algorithm would be for retinal screening. As the competition progressed I became more and more convinced that automatic screening would really be very helpful. The scoring system is [quadratic weighted kappa](https://en.wikipedia.org/wiki/Cohen%27s_kappa) but if your not a math-head forget that. What is interesting to note is that there are a number of teams at score 85 or higher. Wich is considered VERY good in the literature.
[look here](http://virtualhost.cs.columbia.edu/~julia/courses/CS6998/Interrater_agreement.Kappa_statistic.pdf) [and here](https://www.medcalc.org/manual/kappa.php).







