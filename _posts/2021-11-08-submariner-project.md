---
title: Submariner Project
layout: post
post-image: /assets/images/submariner/2021-submariner-title.png
description: The submariner project is a navy submarine simulation created as a client-based project for The Royal Navy.
tags:
- university
- client-based
- simulation
published: true
---

# What is the Submariner Project?

> The Submariner Project was a joint collaboration project between the University of Portsmouth and the Royal Navy. The project involved creating an accurate Navy Submarine simulator that would later be used in Navy recruitment events. The goal of the simulation is to traverse the sea in the submarine and spot a target vessle (indicated by a red flag).

--- 

### Terragen 4 - 

The world that I needed to create has provide a sense of realism. Because of this, using in-built Unity tools will not be sufficient enough, especially with no experience using them. As such, we thought the best course of action would be to use other software to manage world generation. After searching for software options, we first attempted to use *Terragen 4*.

*Terragen 4* is a very reputable software made for creating environmental scenes and renders for films, games, and virtual reality. As it has been used previously within games and virtual reality, it seemed like an ideal software for world generation.

<figure>
  <img src="/assets/images/submariner/terragen-test-landscape.png" alt="Terragen Test Landscape">
  <figcaption align = "center"><i><b>Figure 1 </b> - Terragen Landscape Testing </i></figcaption>
</figure>

At first, the software seemed very beneficial for us to use; it has a high reputation, having been used in a variety of games and other media. If utilised correctly, it will surely lead to great results.

<figure>
  <img src="/assets/images/submariner/terragen-test-ocean.png" alt="Terragen Ocean Testing">
  <figcaption align = "center"><i><b>Figure 2 </b> - Terragen Ocean Testing</i></figcaption>
</figure>

Due to how powerful *Terragen* is, learning how to utilise the software proved to be a challenge. Normally I would considerer learning the program , however as it was a client project, we couldn’t afford the time to do so.

Unfortunately, the biggest draw back was the limited amount of export options available. This became an issue due to our method of generating a landscape required maps. These maps would be applied to a terrain object, creating a landscape. In previous versions, they allowed for exporting maps, which was no longer the case.

If exportation was not a problem, this software would be ideal for our project. Thus, this led into further search for map generation software.


### L3DT -
*L3DT* is a Windows application for generating terrain maps and textures. It's intended to help game developers and digital artists create high-quality 3D worlds. *L3DT* offered similar features as *Terragen 4* but in a more simplistic fashion. 

It was easy to create convincing looking terrain with features such as a sea depth or terrain type. Then, adjusting these values on how the world is generating. The main reason for using *L3DT* was the option for map exporting for our terrain landscape.

After finding suitable software for our project, I began to construct the landscape. At first, I did not put much consideration into what I was creating. Rather, my main goal was to understand how the software worked and what features are usable. That way, I can make the most convincing landscape possible. There were different settings to tinker with that allow for simple landscape generation.

<figure>
  <img src="/assets/images/submariner/heightfield-size.png" alt="Heightfield Size ">
  <figcaption align = "center"><i><b>Figure 3 </b> - Heightfield Size</i> </figcaption>
</figure>

The heightfield size allowed for changing the size and resolution of the maps. Measured in meters, scaling the size of the map to best fit an ocean environment. The correct resolution was critical to getting high-definition textures. Likewise, details on the map can be more precise.

<figure>
  <img src="/assets/images/submariner/design-map-parameters.png" alt="Heightfield Size Settings">
  <figcaption align = "center"><i><b>Figure 4 </b> - Design Map Parameters</i></figcaption>
</figure>

Furthermore, Design map parameters determined how many features of the world would be generated and to what scale. Determining a good balance between these features was key to creating the landscape. 

Over the time using the software, I found that editing the landscape wasn’t as in-depth as I hoped. What's gained with simplifying the process, it lost in its lack of post-generation editing. Besides this, the outcome you receive is not as realistic as hoped. Generation led to abnormal-looking islands and unusable underwater sections. Yet, in the end, *L3DT* proved to be the only viable option at the time.

After studying the basics of *L3DT*, it was time to install a trial landscape into Unity. When exporting files into Unity, *L3DT* allows downloading of specific terrain maps. Specifically, the height, normal and texture maps. Then, I applied the maps to the terrain object, creating a new landscape within Unity. 