---
title: "Terrain Traversability"
---

# Terrain Traversability Analysis with Image Dehazing

This was done as part of my CMU Deep Learning class.

We were interested in developing some sort of system that would allow autonomous vehicles to perform terrain traversability analysis in low-visibility conditions. Specifically, we were focused on taking images of hazy or blurry roads and trying to clear them up.

## Dataset creation
To create a machine learning model capable of dehazing an image, we first had to gather a dataset of normal and hazy images of off-road data. Unfortunately this was hard to come by. Not only are off-road pictures uninteresting, but blurry images of offroad pictures are even more boring. 

I worked on taking the RUGD dataset and programmatically generating a hazy input dataset from it. I did this through a combination of Gaussian Filters, color jitter, and a machine learning model that *created* haze.

While there have been previous works that have removed rain and noise from images, much of their dataset was manually created using photoshop significantly limiting their potential use, however we were able to produce around 7400 images without much trouble!

## Model Training
To tackle this problem, we tried three different approaches.
- Dark Channel Prior (existing open source)
- Generative Adversarial Network
- Convolutional Neural Network

Using mIOU as a metric, we showed that DCP performed the best, but took anywhere from 2-20 seconds per image. I worked on the GAN which was the fastest, but had the least mIOU. We were able to show that the CNN had the ideal balance between accuracy and speed, performing almost as well as DCP, but also taking under a second.

I based my GAN architecture on ID-CGAN, an existing work that worked to remove rain and mist from urban environments. I think given the lack of contrastive shapes in blurry offroad data (as compared to a city), it was harder for my GAN to perform nearly as well compared to ID-CGAN. I also think I made a subset of my data a bit too blurry. Maybe a better approach would have been to first train it on slightly blurry images, extend the network, and then fine-tune it on more blurry images. 

Certainly a more complex architecture could have been used since my GAN could process about 6 images in a second running an a CPU.

## Summary

I have attached the slides, final report paper, and presentation video.
For a quick summary, I would check out the slides. For an in-depth explanation, please refer to the video.

I got a serious cold when recording the video, so I sound pretty bad. :sweat_smile:


{{< hint warning >}}
I would have liked to add a bit more info about the project on this webpage, but I am a bit tired of the project so I will do it later.
{{< /hint >}}


<a href="/terrain_slides.pdf" target="_blank">Slides</a>  
<a href="/terrain_report.pdf" target="_blank">Paper</a>  

{{< youtube PUCT_D_scgg >}}
