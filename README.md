# Commuters-Navigation_GIS_Project

## Overview
Maps have become an integral part of our daily lives, and people rely on them for a wide range of purposes. Whether it's finding directions, discovering new places, or planning a trip, maps are essential tools. The ability to customize and personalize maps to fit individual needs has become an essential part of our lives, helping us make informed decisions and navigate the world around us.

As a result, we are designing a GIS system that could help people to navigate through the street

## Table of Contents
- What is this GIS?
- How it looks?
- Why it's efficient?

## What is this GIS?
This GIS visualizes integrated geographic information from multiple public APIs(Such as OSM API). It is equipped with a visually appealing user interface using GTK+ tools to display street maps, public transportation, and natural geographic features of major cities such as Beijing, Toronto, and Tokyo. Users can find their route by entering the start and destination point information, and the program will calculate the optimal route using Dijkstra and A* algorithm. This GIS has also left public interfaces for online real-time information such as live traffic and weather

<img width="1000" alt="Picture of Beijing" src="https://user-images.githubusercontent.com/105031962/228465134-08c8f6b4-e035-46dd-b5b4-78de284c8cf2.png">

## How it looks?
As discussed, this GIS relies on two sources: the pre-loaded APIs, such as OpenStreetMap API; the other way is to use libcurl to fetch additional information online. This means that our GIS could display any information in the public API.

For example, let's take a tour of the Harry Potter world:

<img width="1080" alt="Kings Cross" src="https://user-images.githubusercontent.com/105031962/228466020-7f0fd31f-83d2-4d29-963d-869d08a51d08.png">

This image is the Kings Cross Station. As you can see, our GIS displays the subway stations, subway lines, and traffic signals for demonstration. 

Other than that, as you might have noticed, the map also load natural features from the APIs and visualize them on the screen! How about taking a tour of the forbidden city?

<img width="1086" alt="Picture Of Forbidden City" src="https://user-images.githubusercontent.com/105031962/228466848-0e2356e7-0505-49e9-8f34-c1184897a1cb.png">

## Why it's efficient?
Improving the performance of the map is always a critical task. The team made it possible by pre-loading the map before visualization. Although this may cause a few seconds delay before using, it will do the work after way easier!

The team loaded the characteristic info from APIs into the classes and structs in C++. Then store the classes into suitable data structures like unordered maps and priority queues to ensure faster access.

On the other hand, the algorithm of the GIS is also mighty. The teams started with BFS, then improved to Dijkstra, then added an offset to make it into the A* method when finding the road. Various algorithms implemented by the GIS also made a huge difference.



