# Election Map

As you're making maps, you've probably noticed that they often look alike. Like our
school maps, Greenland and South America are distorted until they appear to have a
similar size. The map we use is known as the Mercator projection. Years after
The West Wing stunned viewers and YouTubers with "the Peters projection", why are
our web maps so uniform?

Frankly it's a question of standards and first movers. Web maps started using a
common standard for how 3D is mapped to 2D. When other mappers joined, they followed
suit. If they didn't, data from two different groups couldn't be overlaid.

For some maps, we want to revisit these design choices. The best example is the
election map. We don't want to scroll to see Hawai`i, zoom out to view the
supermassive Alaska, or see one bit of Canada.

If you want the classic map of the continental US with Alaska and Hawai`i as
neighbors in the corner, you should check out the JavaScript library D3.

## Different D3 projections
