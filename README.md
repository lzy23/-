# 华为人口年龄预测
这题其实和易观那个性别年龄预测很像，chizhu大佬他们也开源了，github上可以搜到。我也借鉴了其中的一些，
构造了各种tfidf,比如activeapp对应uid，appcates对应uid，利用上那个大文件的话，还可以将duration或者times对应app构造矩阵进行tiidf，时间uid也可以构建矩阵。
降维的话我用了svd，我听群里大佬的也试了卡方，但是效果一般。。。我不知道我问题出在哪里。。。可能特征选的太少了？

上面这些应该大家都用了。。。我感觉我唯一可能与大家不一样的一部分就是对大文件的运用那里。
由于我的计算资源有限。。。40多万的app我要是one-hot或者构建矩阵训练，我根本做不到。
app的使用情况对于分辨一个人的年龄起着很大的作用，所以我就取了每个人使用时长前15名的app,构建了一幅‘图’，或者说类似于自然语言一样，就是15个词，
它每个词的词向量对应的就是这个app的特征，这就转化为一个类似于自然语言的处理方式了。然后，对应每个app每个人都有不同的使用时间，这就类似于权重一样，可以加进去
,然后进行学习训练。

最后我想说我这个分数不高才0.614，不过由于计算资源的原因，上面一些特征我建好了但是加不了。。。我觉得再加加特征可能能升？然后，我这个只是
提供一个另外的想法，没有打乱大家想法的意思。。。而且毕竟分数不高，希望大家有判别的看待，因为不一定会有效果。最后，如果你觉得有用，给个star吧！谢谢！
上面这些文件，就是这部分的，另外的我没上传，有需要的我再上传。


还有，如果有大佬发现我代码哪里有问题或者我的方法有什么可以改进的地方可以和我说一下，谢谢！！
