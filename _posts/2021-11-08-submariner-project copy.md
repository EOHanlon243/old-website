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
<!-- ## Project Intialisation

As the final project of my first year of University, I was chosen to be part of Team Submariner. This team was hand selected to produce a project for an external client. The client being The Royal Navy.

The project in question was a virtual reality (VR) submarine simulation, where two people took roles on a submarine. It was required to create two separate roles for the game. Firstly, the Planesman, who operates the bow or stern diving planes of a submarine. The second being a Periscope Operator who operates a periscope to observe surrounds and provides information about their location. They would work together with the objective of identifying a target vessel (marked with a red flag).

The goal of the project was to increase engagement of people attending recruitment events, in hopes of getting more people to sign up for the navy. Due to this, the simulation it would have to be small in terms of playtime and scale. Therefore, the playtime would range between 90 – 120 seconds, allowing more people to play it throughout the event. Additionally, as this was a simulation, it was expected to look and act as realistically as possible whilst having VR functionality.

Due to the nature of this project and our client, an NDA was needed to be signed before the Navy could supply use with information of the project. This also include assets and other useful resources and documentation. The limitations of COVID-19 also prevented us from observing a submarine in person, instead we would receive a 3D scan as reference.

Unfortunately, as Christmas was very close, it would have to wait at least five weeks before the NDA could be processed, and the resources could be sent over. Due to the lack of information from the navy and lack of leadership from our leader at the time, we had no clear starting point for the project.

Since the beginning of the project, I felt uneasy as not only did I not feel like I deserved to work on this project, having much less experience with general game development than everyone else, but also the fact that the Royal Navy was our client. These worries, alongside the lack of management from our leader led me to not participate within the project for the first month or so.

During this time, a game jam for creating the first prototype of the simulation was planned out. As I saw this as a proper start to the project, I was prepared to join them in efforts to make a start on the project, however, due to personal reasons, I was unable to attend. The game jam led to a working prototype with some basic game features working.

As many of the gameplay tasks were being covered by some of the other teammates, my first task within the project was to create and implement some undersea terrain, along with a few islands that would be used as the world for our game. With a little guidance from my team, I began to look into software that I can use to create / generate terrain.

## Terragen 4 - 

The world that I needed to create has provide a sense of realism. Because of this, using in-built Unity tools will not be sufficient enough, especially with no experience using them. As such, we thought the best course of action would be to use other software to manage world generation. After searching for software options, we first attempted to use *Terragen 4*.

*Terragen 4* is a very reputable software made for creating environmental scenes and renders for films, games, and virtual reality. As it has been used previously within games and virtual reality, it seemed like an ideal software for world generation.

<div class="columns">
  <div class= "column is-half" align = "center"> 
    <figure>
      <img src="/assets/images/submariner/terragen-test-landscape.png" alt="Terragen Test Landscape" class="has-ratio">
      <figcaption align = "center"><i>Terragen Landscape Testing </i></figcaption>
    </figure>
  </div>
  <div class= "column is-half" align = "center">
    <figure>
      <img src="/assets/images/submariner/terragen-test-ocean.png" alt="Terragen Ocean Testing" class="has-ratio">
      <figcaption align = "center"><i>Terragen Ocean Testing</i></figcaption>
    </figure>
  </div>
</div>

At first, the software seemed very beneficial for us to use; it has a high reputation, having been used in a variety of games and other media. If utilised correctly, it will surely lead to great results. Due to how powerful *Terragen* is, learning how to utilise the software proved to be a challenge. Normally I would considerer learning the program , however as it was a client project, we couldn’t afford the time to do so.

Unfortunately, the biggest draw back was the limited amount of export options available. This became an issue due to our method of generating a landscape required maps. These maps would be applied to a terrain object, creating a landscape. In previous versions, they allowed for exporting maps, which was no longer the case. If exportation was not a problem, this software would be ideal for our project. Thus, this led into further search for map generation software.


