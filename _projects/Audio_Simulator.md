---
layout: page
title: Audio Simulator With Java
description: A Java based audio simulator. Featuring a pathing algorithm combined with attenuation to generate realistic audio.
img: assets/img/AudioPathing.jpg
importance: 3
category: Fun
tags: Java Audio Algorithms
github: https://github.com/NonIntelligent/Audio-in-Java
---

## The project

My very first programming project. I chose Java as my first programming language as I quickly understood the concept of  OOP (Object-Oriented-Programming).

The project is an audio simulator that can play any .WAV files. It simulates attenuation and direction based on obstacles and distance. You can create walls and audio sources in real-time as well as allowing the map to be cleared without re-running the programme.

I took inspiration for this project based on how sound propagation was handled in the game Rainbow Six Siege. I found a deep-dive [article](https://www.gamedeveloper.com/design/game-design-deep-dive-dynamic-audio-in-destructible-levels-in-i-rainbow-six-siege-i-) talking about dynamic audio in a destructible environment and its implementation in the game.

## Implementation

Java has a wide variety of inbuilt functionality compared to other languages such as display rendering, network IO and most importantly audio rendering. I didn’t know about any libraries, so I stuck with Java’s implementation and read the [programmer’s guide](https://docs.oracle.com/javase/7/docs/technotes/guides/sound/programmer_guide/contents.html) to learn how to use it.

Using the guide, I implemented support for .WAV file reading and playback as a stream or clip. The former reads data from the file into a buffer before to play back in chunks. While the latter loads the entire file into main memory for complete playback control including seeking and with low latency. However, this is only appropriate for seconds worth of audio due to the high data size.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/AudioPathing.jpg" title="Audio Traversal" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

After some research on sound propagation and pathing, I decided to implement the A Star algorithm due to the importance of speed/latency. The algorithm is shown above with a path drawn from the audio source (black) to the player (blue). The green nodes have been considered by algorithm when finding the shortest path, with the yellow nodes being chosen to build a path from.

I’ve also added an obstacle which will reduce the distance the audio can travel if the path has to cross over it to reach the player. Which is why you see the path bending around the corners of each wall (the optimal position for the nodes).

## Challenges

I was learning on the go, whilst developing this project. I spent a lot of time reading documentation about creating windows, rendering textures, basic collision etc.

Implementing the A Star algorithm was challenging because I had to write the algorithm based on my theory knowledge. I also had to account for concurrent array accesses due a separate feature I implemented.

## For the future

By putting my knowledge into practise, I’ve learnt a lot about the Java language and development in general. I could already feel the effects of disorganised code and the complexity of adding new features within this project.

Now, with more years of programming experience with different languages and patterns, I can refactor this project to be more robust and flexible. I could also redesign this project with different libraries or frameworks.
