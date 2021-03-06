---
title: Food Blogs and the Future of MR on the Web
date: 2018-01-18 14:01:52.291000000 -05:00
categories:
- webxr
- musings
tags:
- photogrammetry
- volumetric video
- end-user content creation
- blogging
author: blair
layout: post
---

{% marginfigure 'dl1' 'assets/uploads/davidlebovitz.png' "David Lebovitz's [Pasta recipe](https://www.davidlebovitz.com/how-to-make-fresh-pasta-homemade-recipe/)." %}
Last year, I posted some musings on the question ["What is an MR Blog?"](/2017/11/14/what-is-an-mr-blog/). Perhaps this question would be better phrased as "what will the equivalent of the common blog be for MR content?", since "blog" is really just a placeholder for "non-trivial collection of content that lots of people can create and share". 

While web-based MR will be used for similar applications and experiences as native MR (games, for example), the exciting thing about the web is the shear volume and variety of small bits of content, from opinions to stories to art to commentary to news, on self-hosted sites or places like [Wordpress](https://wordpress.com) or [Tumblr](https://www.tumblr.com/).

{% marginfigure 'sc1' 'assets/uploads/shecooks.png' "Pork Belly recipe on [She Cooks He Cleans](https://shecookshecleans.net/2012/04/30/maple-bourbon-smoked-pork-belly/)." %}
I've been throwing this question at people over the past month or so, and have started to think of the problem in a different way. I suspect these new media forms will emerge organically, but to do so, it has to be possible for people to easily create and explore ideas for MR experiences. Which really makes this an end-to-end problem: what makes blogging possible is that the content elements people put in blogs (text, pictures, videos) are easy to create, edit and mix together. The creative challenge is in the ideas and the creation and curation of individual elements, and the bar for creating something passable is very low: professional quality sites, with beautiful photographs and prose, can take a lot of time to create, but passable pictures and text can be created quickly by anyone. 

{% newthought 'So, asking "what is the MR equivalent to a blog?"' %} is intimately tied to the question "what kind of 3D content can we create, edit and mix together, easily and quickly?" Answering this question is essential to even considering "what kinds of compelling experiences can we create with that content?"
{% marginfigure 'dl2' "assets/uploads/davidlebovitz-2.png" "Beautiful, instructional images are core to recipe blogs; here are more images from the pasta recipe." %}

One example that crystalized this for me was food blogs. Over the holidays, I found myself looking up recipes on the web, and running across a lot of interesting food blogs were more than just traditional collection-of-recipe sites like [allrecipes.com](http://allrecipes.com), such as [David Lebovitz](https://www.davidlebovitz.com/)'s blog.
Food blogs often mix recipes and stories, more blog or magazine than recipe book. They can get quite detailed, too, and usually include lots images and videos (to help the reader understand and follow along, but also to entertain and tantalize; see the images in the sidebar). 


When you think about what it takes to create one of these posts, the steps are those mentioned above: gather images for the food and/or the cooking process, write the text, and lay out the story using whatever tools your blog system provides{% sidenote 'whatever' 'I understand this requires some skills, creativity, and imagination. But the technical barriers are not what prevents people from publishing content on the web.' %}. This might require HMTL and CSS editing, or (more likely) higher level tools like Wordpress's editor or (as I use on this blog) Liquid and Markdown tags that are processed by Jekyll.

{% newthought "What would the analogous steps" %} be to add MR content to stories like this? Cooking is one of the most commonly cited examples of how AR content might be useful to consumers: a cook's hands are busy (and often dirty), they are moving around the space (away from a small single screen like a phone or laptop), they are doing many things at once, and often need to refer to instructions _while_ they are doing the task. So, what would be required to take the pasta receipe above, and have some sort of "responsive MR web template" be able to display the content on an AR head worn display?

Let's ignore navigation and interaction: how the cook "pages through the steps" will be tied to the input capabilities of the device they are using, and might include gestures and voice. Lets also ignore any sort of magical AI that lets us recognize what the user has or hasn't done, know that ingredients need to be choped "over there", what part of the receipe each of the pots on the stove correspond to, or how to talk to the internet-connected appliances and relate them to the bits of the instructions. 

Just consider the simplest case, analogous to the pasta recipe above: the author wants to show the cook a series of steps, illustrated with visuals to help them see the steps and understand what the author considers are the essential parts of how each might work.

{% newthought "The first" %} challenge is layout. For that, an MR-capable design template might provide relatively simple, predictable support for authors, without tackling sophisticated layout problems. For example, imagine an author being able to specify "I need 3 places near the user: a fixed location for some descriptive text, a fixed location for visual elements, and a floating location that stays near the user for reminders and status". 

The page generated by this template might then ask the user up front "Point to a vertical surface where you want the text to appear; now point to a horizontal surface where you would like the visual instructions to be placed"{% sidenote "handwaving" "Yes, yes, this is vague and may not be best, but at least it feels like something that could be implemented." %}. Such a template might also allow the author to tag areas of content in their story as belonging to one of these areas (including possibly having different bits of content for 2D and MR presentation, just as some responsive sites do now for phone and desktop presentation).

While vague, this feels tractable. But it begs the question, "What are the content elements, especially the visual elements?" Surely such an author wouldn't just want to place images, text and video in the 3D world. 

{% newthought "The second" %} challenge, then, is content creation.  One of the immediate appeals of MR is the possibility to integrate virtual 3D content into the user's view of the physical world, letting people view things from different sides, and possibly give them new or better insights into something. 

What if it was just as easy to create a 3D model of food and ingredients at each step in a recipe, just as easy as taking and editing pictures?  Consider this 3D model of a 
<a href="https://sketchfab.com/models/7781337f561241e1974809a8c6783efd?utm_medium=embed&utm_source=website&utm_campain=share-popup" target="_blank">baklava</a>:

<figure>
<figcaption>Turkish Baklava created by <a href="https://sketchfab.com/kabaq?utm_medium=embed&utm_source=website&utm_campain=share-popup" target="_blank">Kabaq Augmented Reality Food</a> and hosted on <a href="https://sketchfab.com?utm_medium=embed&utm_source=website&utm_campain=share-popup" target="_blank">Sketchfab</a>
</figcaption>
<iframe width="100%" height="275px" src="https://sketchfab.com/models/7781337f561241e1974809a8c6783efd/embed" frameborder="0" allowvr allowfullscreen mozallowfullscreen="true" webkitallowfullscreen="true" onmousewheel=""></iframe>
</figure>

While still difficult, capturing realistic models of real objects is getting easier. This is different than the work being done to make editing 3D models easier, such as Google's [Blocks](https://vr.google.com/blocks/) _in-situ_ 3D editor. For our purposes here, these manual editing approaches completely miss the mark. No matter how "easy" (relative to professional tools like Maya or 3D Studio), manual editing cannot be fast enough, or capable of creating 3D versions of food that is on par with a photograph.  

This kind of experience needs a 3D equivalent to the photograph: something that attempts to capture what a part of the real world really looks like, that can be displayed in 3D. The approach used to create the baklava above is called [photogrammetry](https://en.wikipedia.org/wiki/Photogrammetry).  It involves collecting many images of an object and extracting the 3D structure and material properties from them. [Various software solutions](https://en.wikipedia.org/wiki/Comparison_of_photogrammetry_software) have been developed over the years, but have traditionally been difficult and time consuming to use, especially if you want a polished model without unsightly artifacts or holes. New solutions are popping up that hope to simplify the process, including a relatively cheap, turnkey solution shown by HP at CES this year (the [Z 3D Camera](http://www8.hp.com/us/en/campaigns/z-3d-camera/overview.html)). Approaches like this are promising, and point the way toward rapid creation of simple MR experiences.

{% newthought "But why stop" %} at pictures and static models? While more complicated, more sophisticated experiences might want to include 3D equivalents to video: imagine seeing the hands of a chef kneeding the dough above, on the counter beside where you are working? Creating, storing, and rendering 3D video is a much more challenging task than creating a single 3D model, but is also getting closer to reality. Here's a video clip of the current web page for one project trying to solve this problem:

<figure>
<figcaption>
Microsoft has created a <a href="https://www.microsoft.com/en-us/mixed-reality/capture-studios">Capture Studio for Voumetric Video</a> to explore creating and sharing volumetric video.
</figcaption>
<iframe width="100%" height="275" src="https://player.vimeo.com/video/251672052" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>
</figure>

While this solution is not accessible to average consumers, it demonstrates that it is feasible, and points the way toward possible solutions.

{% newthought "This challenge" %} of capturing, editing and sharing static or moving parts of the world, as easily as amateur's can currently create and sharing pictures and videos, is going to be a key hurdle that must be crossed if non-professionals are going to create and share MR content. There will be other elements needed to support a broad spectrum of content and experiences, of course: easily animated avatars (to act as stand-in "actors" in stories), more natural ways of controlling how content is laid out in a space (in contrast to the simple "three places" example above), and social services for creating shared experiences, to name a few.

Whatever these bits of content and underlying services are, the tools presented to end users will need to be simple and accessible if MR on the Web is going to achieve the kind of broad and varied use, the long tail of content, that we have come to know and love.
