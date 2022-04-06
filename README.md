# HTML and CSS Lab

This tutorial was written by [Lindsay K. Mattock](http://lindsaymattock.net) and adapted by [Katherine Walden](https://github.com/kwaldenphd) and [John Templeton](https://github.com/jmtemple). 

<a href="http://creativecommons.org/licenses/by-nc/4.0/" rel="license"><img style="border-width: 0;" src="https://i.creativecommons.org/l/by-nc/4.0/88x31.png" alt="Creative Commons License" /></a>
This tutorial is licensed under a <a href="http://creativecommons.org/licenses/by-nc/4.0/" rel="license">Creative Commons Attribution-NonCommercial 4.0 International License</a>.

As you read in your assigned reading for this week, both of these languages require a specific syntax. The reading from w3 Schools suggested downloading a text editor to create your html files. Your computer likely already has some text editor options (Notepad or Notepad ++ for PC users, or Text Editor for Mac users). Personally I use/would recommend VS Code as your source code editor: ([Download Here](https://code.visualstudio.com/#alt-downloads)).

## Lab Objectives

By the end of this lab you will be able to:
- Generate HTML pages that include links, images, and tables
- Generate CSS stylesheets to format your HTML pages
- Become more familiar with how web data is formatted for future projects

## Acknowledgements

This lab is based on the "Project 3: HTML/CSS" project materials developed by [Lindsay K. Mattock](http://lindsaymattock.net/) for the the [SLIS 5020 Computing Foundations course](http://lindsaymattock.net/computingfoundations.html). 

# Table of Contents
- [What is HTML?](#what-is-html)
  * [Hello World!](#hello-world)
- [Creating an HTML File](#creating-an-html-file)
  * [Adding Content to `Index.html`](#adding-content-to-indexhtml)
- [Building Additional Web Pages](#building-additional-web-pages)
- [Creating Links in HTML](#creating-links-in-html)
- [Adding Images in HTML](#adding-images-in-html)
- [Building Tables in HTML](#building-tables-in-html)
- [Using HTML Styles](#using-html-styles)
- [Using Cascading Style Sheets](#using-cascading-style-sheets-css)
  * [Creating and Implementing CSS](#creating-and-implementing-css)
- [Creating a Website](#creating-a-website)
- [Endnotes](#endnotes)
- [Lab Questions](#lab-questions)

# What is HTML?

1. HTML stands for HyperText Markup Language

<blockquote>“HyperText is the method by which you move around on the web — by clicking on special text called hyperlinks which bring you to the next page. The fact that it is hyper just means it is not linear — i.e. you can go to any place on the Internet whenever you want by clicking on links — there is no set order to do things in.

<ul><li>"Markup is what HTML tags do to the text inside them. They mark it as a certain type of text (italicised text, for example).</li>
 <li>"HTML is a Language, as it has code-words and syntax like any other language.”</em><sup><a href="#fn1" id="ref1">1</a></sup></li></ul></blockquote>

2. HTML is all about sharing, storing, and accessing information. HTML provides the background for the World Wide Web.

## Hello World!

```HTML
<html>
<body>Hello World</body>
</html>
```

3. This is a very basic HTML document. The HTML tags `<HTML>` identify this document as a html document. The body tags `<body>` enclose the content that will be visible on the page.
   
4. Download the `hello_world.html` file ([link to Google Drive download, ND users only](https://drive.google.com/drive/folders/1Kw82eAyMXyJdH6stajbH2oFJRMpY2ZCX?usp=sharing)) and open it in a web browser on your computer. You should see just the text “Hello World!” The browser has translated the HTML tags and returned only the text.

5. `helloworld.html` contains the minimum requirements for an HTML document. However, it is best practice to create a HTML document that is “well formed,” that is, that it follows all of the grammar, vocabulary, and syntax rules of html. We can check the well-formed-ness of this document in a validator like the W3C Markup Validation Service https://validator.w3.org. 

6. Click on “Validate by Direct Input” and copy and paste the code above into the validator and click `check`. You should receive a few errors. 
- [W3Schools, "HTML head tag"](https://www.w3schools.com/tags/tag_head.asp)
- [W3Schools, "HTML !DOCTYPE Declaration"](https://www.w3schools.com/tags/tag_doctype.asp)
- [W3Schools, "HTML ISO Language Codes"](https://www.w3schools.com/tags/ref_language_codes.asp)
  
7. While our browser was able to interpret the code from helloworld.html, this document does not follow all of the rules of the current version of HTML. 

8. HTML is pretty forgiving, but other languages are not, so it’s best to practice following all of the rules from the start.

<blockquote>Q1: Try to interpret a few of these errors in your own words. HINT: The W3Schools resources listed under step 5 provide more information or explanation on some of these errors.</blockquote>

# Creating an HTML File

9. Let’s make a few modifications to the `Hello World` file that will make it more valid. Navigate to the htmltemplate.zip file given to you for this   lab and open the index.html document.

10. In this .html file you will first notice we have the document type declaration beginning with `<!DOCTYPE`. In this case, the document type is followed by `html`. This is simply telling the computer that what follows is a HTML document. 

11. Next we see the opening HTML tag, but there are a few additional attributes here: `<html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en" lang="en">` 

12. This is just another piece of the XHTML specification. 

13. The namespace provides a means of disambiguation between elements with the same name. We won’t run into this issue in this lab. 

14. Also note here that the document language is declared as English with the `en` code with a standardized abbreviation for the English language.

<blockquote>XHTML 1.0 Documentation http://www.w3.org/TR/xhtml1/</blockquote>

<p align="center"><a href="https://github.com/jmtemple/HTML-CSS/blob/master/images/Image_3.png?raw=true"><img class="aligncenter" src="https://github.com/jmtemple/HTML-CSS/blob/master/images/Image_3.png?raw=true" /></a></p>

15. What follows are the tags that define the structure of a basic HTML document as illustrated in the W3C reading this week.

16. The `index.html` file included in the project template reflects HTML that is well-formed and valid. 

17. We can test this by copying and pasting our file into the HTML Validator. (Go ahead and give it a try https://validator.w3.org). 

# Adding Content to `Index.html`

18. At the moment, our document doesn’t have any real content – let’s add some.  Between the `<head>` tags you will see a set of `<title>` tags. 

19. As the diagram illustrates, this data is not presented in the browser. This is true for the most part. 

20. The `<head>` of the document is reserved for metadata, but also includes the `<title>` of the page which is represented in the tabs in some web browsers. 

```html
  <head>
    <title>YOUR PAGE TITLES GOES HERE</title>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width">
  </head>
```

21. Replace “YOUR PAGE TITLE GOES HERE” between the `<title>` tags to give your document a new title.

<blockquote>Q3: Between the head tags, there are also a few meta tags. Use the W3C site to translate this information in your notebook.<br>
Some resources that can help you get started:
<ul>
 <li><a href="https://www.w3schools.com/tags/tag_meta.asp">W3Schools, "HTML Meta Tag"</a></li>
 <li><a href="https://www.w3schools.com/tags/att_meta_charset.asp">W3Schools, "HTML Meta Charset Attribute</a></li>
 <li><a href="https://www.w3schools.com/css/css_rwd_viewport.asp">W3Schools, "Response Web Design With Viewport"</a></li>
 </ul>
</blockquote>
  
22. Now, let’s modify the body. This is where the content that we will see in the web browser is entered. 

23. HTML uses a number of different formatting tags. You can use the W3Schools ["HTML Reference"](https://www.w3schools.com/tags/default.asp) to browse through some of the different options. 

24. For now, we’ll use `<h1>` and `<p>`.

25. After the first `<body>` tag, place a `<h1>` tag on a new line. 

26. Notice two things:
- The line is indented. This isn’t a requirement of HTML, but it is a convention that is used by coders to write cleaner code. The indentation allows you to easily determine what tags are nested within each other. For example, the `<title>` and `<meta>` tags are nested within the `<head>` tags. Now, our `<h1>` is nested within the `<body>`. The use of the tabs simply makes the code easier for us to read, but the computer doesn’t care (with Python the indentation is important and will cause errors if the indents do not appear in the right place).
- The editor completed your `<h1>` with a closing `</h1>` tag. The closing tag is not required for all HTML tags, but it is good practice to close all of your tags. This is a good example. Without a closing tag, everything that follows will be formatted as a `<h1>`. 

<p align="center"><a href="https://github.com/jmtemple/HTML-CSS/blob/master/images/Image_5.jpg?raw=true"><img class="aligncenter" src="https://github.com/jmtemple/HTML-CSS/blob/master/images/Image_5.jpg?raw=true" /></a></p>

27. Go ahead and update the content between the `<h1>` tags. `<h1>` is preformatted as first level heading text. We’ll see how it looks in a minute. 

<p align="center"><a href="https://github.com/jmtemple/HTML-CSS/blob/master/images/Image_6.jpg?raw=true"><img class="aligncenter" src="https://github.com/jmtemple/HTML-CSS/blob/master/images/Image_6.jpg?raw=true" /></a></p>

27. Next add a `<p>` tag and type some text. `<p>` tags are preformatted as paragraphs with padding between paragraphs.

<p align="center"><a href="https://github.com/jmtemple/HTML-CSS/blob/master/images/Fig_J.png?raw=true"><img class="aligncenter" src="https://github.com/jmtemple/HTML-CSS/blob/master/images/Fig_J.png?raw=true" /></a></p>

28. At any time you can check the way that your code will render by saving, and clicking on the .html link/refreshing the page. 

29. Save the file in a dedicated folder for this project, and call it `index.html.`

<blockquote>Why <code>index.html</code>? <code>index.html</code> is the name of the default landing page for websites. The web server (the computer hosing the site) will automatically recognize <code>index.html</code> as the first page or the home page of a website. Some servers use other variations like <code>home.html</code>, but we’ll use <code>index.html</code>.</blockquote>

# Building Additional Web Pages

30. What we have just created is a single web page. If we want to build a web site, we have to link this page to additional pages of content. 

31. Let’s create a second `.html` file and save this file as `page2.html`. You can do this by duplicating the index.html file and then renaming. Hint: this will also help us make sure we're starting with an HTML document that is well-formed and valid.

32. Now add some new content to your second page. Be sure to add a title, `<h1>` and `<p>` tags. 

# Creating Links in HTML

33. Now, let’s add a link to the second page on our `index.html` page. 

34. We add links with the `<a href>` tag. This tag allows us to link pages in the same website and link out to pages that exist on external websites.

35. The tag syntax is as follows: `<a href="URL to page">Text that will appear as the link</a>`. 
  
36. Below your paragraph tag on the `index.html` page add the line `<a href=”page2.html”>Link to page 2</a>.`
- Learn more about the `<a href>` tag via W3Schools: http://www.w3schools.com/TAGS/att_a_href.asp

<p align="center"><a href="https://github.com/jmtemple/HTML-CSS/blob/master/images/Image_10.png?raw=true"><img class="aligncenter" src="https://github.com/jmtemple/HTML-CSS/blob/master/images/Image_10.png?raw=true" /></a></p>

37. Run `index.html` to see the updated file with a link. 

38. When you click on “Link to page 2” your `page2.html` file should open. In this case, our URL to the page in our `<a href>` tags is just the name of new page we created. 

39. We do not need a full URL (http://www.somewhere.com) because we are calling a file that is stored in the same directory on our machine. 

40. If we had saved this file to another folder or directory, we would need to include the full file path, including any directory information.
- For example if we had put `page2.html` in a folder titled "Page_Two," the `a href` tag would look like `<a href="Page_Two/page2.html">`.

# Adding Images in HTML

41. Let’s add an image to the `index.html` page. 

42. Find an image that you like on the web, save it to your local computer in the dedicated file location of your project (e.g., where the index.html and page2.html exist).

43. The `<img>` tag is very similar to the `<a href>` tag that we just used. 
- Learn more about the `<img>` tag via W3Schools:  http://www.w3schools.com/tags/tag_img.asp

44. The tag has two required attributes:
- `src` or the source
-  `alt` or the alternative text for the image

45. The `src` can be a local file or a URL to an image on the web, just like the href attribute in the `<a href>` tag. 

46. The `alt` is for the alternative text or the text that is displayed for screen readers or browsers like lynx that don’t support images. 

<p align="center"><a href="https://github.com/jmtemple/HTML-CSS/blob/master/images/Fig_M.png?raw=true"><img class="aligncenter" src="https://github.com/jmtemple/HTML-CSS/blob/master/images/Fig_M.png?raw=true" /></a></p>

47. On your `index.html` page, add the line `<img src="imagefilename" alt=Description of image>` in the `<body>`.

48. Be sure to use your image file name in place of the italicized text above. 

<p align="center"><a href="https://github.com/jmtemple/HTML-CSS/blob/master/images/Image_12.jpg?raw=true"><img class="aligncenter" src="https://github.com/jmtemple/HTML-CSS/blob/master/images/Image_12.jpg?raw=true" /></a></p>

49. View the created page in your browser to see if the image has loaded correctly.

<blockquote>Q4: If you haven't already, modify index.html to include a link to a second HTML file. Next, add an image to index.html.</blockquote>

<blockquote>Q5: Move the image you added in Q4 into a new "Images" folder. What happens when you save and run the code? What would you need to modify in the HTML to correctly display this image?</blockquote>

# Building Tables in HTML
 
50. HTML uses a few core tags for web pages that include tables.
- `table` (marks the start and end of a table
- `tbody` (marks the start and end of the table body)
- `tr` (marks the start and end of each table row)
- `th` (marks the start and end of each column in the first row of the table)
- `td` (marks the start and end of each column after the first row of the table)

51. How we might see those tags combined in a table structure:

```HTML
<table>
 <tr>
  <th>First Column Header</th>
  <th>Second Column Header</th>
  <th>Third Column Header</th>
 </tr>
 <tr>
  <td>Data in first column/first row</td>
  <td>Data in second column/first row</td>
  <td>Data in third column/first row</td>
 </tr>
 <tr>
  <td>Data in first column/second row</td>
  <td>Data in second column/second row</td>
  <td>Data in third column/second row</td>
 </tr>
</table>
```

52. The output of that HTML would look like:

<table>
 <tr>
  <th>First Column Header</th>
  <th>Second Column Header</th>
  <th>Third Column Header</th>
 </tr>
 <tr>
  <td>Data in first column/first row</td>
  <td>Data in second column/first row</td>
  <td>Data in third column/first row</td>
 </tr>
 <tr>
  <td>Data in first column/second row</td>
  <td>Data in second column/second row</td>
  <td>Data in third column/second row</td>
 </tr>
</table>

53. Additional attributes like `align`, `style`, etc. can be used with many of these tags.

54. For more on building tables in HTML:
- [W3Schools, "HTML Tables"](https://www.w3schools.com/html/html_tables.asp)
- [W3Schools, "HTML table tag"](https://www.w3schools.com/tags/tag_table.asp)

<blockquote>Q6: Add a table to one of your HTML pages (index.html or page2.html). You could create fictional data or add meaningful data from another source. What challenges did you face getting the table to display and function like you expected?</blockquote> 

# Using HTML Styles

55. HTML allows us to add style to our pages internally, or inline, using HTML tags. 

56. We’ve already styled our pages a bit using the `<h1>` tag. `<h1>` designates preformatted text that is larger than the `<p>` or paragraph text. But, what if we want to add color or change the font on our page? 

<p align="center"><a href="https://github.com/jmtemple/HTML-CSS/blob/master/images/Image_13.jpg?raw=true"><img class="aligncenter" src="https://github.com/jmtemple/HTML-CSS/blob/master/images/Image_13.jpg?raw=true" /></a></p>

57. We can add style to individual HTML element tags using `style` attributes.

58. The syntax for style attributes is `style="STYLE_PROPERTY:PROPERTY_VALUE;"`

59. For example, if we wanted text characters in the `H1` tag to be blue and center aligned:
```HTML
 <h1 style="color:blue; text-align:center;">Hello World!</h1>
```

60. And if we wanted text in the `p` tag to have a light blue background and a different font:
```HTML
 <p style="background-color:powderblue; font-family:courier;">This is my first HTML page.</p>
```

61. All style elements are enclosed in quotation marks and include a semicolon after each element.

62. To put that all together:

```HTML
<body>
 <h1 style="color:blue; text-align:center;">Hello World!</h1>
 <p style="background-color:powderblue; font-family:courier;">This is my first HTML page.</p>
</body>
```

<p align="center"><a href="https://github.com/jmtemple/HTML-CSS/blob/master/images/Image_14.png?raw=true"><img class="aligncenter" src="https://github.com/jmtemple/HTML-CSS/blob/master/images/Image_14.png?raw=true" /></a></p>

63. We can see how the style attributes are changing how the web page content displays:
- The `<h1>` heading has has a blue text color and is center-aligned
- The `<p>` content has a powder blue background color and Courier font

64. For more on HTML styles:
- HTML Styles: https://www.w3schools.com/html/html_styles.asp
- HTML Colors: https://www.w3schools.com/html/html_colors.asp

<blockquote>Q7: Take a look at the HTML Colors page listed above. Do you see anything familiar?</blockquote>

<blockquote>Q8: If you haven't already, experiment with modifying your existing HTML pages to include some of these style elements.</blockquote>

# Using Cascading Style Sheets (CSS)

65. You can customize HTML using style attributes, but imagine you want all instances of the `<h1>` or `<p>` tag in your website to have the same formatting.

66. Doing this with `style` would require adding code every time you use these elements.

67. Cascading Style Sheets (CSS) provides a more elegant way to add these style attributes across the pages in our site. 
- For more on CSS: https://www.w3schools.com/css/css_intro.asp

68. For those familiar with website-building tools like WordPress, Weebly, or Wix, CSS is a main part of how different site "themes" are managed. 

69. Let’s create a simple external CSS for our site. 

70. The CSS is cascading because there is a hierarchy to the way that styles are applied. 

71. If styles are defined within the document (as in the previous example), then they are applied before those in the stylesheet. This lets us override the stylsheet if there is particular content that we would like to style differently.

## Creating and Implementing CSS

72. Open the already-existing `style.css` file from the htmltemplate.zip download.

73. The CSS file doesn’t contain any content, it only defines the styles for the various elements in HTML files. 

<p align="center"><a href="https://github.com/jmtemple/HTML-CSS/blob/master/images/Image_15.png?raw=true"><img class="aligncenter" src="https://github.com/jmtemple/HTML-CSS/blob/master/images/Image_15.png?raw=true" /></a></p>

74. Let's get started by adding a few styles for the background, `<h1>`, and `<p>`. 

75. Each tag is defined first `<body>`, `<h1>`, and `<p>` in this example. These are referred to as the selectors. 

76. Our style instructions for each tag are enclosed in `{ }`. These are called declarations. 

77. We can add as many style declarations as we would like in between the brackets, separating each with a semicolon. Each declaration has a property followed by a colon and then a value. 

78. It is common practice to place each declaration on a new line and to indent the declarations, but this is only to make the file easier for us to read and edit. The spacing has no impact on how the computer reads and interprets the code.

79. Putting that all together:

```CSS
body {
 background-color: lightblue;
 }
 
h1 {
 color: white;
 text-align: center;
}

p {
 font-family: courier;
 font-size: 20px;
}
```

80. Now we need to link the CSS to any HTML file where we want the style sheet to apply. This connection is called a reference. 

81. Each HTML page must reference the CSS to apply it to the page. 

82. We create this reference in the `<head>` of the HTML document with the other metadata. 

83. In the `<head>` of `index.html` add the reference `<link rel="stylesheet" type="text/css" href="mystyle.css">`.

```HTML
<head>
 <title>Page Title</title>
 <link rel="stylesheet" type="text/css" href="style.css">
```

84. This line can appear anywhere between the `<head>` and `</head>`. 
- The `<link>` tag is another way to create links to other documents. 
- In this case the `rel` attribute defines the relationship between the HTML file and the linking document. 
- The `type` defines the type and `href` contains the URL or location reference for the file.

85. To learn more about the `<link rel>` tag: http://www.w3schools.com/tags/att_link_rel.asp

THIS FIG STAYS
<p align="center"><a href="https://github.com/jmtemple/HTML-CSS/blob/master/images/Image_17.jpg?raw=true"><img class="aligncenter" src="https://github.com/jmtemple/HTML-CSS/blob/master/images/Image_17.jpg?raw=true" /></a></p>

86. Open the `index.html` file in your browser to see the updated CSS.

87. However, if you click on the link to `page2.html`, it will look the same as it did before. This is because we need to link the stylesheet to each of the pages. 

88. Add the same `<link rel="stylesheet" type="text/css" href="mystyle.css">` to `page2.html`. 

89. Now both pages should share the same style.

<blockquote>Q9: If you haven't already, experiment with creating a CSS and linking it to your HTML pages.</blockquote>

# Creating a Website

90. Now, it’s time to build your own website. The lab procedure has covered the tools you can use to get started, but you can also expand on what you've learned using the W3Schools HTML and CSS resources and documentation (be sure to cite resources you consult or reference- a list of URLs is fine). The files, HTML, and CSS you have created while working through the lab procedure can be the starting point for this website.

91. For now, your site needs to fit a few minimum requirements.
  
92. First, the theme. Choose at least three media items—these can be books, articles, podcasts, films, songs, etc. Ideally, these three (or more) items will have something in common, but that connection is up to you.

93. Next, you are going to build a website about these items. 

94. You need to meet the following requirements:
- You need a landing page (index.html) that describes the items and provides a brief introduction to your site. For example, if you are presenting books from your favorite author you could provide a brief into to the author here. It doesn’t need to be extensive, but you want to include some content. Your landing page should also include some logo or image.
- The landing page (index.html) must also link to three different pages, one for each of the items you have chosen. 
- Each of the item pages must include:
  * A short description of the item. You may pull this description from another source (publisher, archives, Wikipedia), just be sure to cite the source and link back to it if it is online.
  * A link to some related source on the web (Wikipedia, a book review or museum exhibit, for example) If you’ve pulled your description from another source, then the link to this source can serve as the link.
  * A representative image.
- The site also needs to include at least one table built in HTML (could be on any page)
- You also need a CSS for your site. The CSS will be used across all four pages of content to standardize the look and feel of your site.

95. That’s it. You are free to be as creative as you’d like as long as you meet these requirements.

96. I encourage you to use the W3Schools pages as a guide for HTML (http://www.w3schools.com/html/) and CSS (http://www.w3schools.com/css/default.asp) as you design your site. 

97. You’ll find tutorials for menus, tables, and other elements to jazz up your site. Feel free to borrow code and CSS from anywhere on the web. Have fun and experiment!

98. Submit the HTML files and relevant CSS as as `.zip` folder on Canvas, along with your answers to lab notebook questions.

<blockquote>Q9: Have you ever created a website before? Have you used a program like WordPress, Wix, SquareSpace, or Weebly? How is this process different? Reflect on the process of creating a website by working directly with the HTML.</blockquote>

<blockquote>Q10: Submit the HTML files and relevant CSS as as zip folder on Canvas.</blockquote>

# Endnotes

<sup id="fn1">1. “What is HTML?” http://www.yourhtmlsource.com/starthere/whatishtml.html.<a href="#ref11" title="Jump back to footnote 1 in the text.">↩</a></sup>

# Lab Questions

[Link to lab notebook template](https://docs.google.com/document/d/1r92sHMZ5Ok137qbfPkK1Z9-zedyIeaXn6z1hniHCnOc/copy) (ND users, Google Doc).

All of the required questions are listed here. Be sure to answer each question completely, including an explanation of how you arrived at your answer. Also submit the HTML files and relevant CSS as a `.zip` folder on Canvas.

Q1: Try to interpret a few of these errors in your own words. HINT: The W3Schools resources listed under step 15 provide more information or explanation on some of these errors.

Q2: Between the head tags, there are also a few meta tags. Use the W3C site to translate this information in your notebook. Some resources that can help you get started:
- [W3Schools, "HTML Meta Tag"](https://www.w3schools.com/tags/tag_meta.asp)
- [W3Schools, "HTML Meta Charset Attribute"](https://www.w3schools.com/tags/att_meta_charset.asp)
- [W3Schools, "Responsive Web Design With Viewport"](https://www.w3schools.com/css/css_rwd_viewport.asp)

Q3: If you haven't already, modify index.html to include a link to a second HTML file. Next, add an image to index.html.

Q4: Move the image you added in Q4 into a new "Images" folder. What happens when you save and run the code? What would you need to modify in the HTML to correctly display this image?

Q5: Add a table to one of your HTML pages (index.html or page2.html). You could create fictional data or add meaningful data from another source. What challenges did you face getting the table to display and function like you expected?

Q6: Take a look at the HTML Colors page listed above. Do you see anything familiar?

Q7: If you haven't already, experiment with modifying your existing HTML pages to include some of these style elements.

Q8: If you haven't already, experiment with creating a CSS and linking it to your HTML pages.

Q9: Have you ever created a website before? Have you used a program like WordPress, Weebly, SquareSpace, or Wix? How is this process different? Reflect on the process of creating a website by working directly with the HTML.

Q10: Submit the HTML files and relevant CSS as as zip folder on Canvas.
