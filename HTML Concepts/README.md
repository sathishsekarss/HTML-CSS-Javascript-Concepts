Table of contents
- [Head tag](#headTagDetails)
- [Headers tag](#headersTag)
- [Adding images to web pages](#addingImages)


# Head tag

Inside the head tag, we have the meta tag, one meta contains charset set to “UTF-8”, which means almost all human readable characters can be used.  The meta tag can also be used to add other information such as name of the author, description of the page etc.

Eg. <meta name=”author” content=”Chris Mills”/>
<meta name=”desription” content=”This page is about cooking”/>

This meta information will be displayed while our page is searched on google search.

TIP:  specifying a description that includes keywords relating to the content of your page is useful as it has the potential to make your page appear higher in relevant searches performed in search engines ( such activities are termed search engine optimization, or seo ).

 There are also other type’s of meta data.  For more information do research on this topic in MDN site.

To add icon’s to your site, use the link tag as follows

<link rel=”icon” href=”favicon.ic” type=”image/x-icon”/> // even if we want, we can add the sizes attribute too like sizes=”42x42”;

**ALWAYS UNDERLINE TEXTS ONLY FOR LINK’S.  IT IS ONLY APPROPRIATE.**

Underlining texts other than links is not a good practice.

## Headers tag ( h1-h6 )f
It is really good to use appropriate headers for displaying heading.
For eg. h1 for main heading, h2 for sub heading, h3 for sub-sub heading and so on.

Always need to follow proper semantics while developing sites. It is really important that you follow the right html semantic elements.

## Adding images to web pages

There are two ways to add images to web pages, one through <img/> tag and other through css background-image property.

What is the difference between both ? Well, the answer is, css background-image property is only used for decoration purposes, we cannot add alt text to it, it will be invisible to screen readers.  While the <img/> tag is used as part of your page content, it as alt attribute to provide alternative text, which helps screen readers.  If you want to decorate, use css background-image property, if you want to add as part of your web page use <img/> property.

**TITLE ATTRIBUTE:**  Like in <a></a> tag, we can use the title attribute for images too.  But it is not advised to use tittle attribute ( espcially sharing important information in tittle attribute ), think of the user without keyboard.  Always better to provide text in alt or between the tags in certain cases like ( where the image is placed in <a></a> tag, you can specify the text directly between the tags along with images, try to avoid using title as much as possible. ).

**ANNOTATING IMAGES WITH FIGURES AND FIGURE CAPTIONS**

The above image is NOT A CORRECT WAY TO ANNOTATE CAPTIONS ALONG WITH IMAGES.  Although this will work without any issues.  Think about the people with screen readers, what if the page has several images, then there will be a confusion on which image goes with which caption.  To solve this issue, figure and figcaption attribute is used.  The below image describes the correct way to use it.


**WIDTH AND HEIGHT ATTRIBUTE IN IMAGE TAG:**  In image tag, it is better to use width and height attribute. If the internet is slow and image is not downloaded, the page will just allocate the space for the image making it look tidier.


**Note:**  Do not provide width and height values, above or below the actual image size.  It’ll make the image squished, fuzzy or worse.



