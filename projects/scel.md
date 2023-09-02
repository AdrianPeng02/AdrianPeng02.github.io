---
layout: project
type: project
image: img/scel-images/scel_logo.png
title: "Smart Campus Energy Lab (Firmware Team)"
date: 2023
published: true
labels:
  - C
  - C++
  - SQL
  - Python
  - Databases
  - Pipelining
summary: "Vertically Integrated Project that develops the firmware being used by the weatherboxes created by the SCEL lab"
---
<div class="text-center p-4">
<img width="350px" src="../img/scel-images/scel_logo.png" class="img-thumbnail" >
</div>


The Smart Campus Energy Lab (SCEL) is a Vertically Integrated Project (VIP) here at UH Manoa. Currently, SCEL's main goal is to develop weatherboxes which are pieces of hardware composed of various sensors enclosed in weatherproof casings. These weatherboxes collect meteorologial data like solar radiance, temperature, humidity, and etc. This meteorological data is then used to train a machine learning model to forecast weather patterns with the purpose of optimizing ideal locations for photovoltaic panel placement throughout campus. Using this technology, UH Manoa can take steps towards being 100% sustainable. In a bigger picture, the entire state of Hawaii has the goal of being 100% renewable by the year 2045 and this technology can be used to maximize our renewable energy efficiency in terms of cost. 

As I was in the Firmware team, our job is to maintain the current weatherbox code, develop new features that can improve the quality of life of the system behind the scenes, and assist the hardware teams with any issues they may have. In the 2023 Spring semester, my team worked on developing a data pipeline. This pipeline essentially automates the process of structuring the software in new hardware models as they will all follow the same unified schema. This will allow for easier data management and manipulation in the databases as all weatherbox versions will have the same formatting. To develop this feature, we used mostly SQL, Python, and the command line along with C and C++ to work on Arduino code.
