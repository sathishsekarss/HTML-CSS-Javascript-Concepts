Note the images may not be available in the docs at the moment.

**Head tag details**
	Inside the head tag, we have the meta tag, one meta contains charset set to “UTF-8”, which means almost all human readable characters can be used.  The meta tag can also be used to add other information such as name of the author, description of the page etc.

Eg. <meta name=”author” content=”Chris Mills”/>
<meta name=”desription” content=”This page is about cooking”/>

	This meta information will be displayed while our page is searched on google search.

TIP:  specifying a description that includes keywords relating to the content of your page is useful as it has the potential to make your page appear higher in relevant searches performed in search engines ( such activities are termed search engine optimization, or seo ).

     There are also other type’s of meta data.  For more information do research on this topic in MDN site.

To add icon’s to your site, use the link tag as follows

<link rel=”icon” href=”favicon.ic” type=”image/x-icon”/> // even if we want, we can add the sizes attribute too like sizes=”42x42”;

ALWAYS UNDERLINE TEXTS ONLY FOR LINK’S.  IT IS ONLY APPROPRIATE.

Underlining texts other than links is not a good practice.


**Header’s ( h1-h6 )**

	It is really good to use appropriate headers for displaying heading.
		For eg. h1 for main heading, h2 for sub heading, h3 for sub-sub heading and so on.

Always need to follow proper semantics while developing sites. It is really important that you follow the right html semantic elements.
 








**ADDING IMAGES TO WEB PAGES**

	There are two ways to add images to web pages, one through <img/> tag and other through css background-image property.

	What is the difference between both ? Well, the answer is, css background-image property is only used for decoration purposes, we cannot add alt text to it, it will be invisible to screen readers.  While the <img/> tag is used as part of your page content, it as alt attribute to provide alternative text, which helps screen readers.  If you want to decorate, use css background-image property, if you want to add as part of your web page use <img/> property.

	TITLE ATTRIBUTE:  Like in <a></a> tag, we can use the title attribute for images too.  But it is not advised to use tittle attribute ( espcially sharing important information in tittle attribute ), think of the user without keyboard.  Always better to provide text in alt or between the tags in certain cases like ( where the image is placed in <a></a> tag, you can specify the text directly between the tags along with images, try to avoid using title as much as possible. ).

ANNOTATING IMAGES WITH FIGURES AND FIGURE CAPTIONS




The above image is NOT A CORRECT WAY TO ANNOTATE CAPTIONS ALONG WITH IMAGES.  Although this will work without any issues.  Think about the people with screen readers, what if the page has several images, then there will be a confusion on which image goes with which caption.  To solve this issue, figure and figcaption attribute is used.  The below image describes the correct way to use it.



WIDTH AND HEIGHT ATTRIBUTE IN IMAGE TAG:  In image tag, it is better to use width and height attribute. If the internet is slow and image is not downloaded, the page will just allocate the space for the image making it look tidier.

Note:  Do not provide width and height values, above or below the actual image size.  It’ll make the image squished, fuzzy or worse.

ADDING VIDEOS AND AUDIO TO WEB PAGES

	For adding videos and audio to web pages, the <video></video> and <audio></audio> tags are used.

     How do we add the video’s or audio’s to it ? Simple, just add the src attribute and point the url to it.

	What if there are more video types like mp3, mp4 and mpeg for both video’s and audio’s ?
	Well, in that case, we can use < source > tag inside the video or audio tag.  The source tag should contain src attribute for pointing to the video's location and type attribute for defining what type of video file it is ( eg. video/mp4 or video/mp3 etc ).  The type attribute is not mandatory, but IT IS ADVISED TO PROVIDE THE TYPE ATTRIBUTE AS IT WILL HELP IN FASTER PAGE LOAD TIME. ( if we don’t provide the type, the browser will check all types and takes more processing time ).

	You can also include controls attribute in video or audio tag, to get controls like pause, play, full screen, options etc.

	There are other attributes like autoplay, loop, poster ( for display, the picture at start of the video while it in paused state ). Width and height ( both width and height are only available for video types, since the audio types does not have any visual context ).

     ADDING SUBTITLES TO VIDEOS.

          We can add subtitles to our videos simply by creating a filename.vtt and pointing it in <track> element.
	The track element should be used inside the video tag, if the source tag is used, it should be placed after the source tag.
	
	The track tag has attributes like kind ( to specify kind’s like, it caption or subtitles or any other types), src ( to point to the filename.vtt for loading the file contents ), srclang ( in which it is specified ) and label ( for provided language type ).

	For more information on track element and VTT, refer to mdn docs.

	NOTE: Video captions are also used for SEO.


