# Self Project


This is a base level demo into QGIS.

## What this demo contains

This project shows a few things - 

The base layer is the most simple, it provides a more colorful background at full extent, and as you zoom in, it fills in surrounding detail provided by Open Street Map. 

The countries layer is a vector layer that shows continents and countries around the globe.

Important locales is a short list of various places around the world that have a name for labels, what continent they are in.

Overlap will be explained below... 

## What this demo shows

This map shows a join of the important locations and the countries layer in the overlap layer (locales and countries have a continent column).

What this visually means is whatever continent the location is in is filled in with color at full extent, and the color will go away when zooming in at scale of 25,000,000. It is intended to draw the eye to the selected continents. And the labels for the locations will appear at 50,000,000.

## What is behind the scenes

What you cannot see, is the initial source of the important locales is a PostGIS database! As it is hosted on the original system and not on the internet, I supplied a CSV file with the same data to replicate the QGIS file if needed. Obviously the overlap shape file works independently. 

## What I have learned

PostGIS is a bit of a different database beast than I have used before. The geom column is VERY important in QGIS. From my testing, assigning points will not work without it. I had to call a friend of mine to tell me how to get it to work.

I originally wanted the overlap layer to be dynamic. So if I added a row with a new continent in the database, it would then be colored in on the map (Not the actual exported shape file). But I have not yet discovered a way to do that. 




