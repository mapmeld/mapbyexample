# Leaflet and Friends

The good news when I first started on this project was that Derek had already
created a basic map powered by Leaflet.js.

Over the past several years, several different libraries have been created to
display interactive maps on the web. Google Maps and its API took an early lead.
OpenLayers was created as an open source alternative, but without non-Google maps
to show in its frame, there wasn't a lot going for it. OpenLayers responded by
growing and growing its library to support many different map sources and formats,
including some older GIS servers. But this just made the library seemed big and
tailored toward GIS experts, not the web developers.

In early 2011 I ran a class on P2PU about how to use OpenLayers.

At the time, Google was making moves toward charging for their mapping API.
OpenStreetMap was improving in data coverage and quality. And a few companies
started producing their own alternatives to OpenLayers. It was the perfect
environment for the Leaflet.js library. Its initial selling points were that it
was small, open source, and mobile-friendly. Cloudmade (then a major OpenStreetMap
user) promoted Leaflet, and many developers welcomed the change.

Even though Derek and I had never worked for the same organization or on the same project,
we had worked in a field where open maps were important and no one wanted to reinvent
the wheel. So we were both familiar with the same open source library.

Leaflet doesn't come with everything. You need to get a base map background.
You need to build all your controls and get all of your data and figure out how
you should be adding that onto the Leaflet map. And, most importantly, you need
to write all of the interaction around it. Leaflet is going to tell me that a marker
is clicked, but I have to keep track of what that marker means, and I have to
write the code deciding what to do next.
