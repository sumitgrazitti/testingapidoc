# What is Depth?

Depth is the distance of a page from the home page. The home page has ```depth``` of ```1```. Any page linked to from the home page has ```depth``` of ```2```.

### Crawling and Depth
Consider the following image:

![alt text](https://i.ibb.co/H2VRYN7/depth.png)

#### Index SearchUnify Home Page
If ```depth==1```, then the SearchUnify crawler will index only the home page.
#### Index  Home Page + Platform + Solutions + Resources + Company 
If ```depth==2```, then the SearchUnify crawler will index the home page and the pages linked to from the home page. The latter pages have been colored yellow in the diagram.
#### Index  Home Page + Platform + Solutions + Resources + Company + the Pages in Green
If ```Index ==3```, then the SearchUnify crawler will index home page, the pages linked to from the home page, and the pages linked to by the yellow-colored pages. The last category has been highlighted green in the diagram.

And it goes on.

### Best Practices

1. Strive to assign an accurate value to ```depth```. Crawling time increases exponentially with depth.
2. Keep ```depth``` less than ```5```, unless your website is the size of Wikipedia.
