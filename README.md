---
noteId: "a687cde02a2111ef892a5f797d1617e6"
tags: []
---

本文是对VAIC_23_24软件详细的解说，以帮助参加过VEX竞赛，对Brian编程有过经验又不熟悉AI原理和技术的读者，能较快掌握以VAIC_23_24软件为例的AI原理，理解VAIC-AI的基础知识和基本思路，以适应今后VEX AI竞赛。

VEX已经成为世界最著名的从VAX竞赛之一，将会在保持其竞赛的基本规则、比赛场地、机器人设计和搭建、传感器系列等传统的基础上，增加AI技术的应用。

可以预见AI技术将成为今后VEX竞赛的核心，因此，掌握必要的AI将是今后参加VEX竞赛的必备技能。

为循序渐进，本文分为三部分：

第一部分 “何为VAIC.ipynb” 是对VAIC_23_24软件运行的硬件环境介绍。

第二部分 “VAIC软件介绍.ipynb” 是对VAIC_23_24软件组成和涉及的AI概念的说明。

第三部分 “VAIC程序详解.ipynb” 是对 VAIC_23_24软件的运行方法的详细介绍，假设读者有过Brian C++的编程经历，讨论重点是python的Jetson AI及与AI有关的Brian C++程序功能，不涉及原Brian C++的编程内容。

由于在讲解中大量引用了程序段(python,C++)(Visual Studio Code)，以ipynb(Jupyter Notebook)文件格式写成。

使用ipynb格式可以清楚分辨程序段落(code)和解释段落，使用VSCode可以方便在各个文件中查找函数调用关系。

需要注意的是，在VSCode里阅读本文时不要执行code cell，因为作为编辑器VSCode的环境与VAIC代码的执行环境不同，即使是在Jetson的Ubuntu或Brian的Vexcode Pro V5环境里，进行讲述的代码段并非全部代码，并且未按程序执行的顺序选择。

This article provides a detailed explanation of the VAIC_23_24 software. It is intended to help readers who have participated in VEX competitions and have experience with VEX coding but are not familiar with AI principles and technologies. The goal is to enable these readers to quickly grasp the AI principles exemplified by the VAIC_23_24 software, understand the fundamental knowledge and basic ideas of VAIC-AI, and prepare for future VEX AI competitions.

VEX has become one of the world's most renowned competitions, and it will continue to maintain its basic rules, competition venues, robot design and construction, and sensor series while incorporating AI technology applications.

It is foreseeable that AI technology will become the core of future VEX competitions, making it an essential skill for participants. To ensure a gradual learning process, this guide is divided into three parts:

1.The first part “what is VAIC.ipynb” introduces the hardware environment for running VAIC_23_24 software.

2.The second part “Introduction to VAIC Software” explains the components of VAIC_23_24 software and the AI concepts involved.

3.The third section, "Detailed Explanation of VAIC Program.ipynb," provides a comprehensive introduction to the operation methods of the VAIC_23_24 software. It assumes that the reader has experience with Brian C++ programming. The discussion focuses on Jetson AI in Python and the AI-related functionalities of Brian C++ programs, without covering the original Brian C++ programming content.

Since the explanation heavily references code snippets (in Python and C++) and uses the ipynb (Jupyter Notebook) file format, it is important to distinguish between code sections and explanatory sections clearly. Using VSCode makes it easy to search for function call relationships within various files.

Please note that when reading this document in VSCode, do not execute the code cells, as the VSCode environment differs from the VAIC execution environment. Even in Jetson's Ubuntu or Brian's Vexcode Pro V5 environment, the described code snippets are not the entire code and are not selected in the order of program execution.