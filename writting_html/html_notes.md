# HTML
Full form is HyperText Markup Language. Basic structure of an HTML page looks like this:
```bash
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="utf-8" />
        <title>Web Page Structure</title>
    </head>
    <body></body>
</html>
```
Writting HTML, is typically marking up or writting content inside a series of tags or elements. Tags are defined by the "<" and ">" around the tag name. Majority of 
elements in HTML have an openning and closing tag, a closing tag has "/" after its "<" sign and before the elements name. A few elements, like **meta** in  head are
called as **void** elements as they don't wrap around anything, and hence are self closing -notice the closing forward slash at the end with no element name. 

## basic elements:

### The doctype:
First of all, we opened our document with the HTML5 Doc-type declaration: 
```bash
<!DOCTYPE html>
```
We can write ```<!doctype html>``` also.

### html tag and lang attribute:
After doctype declaration, we open the html tag, the first, and therefore root tag for our document. We use lang attribute to specify the language for the document, and then we open the head section:
```bash
<html lang="en"
    <head>
```

### chracter encoding:
We specify character encoding which tell the browser how to parse tbe information contained within.
```bash
<meta charset="utf-8" />
```

### anchor tag:
All hail the mighty <a> element The a tag (short for anchor tag) is arguably the most important and def i ning tag of HTML. The anchor tag is the tag used to link from the document 
a user is on to another document elsewhere on the internet, or another point in the same document.
A welcome benefit of HTML5 is that we can wrap multiple elements in an a tag. 
```bash
<a href="index.html">  
    <h2>The home page</h2>  
    <p>This paragraph also links to the home page</p>  
    <img src="home-image.png" alt="A rendering of the home page" />
</a>
```
The only limitations to keep in mind with <a> tags are that, understandably, you can’t wrap one <a> tag within another <a> tag or other interactive element (such as a <button>) and you can’t wrap a form in an a tag either.

### Semantic elements:
Semantic is the process of giving our markup meaning. This has 3 types:

1. sectioning elements:
For the broadest strokes in an html page. These are the kind of elements to use for header, footer, and sidebar areas.

2. Grouping elements:
Which are used to wrap associated elements. Think of paragraphs, blockquotes, and content of that nature.

3. Text-level semantics:
Which are the elements we use to designate particular, like a section of bold or italic text or code.

* various **sectioning** elements:
#### '<main>' element:
content area of a document includes content that is unique to that document and excludes content that is repeated across a set of documents such as site navigation 
links, copyright information, site logos and banners, and search forms (unless the document or application’s main function is that of a search form).

It’s also worth noting that there shouldn’t be more than one main on each page (after all, you can’t have two main pieces of content) and it shouldn’t be used as a 
descendent child element of some of the other semantic HTML5 elements, such as article, aside, header, footer, or nav.

#### '<section>' element:
section element is used to define a generic section of a document or application. For example, you may choose to create sections around your content; one section for 
contact information, another section for news feeds, and so on. It’s important to understand that this element isn’t intended for styling purposes; if you need to 
wrap an element merely to style it, you should continue to use a div as you would have before.
    When working on web-based applications, I tend to use section as the wrapping element for visual components. It provides a simple way to see the beginning and end of components in the markup.
    You can also qualify for yourself whether you should be using a section element based on whether the content you are sectioning has a natural heading within it 
(for example, an h1-h6). If it doesn’t, it’s likely you’d be better off opting for div.

#### '<nav>' element:
The nav element is used to wrap major navigational links to other pages or parts within the same page. As it is for use in major navigational blocks, it isn’t strictly
intended for use in footers (al-though it can be) and the like, where groups of links to other pages are common. If you usually mark up your navigational elements with
an unordered list (ul) and a bunch of list tags (li), you may be better served with a nav and a number of nested a tags instead.

#### '<article>' element:
The article element is used to wrap a self-contained piece of content. A content which makes complete sense independently that is a self-contained content.

#### '<aside>' element:
The aside element is used for content that is tangentially related to the content around it. In practical terms, I often use it for sidebars, or content in a little tip
about a related subject in a blog post. It’s also considered suitable for pull quotes, advertising, and groups of navigation elements. Basically, anything not directly
related to the main content would work well in an aside.
    If it was an e-commerce site, I’d consider areas like Customers who bought this alsobought as prime candidates for an aside.

