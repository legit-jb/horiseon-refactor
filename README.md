# Horiseon Refactor
## Description
To quote the User Guide for the project:

AS A marketing agency
I WANT a codebase that follows accessibility standards
SO THAT our own site is optimized for search engines

I added Alt text to all images.
The use of a background image is still in the style.css as it is largely aesthetic. As a background image in the style.css, it doesn't get alt text. However, as a curtasy and to ensure that the extra mile was taken in reguards to accessibility, 

"<span role="img" aria-label="people at a conference table collaborating on bussiness and search optimization strategies"> </span>"

was added to give some text if it can be read. If it is skipped, the consumer doesn't miss any needed information. Its more of a bunus.

**********NOTE***********
Since accessibiily compliance was a priority, a style change needed to be made.

This:
```md
    ![original element with an image with right float property](./assets/images/original.png)

to this:
```md
    ![changed element with the image floated to the left](.?assets/images/changed.png)

If an image is floated right then a reader will not convey the setup correctly as it only reads HTML.

I would discuss this change and work on a solution.

As I was going through the style.css and index.html I consolidated extraneous code. For example:

The original code of:
.search-engine-optimization h2 {
    margin-bottom: 20px;
    font-size: 36px;
}

.online-reputation-management h2 {
    margin-bottom: 20px;
    font-size: 36px;
}

.social-media-marketing h2 {
    margin-bottom: 20px;
    font-size: 36px;
}

was consolidated to:

h2 {
    margin-bottom: 20px;
    font-size: 36px;
}

This was done throughout the code. As well as cleaning up any extraneous symbols such as:

<img src="./assets/images/cost-management.png"></img>

was changed to:

<img src="./assets/images/social-media-marketing.jpg" alt="people at a table intering with a laptop, tablets, and icons showing social media buzzwords such as tweet and share">
***(the ending </img> was unnecesary and deleted)***