## L3DT -
*L3DT* is a Windows application for generating terrain maps and textures. It's intended to help game developers and digital artists create high-quality 3D worlds. *L3DT* offered similar features as *Terragen 4* but in a more simplistic fashion. 

It was easy to create convincing looking terrain with features such as a sea depth or terrain type. Then, adjusting these values on how the world is generating. The main reason for using *L3DT* was the option for map exporting for our terrain landscape.

After finding suitable software for our project, I began to construct the landscape. At first, I did not put much consideration into what I was creating. Rather, my main goal was to understand how the software worked and what features are usable. That way, I can make the most convincing landscape possible. There were different settings to tinker with that allow for simple landscape generation.

<div class="columns">
  <div class= "column" align = "center"> 
    <figure>
      <img src="/assets/images/submariner/heightfield-size.png" alt="Heightfield Size" class="has-ratio">
      <figcaption align = "center"><i>Heightfield Size</i> </figcaption>
    </figure>
  </div>
  <div class= "column" align = "center">
    <figure>
      <img src="/assets/images/submariner/design-map-parameters.png" alt="Design Map Parameters" class="has-ratio">
      <figcaption align = "center"><i>Design Map Parameters</i></figcaption>
    </figure>
  </div>
</div>

The heightfield size allowed for changing the size and resolution of the maps. Measured in meters, scaling the size of the map to best fit an ocean environment. The correct resolution was critical to getting high-definition textures. Likewise, details on the map can be more precise. Furthermore, Design map parameters determined how many features of the world would be generated and to what scale. Determining a good balance between these features was key to creating the landscape. 

Over the time using the software, I found that editing the landscape wasn’t as in-depth as I hoped. What's gained with simplifying the process, it lost in its lack of post-generation editing. Besides this, the outcome you receive is not as realistic as hoped. Generation led to abnormal-looking islands and unusable underwater sections. Yet, in the end, *L3DT* proved to be the only viable option at the time.

After studying the basics of *L3DT*, it was time to install a trial landscape into Unity. When exporting files into Unity, *L3DT* allows downloading of specific terrain maps. Specifically, the height, normal and texture maps. Then, I applied the maps to the terrain object, creating a new landscape within Unity. 

## Crosshair Creation -

As a side task, I was also talked about designing and implementing crosshairs to our game. These will display where the player is aiming at the screen. With my designs, they had to not obstruct the view of in-game objects or UI elements. My starting point was to look for inspiration for designs from similar games.

One of those games was Wolfpack, an in-depth simulation of a submarine taking place during World War 2. Due to how similar the game was to our project, it was a great source of inspiration for our game. This game utilised two crosshairs, such as a regular crosshair and a dot design. Both designs are used in differing scenarios.

<div class="columns">
  <div class= "column" align = "center"> 
    <figure>
      <img src="/assets/images/submariner/crosshair-cross.png" alt="Cross Crosshair" class="has-ratio">
      <figcaption align = "center"><i>Cross Crosshair</i> </figcaption>
    </figure>
  </div>
  <div class= "column" align = "center">
    <figure>
      <img src="/assets/images/submariner/crosshair-dot.png" alt="Dot Crosshair" class="has-ratio">
      <figcaption align = "center"><i>Dot Crosshair</i></figcaption>
    </figure>
  </div>
</div>

Both crosshairs can work well due to the first-person perspective of our game. Both provide are great for guiding the player to where they are looking at.

Crosshairs have great association with the first person shooter (FPS) genre of games. As such, my research went towards looking at crosshair design from that genre. Two FPS games I used as reference and inspiration from were Counter Strike: Global Offensive (CS: GO) and Tom Clancy’s Rainbow Six Siege (R6S). 

<figure>
  <img src="/assets/images/submariner/crosshair-tshape.png" alt="T-Shaped Crosshair" class="has-ratio">
  <figcaption align = "center"><i>T-Shaped Crosshair</i></figcaption>
</figure>

First, I started with looking into CS:GO.  Due to the games heavy themes of combat and use of weaponry, crosshairs are essential. The game offers a variety of crosshair designs, which are customisable for accessibility. Out of the available designs, the main one that piqued my interest was the t-shaped crosshair. It provides a bold design whilst providing a bit more clarity that the normal crosshair.