ADDING OBJECT’S AND IFRAMES IN HTML PAGES
	Adding an iframe to our page mean’s simply embedding other web pages into our html page.
	For eg. Youtube allows users to add their video through their own iframe link, which they provide in video’s.  ( it can be accessed through the share button in the youtube ).  Also, it works for maps too.

	Adding iframe’s to our page has also many con’s.  One is the security issue.  It can lead to clickjacking, other harmful things.  Do not include other web page in iframe always, that might lead to copyright issues.

	Object and embed tag’s are used to embed pdf’s and other files types into our web pages.

         For a more detailed explanation on this topic, refer mdn docs.

TIPS:  There are two types of images raster image, which contains the grid of pixels about what color each pixel is and where it is placed etc.

	The other one is vector image. The example of vector image is svg’s.  They contain algorithm about the image details in .svg file in the xml format.


RESPONSIVE IMAGES
	Rather than downloading all the images for all the screen, it is appropriate to download appropriate images for appropriate screen.  For example a mobile browser might not need a very long width image that is used to desktop, it may be cropped for mobile devices.  This method saves as a  network bandwidth while the page is loading, since desktop images used to be larger in size and mobile device images are smaller in size.

	We usually provide “src” and “alt” attribute in img tag ( void element ), but it is also advised to use “srcset” and “sizes” attribute to load differently sized images, based on the size of the screen.

	We can also use a picture element, which has several sources inside it, to load different images for different screen sizes.  See the below image for example.



	Here, the default image is taken from the img tag, and the other images load based upon the screen size.


TABLE’S IN HTML

	Table’s in html are used to display tabular data.  Back in the day’s table’s were also used to display layout’s for the page, where it contains header’s and footer’s ( BUT, THIS SHOULD BE STRICTLY AVOIDED ).  Table’s should only be used for displaying tabular data.

th Element -  This element is to indicate that it is a table header.  It is not the same as thead element, they are different.

td Element - This element represent individual cells in the table.  td stands for Table Data.

tr  Element -  This element represent’s individual rows in the table.
	Eg.  <tr><td>one</td><td>two</td></tr>

These are the basic elements inside the table tag.

Designing Column’s

	Sometime’s we need to add color’s to specific columns alone.  We cannot add the colors to each rows cell to set the column color.

	In that case we can use the col element, this col element needs to be wrapped inside the colgroup element. Eg.  See the image below.



You can see the color of the column is set through the col element, which is inside the colgroup.

If you don’t want to color other column you can leave it empty, but you have specify just the col element without attributes, like they did for the first column in the example.

CAPTIONS: We can add caption tag to the table and provide captions for the displayed table.  It will be useful, to determine what data the table is showing.  The captions tag should be added after the table opening tag.

Thead,tbody,and tfoot -  These three tags are actually responsible for displaying the table’s data.  We can even create table without these tag, the browser will automatically add the tbody tag to the table.  The thead tag is used to hold the header row of the table.  The tbody tag is used to hold the main contents of the table.  The tfoot tag is used to hold the footer content for the table.  Even if you swap these tag order’s, they’ll be properly rendered by the browser in correct way.

Note:  We can also nest table’s inside one table, but this generally not advised.

Scope attribute in table’s.  For more information about this attribute, refer mdn docs.