#### '<footer>' element:
it should be used to contain information about the section it sits within. It might contain links to other documents or copyright information, for example. 
    Like the header, it can be used multiple times within a page if needed. For example,it could be used for the footer of a blog but also a footer within a blog post 
article on that same blog. However, the specification notes that contact informationfor the author of a blog post should instead be wrapped by an address element.

#### html5 outline algorithm:
However, HTML5 introduced the ability for each sectioning container to have its own self-con-tained outline. That means it is not necessary to think about which level 
of heading tag you’re at in terms of the entire document. You could just concentrate on the sectioning container you were currently working in. To illustrate why this 
might be preferable, within a blog, post titles could be set to use h1 tags, while the title of the blog itself could also have an h1 tag. For example, consider the 
following structure:
```bash
<h1>Ben's site</h1> 
<section>  
    <h1>Ben's blog</h1>  
    <p>All about what I do</p> 
</section> 
<article>  
    <header>  
        <h1>A post about something</h1> 
        <p>Trust me this is a great read</p>  
        <p>No, not really</p>  
        <p>See. Told you.</p>  
    </header> 
</article>
```
As such, theoretically, you shouldn’t need to keep track of the heading tag you needto use in terms of the whole document. It should be possible to use whatever 
appropriate level of heading tag is needed within each piece of sectioned content and the HTML5 outline algorithm will order it accordingly.
   However, the reality is that search engines and the like make no use of the HTML5outliner at present. Therefore, from a pragmatic viewpoint, it probably makes more 
   sense to continue thinking about headings in terms of the whole document. That will make your documents easier to read for search engines and also aid assistive 
   technology to infer the correct meaning. 

#### h1-h6 and '<hgroup>' element:
```bash
<h1>Scones:</h1> 
<h2>The most resplendent of snacks</h2>
```
Above practice is discouraged.Instead, try and reserve h1-h6 elements for when sections of content require a distinct heading. Like the following:
```bash
<hgroup>  
    <h1>Scones:</h1>  
    <p>The most resplendent of snacks</p> 
</hgroup>
```
You should use an hgroup element with a h1-h6 tag inside, along with any number of ptags before or after.

* **Grouping** element, these are the elements that are used to contain groups of other elements.

#### '<div>' element:
The most ubiquitous grouping element is the div. The div is so widely used because it is opin-ion-less. It conveys nothing. The only implied meaning of a div is that 
it groups something. Despite that, you will often see a div wrapping nothing but a 
string of text.
    You should only opt for a div as a last resort. It is the element to use when you can think of nothing better.

#### '<p>' element:
The p element is used to mark up a paragraph. However, don’t think that means it canonly be used on text 3-4 lines long. On the contrary, use it to mark up any text 
that cannot be better marked up with one of the other elements. For non-specific text, the <p> element is definitely a better choice than a <div>.

#### '<blockquote>' element:
A blockquote is used to mark up text that is quoted from somewhere else. You don’t have to wrap the text inside with any other element, but you can.

#### '<figure>' and '<figcaption>' element:
**<figure>** element can be used to annotate illustrations, diagram, photos, code listing, etc. 
    So, we use it as an element to call out visuals of any sort and the accompanying figcaption provides the means to add some text supporting the visuals. Now, it is 
worth pointing out here that while we should always provide text in the alt attribute of an img tag to support assistive technology or to mitigate problems if an image
fails to load, it isn’t a requirement to provide a figcaption with a figure. The figcaption is added if you want to add a visual description along-side the visuals.
```bash
<figure class="MoneyShot">  
    <img  
        class="MoneyShotImg"  
        src="img/scones.jpg"  
        alt="Incredible scones baked to perfection and ready to eat"  
    />  
    <figcaption class="ImageCaption">  
        This image isn't of scones I have made, instead it's a stock photo  from Wikipedia  
    </figcaption> 
</figure>
```
we can see that the figure element is used to wrap this little self-contained block. Inside, the figcaption is used to provide a caption for the parent figure element. 
It’s perfect when images or code need a little caption alongside (that wouldn’t be suitable in the main text of the content).

#### '<details>' and '<summary>' elements:
```bash
<details>  
    <summary>I ate 15 scones in one day</summary>  
    <p>  Of course I didn't. It would probably kill me if I did. What a way  to go. Mmmmmm, scones!
 </p> 
</details>
 ```