<figure>
  <img src="/assets/images/submariner/crosshair-triangle.png" alt="Triangle Crosshair" class="has-ratio">
  <figcaption align = "center"><i>Triangle Crosshair</i></figcaption>
</figure>

Secondly, I looked into R6S which shares a few similarities with CSGO with its theming. The ACOG scope’s triangular styled crosshair provides a point to direct the player to the centre of the screen. But, the bottom line would be very distracting and unnecessary, causing confusion and reducing clarity.

<figure>
  <img src="/assets/images/submariner/crosshair-gungeon.png" alt="Enter The Gungeon Crosshairs" class="has-ratio">
  <figcaption align = "center"><i>Enter The Gungeon Crosshair</i></figcaption>
</figure>

Finally, another game that inspired me was 'Enter the Dungeon'. To fit the games theme of 'guns', they stylised cursors to emulate traditional crosshairs. From the styles, the main ones that stuck out were the square and circle cursor with the centre dot. These different styles provided boldness that may help new players. 

--- 

### Feedback -

To ensure that our progress with up to expectations, we scheduled a meeting with our lecturer, Ted. Within this meeting, we wanted to go over completed tasks, ways to improve and approaches for future tasks. We created a Powerpoint that showcases our progress and achieved milestones. Each page represented a person and the progress they contributed to the project.

During the meeting, we presented the presentation, where it was meet the good response. Yet, to meet the standard of the Royal Navy,  many elements had improvements to make. In the work I created, there were areas in my research and prototyping where I neglected. 

For world generation, Ted suggested to research into Bathymetry, the study of sea depth. He linked me to online resources to assist me, such as a bathymetry map of the world. This will help me further understand sea depth and archipelago landscape formation.

For my crosshairs, he advised me to observe how the crosshairs would work with colour blindness. Especially, light colour primaries such as red and green. This will help understand how the colour choice would affect the user experience. Checking these types of concerns will help to increase the accessibility of our game and game development later on.
 
With our feedback obtained, my next goal was to re-create the landscape. Using bathymetry to create acceptable criteria to assess landscape generation.

--- 

## Bathymetry - 

Bathymetry is the study of shapes and the depth of water within oceans, rivers and other large bodies of water. Similar to topography maps, they are mapped out to represent three dimensional features of water bodies by providing lines / colours that differentiate between layers of depth. This also serves as a foundation for other sciences such as hydrography ,which measures the physical features of water.

In addition to this, it has assisted me with my understanding of terms and other vocabulary commonly used within the topic. For example, depth and altitude have separate definitions and are both measured differently. Depth being the deepness of a waterbody from the water surface; altitude being the deepness in regard to the platforms ‘system reference point. The terminology learnt helped me to have a better understanding on bathymetry maps.

There are many interactive bathymetry maps online, made by well-established organisations and some government websites that provided bathymetry data from all over the world. They even provide survey track lines, showing the distance and location the survey took place, when the survey was completed and even maximum and minimum depths of the area surveyed. Looking at the data, in regard to their date and relevance, it allowed me to understand bathymetry of different terrains around the world.

Through this research, I had decided that a small coastal archipelago would be the best type of terrain to go, as doing so will allow for dynamic placement of other vessels. This placement will urge the player to explore around the zone in search for the targeted vessel. In addition to this, it will provide an interesting view for the periscope player to look at, encouraging more engagement with the game. Finally, it will also provide a challenge when navigating the area, encouraging teamwork between the periscope and planesman players.

## World Generation Testing -

In my efforts to create an immersive and effective world for our periscope user to view, a plan was created to ensure essential criteria was met during its development.

The plan consisted of me using the generation features provided within L3DT to create multiple worlds to find the most optimal setting to create the final world. These criteria were taking my bathymetry research into mind. The criteria created are as followed:

