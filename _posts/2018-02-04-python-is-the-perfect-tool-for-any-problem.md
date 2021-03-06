---
published: true
title: "Python Is The Perfect Tool For Any Problem"
date: 2018-02-04
categories:
  - python
  - programming
---

![](https://miro.medium.com/max/2000/0*UiI1SaCbMvovF2wh.?q=20)

## Reflecting on my first Python program

Reflection is always a helpful (and sometimes entertaining ) exercise. For nostalgia’s sake — if one can be nostalgic for something 2 years old— I wanted to share my first Python program. I initially picked up Python as an aerospace engineering student to avoid spreadsheets and little did I know how good a decision this would turn out to be.

My Python education began with the book [_Automate the Boring Stuff with Python_](https://automatetheboringstuff.com/?)by Al Sweigart, an excellent application-based book with simple programs to do useful tasks. When I learn a new topic, I look for any chances to use it and I needed a problem to solve in Python. Fortunately, I found one in the form of a $200 textbook required for a class. My personal limit for textbooks is about $20 (_Automate the Boring Stuff_ is free online) and I refused to even rent this book. Desperate to get the book before the first assignment, I saw it was available for a free one-week trial through Amazon with a new account. I got the book for one week and was able to do the first assignment. While I could have kept creating new accounts one week at a time, I needed a better solution. Enter Python and my first programming application.


<!--more-->

One of many useful libraries in _Automate the Boring Stuff_ is [pyautogui](https://pyautogui.readthedocs.io/en/latest/?) which allows you to control the keyboard and mouse through Python. They say when you have a hammer, every problem looks like a nail, and that was definitely the case here. Python and pyautogui would allow me to press the arrow keys and take screenshots, and I put the two together to come up with a solution to the book issue. I wrote my first program to automatically turn through every page in the book and take a screenshot. The end program was only 10 lines long yet I was nearly as proud of it as anything I had done in aerospace engineering! Following is the program in its entirety:

```

import pyautogui
import time

# Sleep for 5 seconds to allow me to open book
time.sleep(5)

# Range can be changed depending on the number of pages
for i in range(1000):

# Turn page
 pyautogui.keyDown('right')
 pyautogui.keyUp('right')

# Take and save a screenshot
 pyautogui.screenshot('images/page_%d.pdf' % i)
 time.sleep(0.05)

```

Running the program is pretty simple (I encourage anyone to try). I saved the script as book_screenshot.py, then pulled up a command prompt in the same folder and typed:

```

python book_screenshot.py

```

Then I would have 5 seconds to flip to the book and put it into fullscreen. The program would do the rest, flipping through every page and taking a screenshot that was saved as a pdf. I could then join all the pdfs together into one file, and have a (questionably legal) copy of the book! Granted, this was a pretty awful copy because it could not be searched, but I made any excuse possible to use my “book”.

![](https://miro.medium.com/max/2000/1*kxxaqXCHYHJbuURp6clKtA.gif?q=20)
*I could watch this for hours*

This example demonstrates two key points that have stuck with me as I continue my data science education:

1.  The [best way to learn a new skill is to find a problem you need to solve](/how-to-master-new-skills-656d42d0e09c?)!
2.  You don’t need to fully master a skill before it is useful.

With just a few lines of code and a free online book, I wrote a program that I actually put to use. Learning the basics can be tedious, and my first attempts to learn Python failed within a few hours as I got stuck with ideas like data structures and loops. Changing tactics, I started to develop solutions to real problems and ended up learning the fundamentals along the way. There is so much to master in programming and data science, but you don’t need to learn everything at once. Pick a problem you need to solve and get started!

Since then, I have made a few [more sophisticated programs](/stock-analysis-in-python-a0054e2c1a4c?), but I still remember this first script with fondness!

Share your first program! I welcome discussion, feedback, and constructive criticism. I can be reached on Twitter @koehrsen_will.
