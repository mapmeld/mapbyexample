OpenStreetMap has an XML API which is worth looking at, but for most queries,
there’s a hidden shortcut called the Overpass API.

The first thing to understand about OpenStreetMap data is that every part of the
map is stored as nodes, ways, and relations.

* A node is a latitude and longitude coordinate. You can add tags to tell more information
  about that place, like amenity = school, name = Nottingham West. OpenStreetMap is flexible in
  what tags it accepts, but you want to follow others' conventions to make sure others see
  and understand your data.

* A way is a list of nodes, forming a line. Polygons on OpenStreetMap are a way which
  begins and ends with the same node. If you are mapping a school, you could draw the outline of
  the school building, end at the same point where you started, and tag the final shape amenity=school
  and building=yes. There is an area=yes tag to specify a filled-in polygon, but usually OpenStreetMap
  uses context clues like building=yes or natural=lake to decide to fill in the shape.

* A relation is any group of nodes, ways, and other relations. Large shapes including interstates,
  coastlines, national borders, transit routes, and multi-building campuses would be listed as several
  nodes and ways, with a single relation object to unite them. Relations are highly important
  but generally less common and less easy to make from scratch.