1.	Majority of the terrain must be sea level whilst allowing the formation of an archipelago to exist.
2.	Islands created must have a notable nature element (which is only apparent upon generation of the texture layer).
3.	Water depth must be deep enough for the submarine to manoeuvre without trouble. (Max Depth: 1200m)
4.	Must provide a little navigation challenge in terms of manoeuvrability throughout the water.

Using the world generation settings and parameters, I generated three different prototype worlds that followed, with each iteration having slight differences in their attributes, narrowing down towards the most optimal generation settings. Here are each of the prototypes and the settings they used:

#### Attempt 1:

<figure>
  <img src="/assets/images/submariner/landscape-generation-1.png" alt="Landscape Generation 1"  style="height:350px">
  <figcaption align = "center"><i>Landscape Generation 1</i></figcaption>
</figure>

| Benefits:                                  | Drawbacks:          | Improvements:                  |
|--------------------------------------------|---------------------|--------------------------------|
| Good land to sea ration.                   | Not enough islands. | Add more islands to generation |
| Islands are well established.              | Sea is too deep.    | Reduce depth of map.           |
| Considerable nature elements.              |                     |                                |
| Sea depth viable for submarine movability. |                     |                                |

During this attempt, the design map scale was too low, which produced bland and quite unnatural looking islands which did not fit within my criteria. So, for the later attempts, the design map scale was increased, allowing for more interesting islands and potentially archipelagos to be generated.

#### Attempt 2:

<figure>
  <img src="/assets/images/submariner/landscape-generation-2.png" alt="Landscape Generation 2" style="height:350px">
  <figcaption align = "center"><i>Landscape Generation 2</i></figcaption>
</figure>

| **Benefits:**                  | **Drawbacks:**                                 | **Improvements:**                                            |
|--------------------------------|------------------------------------------------|--------------------------------------------------------------|
| Good land to sea ration.       | Sea exceeding depth limit in parts.            | Sea near islands needs to be deeper.                         |
| Islands are well established.  | Sea depth not viable for submarine movability. | Change undersea land so it doesn’t hinder submarine movement |
| Considerable nature elements.  | Sea is mostly shallow.                         |                                                              |
|                                |                                                |                                                              |

For this attempt, although the islands were more interesting and provided a nice variance in shape and size, they were spaced out too far. That prevented us from implementing certain requirements in the way we wanted them to, such as ships hiding behind the islands.

#### Attempt 3:

<figure>
  <img src="/assets/images/submariner/landscape-generation-3.png" alt="Landscape Generation 3" style="height:350px">
  <figcaption align = "center"><i>Landscape Generation 3</i></figcaption>
</figure>

| **Benefits:**                               | **Drawbacks:**                      | **Improvements:**  |
|---------------------------------------------|-------------------------------------|--------------------|
| Good land to sea ratio.                     | Sea exceeding depth limit in parts. | Change sea depth.  |
| Islands are well established.               | Too many islands.                   |                    |
| Considerable nature elements.               | Part of the sea is shallow.         |                    |
| Sea depth viable for submarine movability.  |                                     |                    |
| Sea only exceeding the depth limit.         |                                     |                    |
|                                             |                                     |                    |

When generating this attempt, it provided quite an interesting formation of islands that were spaced well enough to achieve my criteria and to allow for interesting gameplay mechanics to be fully utilised. However, the large islands did concern me at first, so I implemented a terrain object within a separate unity project to see how much it would affect the submarine’s manoeuvrability and the periscope visibility. It did constrict the submarine’s movement a little bit, it still provided what we needed for the project.

## Crosshair Prototyping -

During the development phase, different designs of crosshairs were created, developing the ideas and inspirations noted in the research section. There were a few criteria created to ensure that they meet the standard for the project.

The criteria are as followed:

1.	Must fit within a 16 x 16-pixel canvas.
2.	Must be bold enough to get players attention.
3. 	Must provide good clarity (65% clear space).

Five designs were created in order to test a wide range of different styles and sizes in order to see which fits best. Here are each of the designs created:

#### Circular:

