---
title: Co-Authorship
layout: page-narrow
permalink: /coauthorship.html
# include CollectionBuilder info at bottom
#credits: true
# Edit the markdown on in this file to describe your collection
# Look in _includes/feature for options to easily add features to the page
---

# Co-authorship

- Node (circle) size indicates number of times the work has been cited since publishing
- The node color and distance indicates a group (or cluster) formed by subject and keyword likeness, academic fields of study in this case
- Edges (lines) connecting nodes indicate shared __co-authorship of papers__

{% capture modal1 %}

Beginning with the top right hand corner of the screen, select the __frame icon__ to enter full screen, the __sun icon__ if you prefer a light background, the __camera icon__ to download a screenshot and the last three to share, save a version and open the JSON file of the visualization.

<img src="https://objects.lib.uidaho.edu/twrs/how_to_a.gif"  class="img-fluid" alt="Instructional gif demonstrating functionalities of VOSviewer" >

Hover over (or select it to keep open) a node (circle) to highlight work that it's connected to either in citation, co-authorship or attribute depending on which of these you explore. This will also reveal an information panel on the bottom of the screen that will provide the __author(s), title, source, year__ and __total number of times that work was cited__ in subsequent research papers. If a copy of the research paper is available, select the blue URL on the right hand side of the information panel to open this up in a new window.

<img src="https://objects.lib.uidaho.edu/twrs/how_to_b.gif"  class="img-fluid" alt="Instructional gif demonstrating selecting nodes, reading instructional panes and exploring individual research papers" >

Data may be hidden by larger nodes, so use the control panel on the right hand side or your scroll wheel on a mouse to zoom in.

<img src="https://objects.lib.uidaho.edu/twrs/how_to_d.gif"  class="img-fluid" alt="Instructional gif demonstrating zooming in and out" >

{% endcapture %}

{% include feature/modal.html button="Need Help?" color="info" title="Configuration" size="xl" text=modal1 %}

<iframe
  allowfullscreen="true"
  src="https://app.vosviewer.com/?json=https%3A%2F%2Fdrive.google.com%2Fuc%3Fid%3D17S1Q2wYTit-yj-DxBKeYnLQBPSr2ICty&item_color=1&item_size=4&dark_ui=true"
  width="100%"
  height="75%"
  style="border: 1px solid #ddd; max-width: 1200px; min-height: 500px"
>
</iframe>