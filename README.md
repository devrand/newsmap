# newsmap
One of vis for our project about fake news.
The task was to show a vast landscape of content, by showing many headers from an actual news. They were sampled from 50,000 news with worst quality (due to our model). They are clustered by 6 main themes and some subtopics. So idea was to show them as a "news map", with zoom and pan.

So we need a layout which will place similar news close together, using some automatic label placement to prevent overlapping.
To achieve this I've used two steps (in prepare_labels_treemap.html):
1. created initial positions for each label with a help of d3.treemap layout algo
2. deployed simulating annealing algo to adjust labels into positions where they will not be overlapped. 

Index.html is for displaying the result, with d3.zoom on the canvas