<figure>
  <img src="/assets/images/submariner/circular-crosshairs.png" alt="Circular Crosshairs">
  <figcaption align = "center"><i>Circular Crosshairs </i></figcaption>
</figure>

Inspired by the circular crosshair found in ‘Enter the Gungeon’.  The circle was enlarged to fill available space, providing clarity within the circle.
Centre dot provides the player with the central point of the screen.

| Benefits:                               | Drawbacks:                         |
|-----------------------------------------|------------------------------------|
| Bold, easy to spot.                     | Quite large                        |
| Easy to see what you are hovering over. | Has potential to distract players. |

#### Minimal:

<figure>
  <img src="/assets/images/submariner/minimal-crosshairs.png" alt="Minimal Crosshairs">
  <figcaption align = "center"><i>Minimal Crosshairs </i></figcaption>
</figure>

Based on the small dot crosshair found in ‘Wolfpack’.
Small to provide less distraction to players. Helps players immerse themselves in the game better.
Mainly be used in the planesman room to interact with UI elements.

| Benefits:                               | Drawbacks:                         |
|-----------------------------------------|------------------------------------|
| Simple, easy to understand.             | Harder to see                      |
| Small, little to no distractions.       |                                    |
| More precise for inputs.                |                                    |  


#### Square:

<figure>
  <img src= "/assets/images/submariner/square-crosshairs.png" alt="Square Crosshairs">
  <figcaption align = "center"><i>Square Crosshairs </i></figcaption>
</figure>

Based on the square crosshair found in ‘Enter the Gungeon’.
Similar to circular design in terms of benefits/drawbacks. Square enlarged to fill available space. Removed two corners to not make the design overwhelming whilst improving clarity.
Would ideally be used in a planesman room, perhaps in periscope view as well.

| Benefits:                               | Drawbacks:                         |
|-----------------------------------------|------------------------------------|
| Bold, easy to spot.                     | Quite large                        |
| Easy to see what you are hovering over. | Has potential to distract players. |

#### Triangular:

<figure>
  <img src= "/assets/images/submariner/triangular-crosshairs.png" alt="Triangular Crosshairs">
  <figcaption align = "center"><i> Triangular Crosshairs </i></figcaption>
</figure>

Based on the ACOG scope found in ‘Tom Clancy’s Rainbow Six Siege’.
Doesn’t take up a lot of available space. Easy to see where pointing to. Triangle hollow for clarity of UI elements behind it.#

| Benefits:                               | Drawbacks:                         |
|-----------------------------------------|------------------------------------|
| Small and simple.                       | Unorthodox, hard to understand.    |
| Bold, provides a lot of visual clarity. |                                    |

#### T-Shaped:

<figure>
  <img src= "/assets/images/submariner/t-shaped-crosshairs.png" alt="T-Shaped Crosshairs">
  <figcaption align = "center"><i> T-Shaped Crosshairs </i></figcaption>
</figure>

Based on the t-shaped crosshair found in ‘Counter Strike: Global Offensive’.
Went for t-shape rather than the normal crosshair for clarity, whilst still being bold.

| Benefits:                                    | Drawbacks:                                        |
|----------------------------------------------|---------------------------------------------------|
| Very common, easy to recognise / understand. | Doesn’t fit as well for the theme of the game.    |

### Colour Accessibility:
As for the colours of the crosshairs, it was originally tasked that I produce white or black crosshairs to be used in game. However, due to lighting in the planesman room, it could blend in / not contrast enough to the environment created. To counteract the problem, I created 10 different colour variants (including the black and white shades before) in order to see which ones would work best. Using Ted’s advice, the colour variants were tested using a colour-blind simulator. Here are the results (testing circular crosshair)

