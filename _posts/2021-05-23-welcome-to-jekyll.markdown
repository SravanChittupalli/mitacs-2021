---
layout: post
title:  "Week 1"
date:   2021-05-23 19:37:20 +0530
categories: jekyll update
---

## 24-05-2021

Had a short meet with the professor. We discussed about the project in detail. I was then given 3 videos and the task is to segregate ripe, unripe strawberries and flowers and also find the level of ripeness(unripe, partially ripe, almost ripe, fully ripe) of the strawberries. Before starting with the task I had to research a bit and submit my plan of action. I will start coding from tomorrow.

## 25-05-2021

Started coding!  
Explored different color spaces. HSV was the best. Tuned color ranges for segmentation. As HSV doesnot take into consideration the structural composition of the class, there are a lot of misclassifications. Also, lighting condition affect this algorithm a lot. Got 82% accuracy for flower detection and ~52% accuracy for ripe strawberry detection. So, now as the baseline accuracy is set I can move on to the second method.  

## 26-05-2021

Most of my day went into setting up Darknet and then annotating 86 images. Plan is to train a model partially and then getting predictions and using them to create a new dataset. 

Trained YOLO tiny to check if YOLO is good at classifying flowers, ripe, unripe strawberries. Well, it was working extremely well. 

## 27-05-2021

Tested the trained YOLO tiny weights on different videos. The results were good. 

Made a script to get predictions and these predictions were stored in such a way that the data generated can be used to create a bigger dataset and then trained the model again with bigger and better data for better accuracy. Astonishingly after 6000 epochs the loss of both the models was approximately the same.

<!-- {% highlight ruby %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}

Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/ -->
