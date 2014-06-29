 These are all great scenarios for sharing OpenStreetMap data, but sometimes users are sharing data that isn’t permanent. When I was in college, there was a day when there was snow on the ground in all 50 states (yes, including the slopes of Mauna Loa in Hawai`i). A student meteorologist in Kansas was collecting photos and asked how to map them all, so I developed an AppEngine project, and we worked through the bugs.

The key concept behind SnowShot is that a curator receives photos by e-mail, and then forwards them to a secret SnowShot e-mail with the location in the subject headline. The server can then upload the photo and attach it to the map.
Our greatest difficulty was when people e-mailed large photos, it was too big for Google AppEngine’s blob store, and when we used Python image libraries to shrink the photos, it took up time and processing power which broke the service.

Here’s how you can set up an app with an instant post e-mail or with a curator page.