| Deutan:                       |                                                                                           |
|-------------------------------|-------------------------------------------------------------------------------------------|
| Green-Weak / Deuteranomaly    | ![Deuteranomaly](/assets/images/submariner/deuteranomaly.png)                             |
| Green-Blind / Deuteranopia    | ![Deuteranopia](/assets/images/submariner/deuteranopia.png)                               |
|                               |                                                                                           |
| **Protan:**                   |                                                                                           |
| Red-Weak / Protanomaly Weak   | ![Protanomaly](/assets/images/submariner/protanomaly.png)                                 |
| Red-Blind / Protanopia Blind  | ![Protanopia](/assets/images/submariner/protanopia.png)                                   |
|                               |                                                                                           |
| **Tritan:**                   |                                                                                           |
| Blue-Weak / Tritanomaly Weak  | ![Tritanomaly](/assets/images/submariner/tritanomaly.png)                                 |
| Blue-Blind / Tritanopia Blind | ![Tritanopia](/assets/images/submariner/tritanopia.png)                                   |
|                               |                                                                                           |
| **Monochromatic:**            |                                                                                           |
| Monochromacy                  | ![Monochromacy](/assets/images/submariner/monochromacy.png)                               |
| Blue Cone Monochromacy        | ![Blue Cone Monochromacy](/assets/images/submariner/blue-cone-monochromacy.png)           |

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Game Jam:

Before we started the game jam, each of us were assigned different tasks that we would work throughout the game tasks. My main tasks were to create world borders just in case the player goes too far away from the mission area. In addition, I would have to create a fog system that would cover the sea to reduce visibility of the water edge and provide and interesting view for the periscope view.
At this point in the project, we focused on making a single player experience with no VR as every opportunity for this idea to be implemented was not taken. Our new main goal is to have a finished project by the end of the week, ready to deliver for to our client.
Unfortunately, at the beginning of the game jam, we had a major setback. The repository we were going to use for source control was not ready in time, even though we were told it would be easy and completed a few days prior to this. Whilst waiting for the repository to be up, I took the initiative and researched into my tasks.

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## World Border Fog Research

I made the decision to research fog and borders under the same task as my main idea was that I used the fog alongside the border to make the border look more evident.
For the fog, I was recommended a YouTube video that explain a way to use Unity particle system, alongside a smoke sprite sheet to produce convincing look, volumetric fog (Mirza, 2016). My next step was to look for a royalty free smoke sprite set to implement.

As for researching the borders, there were two approaches that could have been chosen. Either the player would remain in a spherical collider and would be out of bounds when they left it or, have box colliders on the outskirts of the world that the submarine will have to enter to be considered out of bounds. Since the spherical border may cause collision issues with the submarine, I decided to go with the box collider idea.

When the repository was up and working, I began work on implementing this border within the game. This was as simple as creating box colliders on the outside of the world and created a basic script to detect the submarine once it passed through.

Following that, I tried implementing the fog system using the video found on YouTube. This involved me creating a material out of the sprite sheet to use in the particle system. Once it was implemented, it was time to change the opacity of the particles to make it more translucent. 

Unfortunately, these changes were hard to see as the smoke sprite sheets was too dark for any noticeable colour changes to be made. My solution to this was to edit the sprite sheet in photoshop, changing it into a white smoke instead. This allowed me to both make a noticeable change in its transparency whilst also allow a tinge to be applied, better suiting different weathers and skyboxes.

Due to this new discovery, my teammate gave me the idea to create separate fog templates based on different skyboxes we had available to use. I decided to base each skybox based on the time of day it would occur. For each imaged I changed the colour of the fog within the scene, how the fog would spawn, and the sky box we used:

| **Morning Sky:**                                               | **Midday Sky:**                                                |
|:--------------------------------------------------------------:|:--------------------------------------------------------------:|
| ![Morning Sky](/assets/images/submariner/morning-sky.png)      | ![Midday Sky](/assets/images/submariner/midday-sky.png)        |
|:--------------------------------------------------------------:|:--------------------------------------------------------------:|
| **Afternoon Sky:**                                             | **Evening Sky:**                                               |
| ![Afternoon Sky](/assets/images/submariner/afternoon-sky.png)  | ![Evening Sky](/assets/images/submariner/evening-sky.png)      |

