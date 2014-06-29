## What is vector data?
Anything drawn on the map using a list of coordinates (including points, lines, and shapes) is vector data. If you’re thinking about clickable photo markers, changing borders, or routing buses, you’re probably thinking in vector data.

## Should I use vector data all of the time?
Vector data will be the main component for many projects. Anytime you have interactive data drawn on top of a map background, the easiest solution will be vector data.

When your data is the map background, or when you have a lot of data, then you have to consider multiple options. Listing all of the coordinates for vector data can become too large to share with users in a vector way. Roads are lines made out of multiple points, so they are all vectors. But when you zoom out to see an entire city, downloading every point on every road is going to take a long time, and showing all of those points will crash the web browser. The same issues come up for datasets with thousands of addresses or detailed national borders.

## How do you know when to use vector data or some other kind of data?
In general, a good thought process is to consider how engaged your user is with the data.

If the roads are just a simplified background with no user interaction, there’s no reason for the user to download them as vector data.

For the next level of interaction, consider the thousands of ATMs in New York City. A user is only going to need information on a few that they click. It makes sense to use a service like Google Fusion Tables, CartoDB, or your own server to display all of the points together in a set of images. When you click on those images or do a search, there will be a small delay while the browser talks to the server, but this small delay is much more convenient than downloading unnecessary data.

For highly interactive pages such as an election map, accurate borders could be a lot of data to download, but attentive users are likely to browse around and make comparisons. They want to see a highlighted border around a state while they are viewing its data. When new election results come in, they might want a state to change color without reloading the page. To draw these maps, you are going to need vector data. TopoJSON’s command line tools can shrink the source data’s file size and simplify the borders.

Then will be some cases where the user is engaged with the data, but the full dataset is impossible to download. If you were comparing data on every block of a large city, that has to be handled by a server. Google Fusion Tables and CartoDB are worth considering again. Another technique (covered in the section on rasters) is to use TileMill to create a UTFGrid layers, and use MapBox.js to display data on each block.

## Is it possible for only one part of the map to be vector data?

A good example of a mix of vector and raster-represented data is getting directions. In most maps, streets are rendered as images, but you need the full vector dataset to calculate directions. The map sends the directions request to a server, the server finds a route, and the browser gets your directions returned as vector data. This makes it possible for you to interact with the streets and intersections in your route.

You could use the same technique in your own map to return search results and display nearby items to a user without sharing the full dataset.
