Table of contents
- [Head tag](#headTagDetails)
- [Headers tag](#headersTag)
- [Adding images to web pages](#addingImages)
- [Adding videos and audios to web pages](#addingVideosAudios)

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

## Headers tag
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

## Adding videos and audios to web pages
For adding videos and audio to web pages, the video and audio tags are used.

How do we add the video’s or audio’s to it ? Simple, just add the src attribute and point the url to it.

**What if there are more video types like mp3, mp4 and mpeg for both video’s and audio’s ?**

Well, in that case, we can use < source > tag inside the video or audio tag.  The source tag should contain src attribute for pointing to the video's location and type attribute for defining what type of video file it is ( eg. video/mp4 or video/mp3 etc ).  The type attribute is not mandatory, but IT IS ADVISED TO PROVIDE THE TYPE ATTRIBUTE AS IT WILL HELP IN FASTER PAGE LOAD TIME. ( if we don’t provide the type, the browser will check all types and takes more processing time ).

You can also include controls attribute in video or audio tag, to get controls like pause, play, full screen, options etc.

There are other attributes like autoplay, loop, poster ( for display, the picture at start of the video while it in paused state ). Width and height ( both width and height are only available for video types, since the audio types does not have any visual context ).

**ADDING SUBTITLES TO VIDEOS.**

We can add subtitles to our videos simply by creating a filename.vtt and pointing it in <track> element.

The track element should be used inside the video tag, if the source tag is used, it should be placed after the source tag.
	
The track tag has attributes like kind ( to specify kind’s like, it caption or subtitles or any other types), src ( to point to the filename.vtt for loading the file contents ), srclang ( in which it is specified ) and label ( for provided language type ).

For more information on track element and VTT, refer to mdn docs.

NOTE: Video captions are also used for SEO.




