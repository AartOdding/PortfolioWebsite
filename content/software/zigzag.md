---
draft: false
title: ZigZag
date: 2019-08-14T15:19:55.316Z
featured: false
---
![ZigZag](img/zigzag-capture.png "The ZigZag user interface.")

ZigZag is a node based programming language that you can use to create interactive graphics in an intuitive and fun way. You create a network of "operators", that perform different steps on the data flowing through them. Each frame all the operators in the network are executed once, which results in a smooth video as output. Because the rendering happens in realtime on the graphics card, interactivity can be added easily by coupling parameters of the network to external signals such as audio levels or sensor data.

ZigZag is designed with customizability and user extensibility in mind. You can create your own operators, data types, and views in C++, and use them from within ZigZag. This allows you to both be very productive, by working in a high level of abstraction, and gives you full customizability where you need by creating new operators and data types in the C++ API.

Source code can be found at: <https://github.com/AartOdding/ZigZag>