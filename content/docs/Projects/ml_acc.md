---
title: "ML Accelerator"
---

# Machine Learning Accelerator

I worked on this as part of my senior design project. The goal was to create a hardware accelerator for an Object Tracking algorithm called [QDTrack](https://github.com/SysCV/qdtrack). I managed a group of about six people and we worked on this for about eight months.

**Tools Used:** Xilinx FPGAs, Vitis-HLS, Vivado, Python, C++

## Training

Our group had little experience working on large hardware projects or machine learning and especially not at the intersection of the two. Our advisor, Dr. Callie Hao, recommended we spend the first few months following her graduate level course on FPGA acceleration, [ECE 8893](https://sharclab.ece.gatech.edu/teaching/2023-spring-fpga/).

We didn't have much to work off of besides the publicly available slides and assignments, so I would often work ahead and work on the lectures and assignments, before helping everyone in my group with it.

## Implementation

Eventually, as we started to create the parallel system for QDTrack. We ran into a few problems: The FPGA was too small to fit the entire model. We had a bit of trouble trying to setup a multi-FPGA system and trying to pass data back and forth from a connected PC.

Eventually we only simulated certain portions of the algorithms and were able to demonstrate a significant speedup over the CPU implementation. Unfortunately we were not able to show an improvement over a GPU. We had simply run out of time by the end with the rest of our coursework. We needed to do more work in hardware design and experiment with different ways to pass in data to achieve greater speedup.

At the end, we had a poster presentation with QDTrack running so passerbys could see how the algorithm puts bounding boxes around them in real-time.
<!-- {{< embed-pdf url="/project_poster.pdf" hidePaginator="true" >}} -->

![ML Acc poster](/project_poster.jpg)


Many thanks to [Akshay Kamath](https://www.linkedin.com/in/akshaykamathk/) for his advice and mentorship in this project!