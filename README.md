# image_dewarping_1

image dewarping

After reading the task and understanding the exact content, I first thought about preprocessing and
deep networks. I realized that I had a long way to go. Also, in this type of research and this issue,
we need a substantial data set, which unfortunately is not available. After various studies and
researches, I was only able to find a data set. I will give it to you. (Of course, this data is slightly
different from what is being asked and has more variety . We have several problems with this.
First, the background of the images we need to know precisely what kind of background we are
considering in these issues. Usually, the texts are written on a white paper and also the paper in a
preface. There is a simple colored background; of course, there are various modes. For example,
one-handed white backgrounds that make it difficult to distinguish between the sheet and the
ground or backgrounds with text themselves are among our most difficult tasks and concerns . 

Example:

[Interview Task Report-danial  farsi (1).pdf](https://github.com/danialfarsi/image_dewarping_1/files/7642912/Interview.Task.Report-danial.farsi.1.pdf)

In addition, other factors are also essential to us in this type of task in the real world. For example,
the shooting method, shooting angle, lighting are also essential and affect our diagnosis.


Using the research I did, much work was done in this regard, and usually, part of the problem
was solved, for example, in the article “Robust Document Image Dewarping Method Using
Text-Lines and Line Segments ” He had mentioned this well, but it was an innovative way to
present it, which was very efficient.
He did not give complete information about solving the problem due to the lack of open source.
After that, he reviewed other articles, and they could solve the issue to some extent. They did not
and did not make it available. I also needed a vital resource for deep learning. After these issues
and the task of reading zinc to image processing, we always know that to be able to solve a problem
at these levels using image processing is much more efficient and less costly than deep learning. I
had a problem. Our main parameter in these issues is the sheet of paper on which it is written. So
in the first step, we have to identify the paper. As I said, this is one of our biggest problems in
some environments. To do this, I first needed to blur the image to avoid additional parameters and
not have trouble recognizing the paper earlier. To do this, I used two filters, one Gaussian filter
and the other a custom filter that relatively images dulls.
At one point, I needed to separate the sheet from the environment to find the corners of the sheet.
After the binary algorithm, I used the pixels and quantized them. We create a situation where all
the pixels are just one of the two values, zero or one. In this case, we have made a good distinction,
and we were able to classify with image processing. We do all these steps in a way that we have
the image in gray. Now we need to have a contour. The most critical thing That exists for us is
paper. So the goal is to reach the paper contour. Using Open CV, we find an extensive and
functional contour and specify it as well. Our goal in finding the paper contour is actually to find
the corner.


[Interview Task Report-danial  farsi (1) (2).pdf](https://github.com/danialfarsi/image_dewarping_1/files/7642914/Interview.Task.Report-danial.farsi.1.2.pdf)


[Interview Task Report-danial  farsi (1) (1).pdf](https://github.com/danialfarsi/image_dewarping_1/files/7642917/Interview.Task.Report-danial.farsi.1.1.pdf)



Once we have formed the contour, we need to find its corners. We use the hemographic functions
and the current corners of the contour to find our final positions. Our primary concern is to identify
the contour corners because they may be part correctly. For example, it is not from the tab in the
image, and it is not easy to recognize it.

[Interview Task Report-danial  farsi (1) (3).pdf](https://github.com/danialfarsi/image_dewarping_1/files/7642921/Interview.Task.Report-danial.farsi.1.3.pdf)



As I have shown in the figure above with the red border, some corners are not recognizable. The
idea and the way of image processing solve this because we solve part of this issue with optical
transformations and filters, making this problem less. As you can see in the figure, our foreground
is not simple, and as you can see, the foreground also has text, but we have to process simple
images and filters. I was able to create a pleasing contour. We have a basic idea to transfer the
image using perspective matrices to find the corners. Now with the corners and matrices, we find
the destination points. We do this with findHomography and warpPerspective functions. After
these steps and transferring the image, now I will draw the image again and we have an image
according to our conditions.


[Interview Task Report-danial  farsi (1) (4).pdf](https://github.com/danialfarsi/image_dewarping_1/files/7642924/Interview.Task.Report-danial.farsi.1.4.pdf)



Conclusion

As we know, the most optimal way can always be the best way, so here we can use image
processing and clear several filters. To achieve our desired result. As you know, in this case, we
do not have deep learning with heavy processing, and we can reach our destination much more
optimally. Here I examined the paper framework to solve this task. However, if we know exactly
what kind of text is our text and what data it has, and as I said in what background are we better
able to manage this issue. The fastest and first way that came to my mind was this way because it
also needs to be processed. We did not have a burden, and we can do it quickly. The best way is
to customize my solution for extreme black and white environments. Backgrounds where the white
paper sheet is indistinguishable from the white background, my model and solution may Be
complex. I checked the model as much as I could and tested it for a background containing text,
which is specified in Google Columbine. Alternatively, at this point, he left the image to deep
processing. However, I have done all this process without using a deep network and only relying
on the principles of simple image processing, and it is convenient.