Using these images, a google form was made, allowing our teammates to vote on which skybox / fog combination would work best for our simulation. Unfortunately, not everyone voted on this form, however the feedback received was useful none the less.

<figure>
  <img src= "/assets/images/submariner/skybox-fog-survey.png" alt="Skybox Fog Survey">
  <figcaption align = "center"><i>Skybox Fog Survey</i></figcaption>
</figure>

Since it was a split between the morning and afternoon sky, I decided to chose the morning sky as it had more clarity than the afternoon sky.  In addition to having the fog on the borders, I made the decision to have a small amount of fog within the play area to better suit the environment and make the fog on the borders more reasonable.

## Ship Movement / Prefab Editing

Just like the fog, I was recommended a video series on how to create a nav mesh and how to use nav agents to navigate the mesh (Brackeys, 2018). However, a few of the details within this video were out of date for the version of Unity we were using. Instead, I looked into another YouTube video, that gave me a great overview on how to create a nav mesh (Table Flip Games, 2019).
My start to creating the nav mesh began with using a plane object to bake my nav mesh onto. This plane would be a little smaller than the playable to ensure no ships went out of bounds. At the beginning, I had the height map placed on the water surface. However, there were issues with how the ships would spawn, with many of them floating above the water. This was more of an issue that with how nav agents worked with nav meshes.
As creating a nav mesh is a major part of the game and its environment, it was crucial that all of the prefabs were all up to date. As such, I saw it as my responsibility to make sure all of the prefabs would function properly on the nav mesh.
The first change made was the models we were using. We were using models created by another team who attempted this project the year prior. Although one of the models we used was well developed and was perfect for our project, the others were not up to par with it. We came to the decision that these models would have to be replaced in order to maintain the quality and the realistic aspect of the game aesthetics. Since we did not have the time to make models from scratch, we had to implement some royalty free models online.  There were many models to test from, but I narrowed it down to three models that had both royalty free license and were somewhat easy to implement into unity.

<figure>
  <img src= "/assets/images/submariner/sailboat-model.png" alt="Sailboat Model">
  <figcaption align = "center"><i> Sailboat Model</i></figcaption>
</figure>

Implementing these models into Unity, at first, seemed really easy. Unfortunately, due to the way they were created and exported, there were many problems with the model. For starters, all the ships had an issue with there rotation, meaning that if the movement script were applied, the ship would either move sideways or backwards. Additionally, the sailboat model axis was wrong. This issue is how Unity and 3DSMax names the axes differently. When it comes to implementing these models to Unity, the models would be on there side rather than upright. These issues could not be solved within Unity, rather requiring me to use 3DSMax to edit each model individually.

<figure>
  <img src= "/assets/images/submariner/yacht-model.png" alt="Yacht Model">
  <figcaption align = "center"><i> Yacht Model</i></figcaption>
</figure>

The rotation problem was quite easy to fix, all that was required was to rotate it and set its new default orientation. As for the axis problem, it required me to change the pivot of the object. The main issue with doing this is that any textures / materials already applied to it, will not work correctly. Thankfully, one of my teammates, who had more knowledge and experience with working with 3D models, was willing to reapply the materials within another software so the axis changes work properly.

<figure>
  <img src= "/assets/images/submariner/dinghy-model.png" alt="Dinghy Model">
  <figcaption align = "center"><i> Dinghy Model</i></figcaption>
</figure>

Once this was completed, the next change was to make sure the ships stay above the water. With the current way the spawn script work, they were all hard coded to spawn with a certain y axis value, to ensure they were above water. As each model had its own properties to keep in mind, hard coding a singular value for this was not ideal.
A solution that me and another teammate came up with was to make the model a child of an empty game object that would be on the sea floor whilst changing the height of the model to look as though it is in the sea. The empty object was then applied the movement script and a nav mesh agent (to control aspects of its movement and allows for interactions with the nav mesh).
As the nav agent was now a component onto the empty game object, of which all of them shared, it was more logical to apply the nav mesh to the bottom of the sea, allowing all the ships to keep the assigned height.
 -->