#### '<address>' element:
The address element is to be used explicitly for marking up contact information for its nearest article or body ancestor. To confuse matters, keep in mind that it isn’t
to be used for postal addresses and the like (unless they are indeed the contact addresses for the content in question).
Instead, postal addresses and other arbitrary contact information should be wrapped in good ol’ p tags.

* **HTML text-level semantics**, These are the elements used to mark up individual words, letters, and symbols to provide explicit meaning as to the intent. It was used to be denoted as inline blocks before html5.

#### '<span>' element:
A span element is the text-level equivalent of a div. It is unopinionated and is the perfect element to reach for when you merely want to wrap text in an element for styling purposes.

#### '<b>' element:
The b element represents a span of text to which attention is being drawn for utilitarian purposes without conveying any extra importance and with no implication of an 
alternate voice or mood, such as key words in a document abstract, product names in a review, actionable words in interactive text-driven software, or an article lede.

#### '<strong>' element:
If you do want to emphasize something for strength, urgency, or importance, strong is the element for you. Here is how the specification defines these use cases:
Importance: The strong element can be used in a heading, caption, or paragraph to distinguish the part that really matters from other parts that might be more detailed,
more jovial, or merely boilerplate. Seriousness: The strong element can be used to mark up a warning or caution notice.
Urgency: The strong element can be used to denote content that the user needs to see sooner than other parts of the document.

#### '<em>' element:
The em element represents stress emphasis of its contents. 

#### '<i>' element:
A span of text in an alternate voice or mood, or otherwise offset from the normal prose in a manner indicating a different quality of text.

### '<video>' & '<audio>':
```bash
<video  src="myVideo.mp4"  width="640"  height="480"  controls  autoplay  muted  preload="auto"  loop  poster="myVideoPoster.png" >  
If you're reading this either the video didn't load or your browser is  waaaayyyyyy old!
</video>
```
audio is kind of same excluding width, heigjy and poster attributes.

above code is not responsive and we apply css to it to make it eesponsive.
```bash
video 
{  
    max-width: 100%;
    height: auto;
}

this css will make responsive if only video hpsyed lpcally, but if want to embed video from yputub or other hosting dite than it will be  not responsive. 
And **<ifrme>** is used for embedding the video. and CSS rule used to make that responsive loke this
```bash
<style>  
    .embed-container {  
         position: relative;
         padding-bottom: 56.25%;
         height: 0;
         overflow: hidden;
         max-width: 100%;
     }  
     .embed-container iframe,  
     .embed-container object,  
     .embed-container embed {  
         position: absolute;
         top: 0;
         left: 0;
         width: 100%;
         height: 100%;
 } </style> 
 <div class="embed-container">  
    <iframe  
        src="https://www.youtube.com/embed/B1_N28DA3gY"  
        frameborder="0"
        allowfullscreen
    ></iframe>
</div>

### The modern way to embed iframes and keep aspect ratio:
If you only need to support more modern browsers  you can set the aspect ratio of something like an iframe with the aspect-ratio CSS property. For an iframe we want to keep in a 16:9 ratio, such as a YouTube video, we could add a suitable class and do this:
```bash
.iframe-16-9 {  
    aspect-ratio: 16/9;
    max-width: 100%;
}

### 'loading' attribute in image, video and iframe element:
If you fi nd yourself adding a lot of images or iframe elements to your page, consider the loading attribute. Setting this attribute to lazy means the browser will only go and fetch 
the item if the user scrolls it into view. This is really useful for any media you know will certainly not be visible when the page first displays, meaning the cost of loading that 
item is saved until it is actually needed. It’s literally as simple as adding it like this:
```bash
<!--use in image-->
<img src="home-image.png" alt="A rendering of the home page" loading="lazy" />

<!--use in ifrme-->
<iframe  
    loading="lazy"  
    width="560"     
    height="31
    src="https://www.youtube.com/embed/NkfMBI1tVwY"  
    title="YouTube video player"  
    frameborder="0"  
    allow="accelerometer; 
    autoplay; 
    clipboard-write; 
    encrypted-media;
    gyroscope; 
    picture-in-picture"  
    allowfullscreen 
    ></iframe>
```

### '<dialog>' element:

