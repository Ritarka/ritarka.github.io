---
title: Experience
weight: 4
draft: false
---

# Industry Experience

{{< hint info >}}
A lot of this is intentionally vague since I'd rather not post proprietary work publicly. If you'd like to know more about what I did, please reach out to me.
{{< /hint >}}

## Keysight
January 2024 - Present

I started working here shortly after graduating with my Bachelor's in December 2023. Here I am developing driver code for high-performance oscilloscopes. This involves navigating the register set for the chip, and writing C++ code to interface with the hardware. A lot of my work so far has involved revamping the codebase architecture, as well as developing algorithms to efficiently calibrate the hardware.

<p style="line-height: 10%;">
    <br>
    <hr style="border:1px solid gray">
</p>

## Cadence Design Systems
May 2023 - August 2023

Cadence is in the EDA (Electrical Design Automation) business - i.e. they make software that helps design hardware. I was working on [Helium](https://www.cadence.com/en_US/home/tools/system-design-and-verification/helium-virtual-and-hybrid-studio.html), a product to help design and debug hardware that is both in virtual and physical form.

I worked on a number of projects, including:
- Writing core C/C++ code for the simulator and developing custom utility functions and libraries
- Writing Java code to support saving state I/O for the simulator
- Migrating a test suite from a legacy system to a new one
- Developing a script that would automatically identify differences in simulation models and hardware designs

The hardest part was navigating the rather large codebase (~400 million lines of code) and understanding the interactions between the abstractions layers. I got to learn a lot about the design process, why certain architecture are helpful and others are not, and how to create tools or designs that are easy to use, debug, and synergize well with other tools.

<p style="line-height: 10%;">
    <br>
    <hr style="border:1px solid gray">
</p>

## Northrop Grumman
June 2022 - August 2022

This was my first internship in the summer of 2022. I mostly read schematics and wrote code to test the functionality of the hardware. I developed a testing framework to accurately identify precisely where the hardware failed, thereby decreasing debugging time from a matter of days to an hour.

I also wrote C++ networking code to interface a test unit with a larger system consisting of oscilloscopes, network analyzers, etc.

**Hardest Bug:** The test unit was booting up from two copies of the same OS and firmware. As such, any changes made to one copy would not be reflected in the other, causing a lot of confusion until the problem was found.

<p style="line-height: 10%;">
    <br>
    <hr style="border:1px solid gray">
</p>

# Research

## Model Selector
August 2023 - January 2024

This is work I did at the High Performance Architecture Lab for about a semester under Dr. Hyesoon Kim. I started working on a broken codebase during the summer of 2023 and slowly got it working. The goal was to develop a tool that would automatically select the best model for a given dataset.

Some of my earlier designs involved a lot of startup latency since the complex model was being trained on a large dataset. Instead I developed a tool that would predict the best model to use on a **per-image** basis, which ended up being a lot faster. This could not only be statically trained, but would could be easily parallelized and distributed across multiple GPUs.

Although the system architecture involved two stacked ML models, I ensured this configuration was successful, but making the selector model a very simple SVM. This was as complicated as it needed to be to create a good separation between the YOLO model classes. Here is an brief [report](/etri_report.pdf) of the work that I did.

<p style="line-height: 10%;">
    <br>
    <hr style="border:1px solid gray">
</p>

## Cask-HLS
August 2022 - May 2023

The goal with this research paper was to enable better debugging of Vitis-HLS. Vitis-HLS is a tool that takes C++ code and converts it into an RTL (Register Transfer Level) design - as such it is often used to develop complex hardware such as machine learning accelerator. This is a very complex compilation process and debugging it can be very difficult.

Since this is a proprietary tool, we were not able to use the source code, and accumulated information from the tool's output files as well as hidden intermediate files. This required a good bit of reverse engineering, but was ultimately quite rewarding. Here's the [paper](https://ieeexplore.ieee.org/abstract/document/10161946) we published.