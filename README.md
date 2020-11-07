![alt text](https://github.com/ayaxxchanz/SimpleBloggerTemplate/blob/master/screenshots/v3.jpg)
![alt text](https://github.com/ayaxxchanz/SimpleBloggerTemplate/blob/master/screenshots/v3-2.jpg)

# Simple Blogger Template
A simple template inspired by torrent sites customized from Blogger's default template. Made specifically for 'sharer' or 'uploader'.

## Demo
- V3: https://simplecustomv3.blogspot.com/
- V2: https://simplecustomv2-light.blogspot.com/
- V2: https://simplecustomv2-dark.blogspot.com/
- V1: https://ayaxxchanz-simple-custom.blogspot.com/

## Feature
- Simple and minimalist
- Fast loading
- List many blog post in homepage
- No footer credit

## Cons
- Not SEO ready
- Messy code

## Installation
Blogger > Theme > Restore > Upload .xml file

## Important notes
- Make sure to choose **Theme** > **Choose Mobile Theme** > **Desktop**
- Change date format and number of post in **Layout** > **Blog Posts** > **Edit**
- Change navigation link in **Theme** > **Edit HTML** 
- Change **JST** (Japan Standard Time) in the template to the timezone you use for your blog
- Use **class="btn"** and **id="download"** to display download button.

Example: ```<a class="btn" id="download" href="#">Download</a>```
- The download button on  the homepage will open the link inside a post that has **id="downlaod"** in the same tab. I want to make it open in a new tab, but most browsers will mark it as untrusted event and block it from opening. So the best way if you want to use this is, use a direct download link in the post. This is because even when the link is open in the same tab, it will just automatically download the file instead of redirecting visitor to other page. If you want to remove the download button on the homepage, just remove this in the template:

```<span class='home-dl'><a expr:href='data:post.link ? data:post.link : data:post.url + &quot;#download&quot; '><i class='fas fa-download fa-sm' style='float: right;font-size:16px;'/></a></span>```

```
<b:if cond='data:blog.pageType == &quot;item&quot;'>
  <script>
  $( document ).ready(function() {
      if ( document.location.href.indexOf(&#39;#download&#39;) &gt; -1 ) {
          window.open(document.getElementById(&quot;download&quot;).href, &quot;_self&quot;);
      }else{return false;}
  });
  </script>
</b:if>
```
- When using **vertical table**, insert **data-label="TH-NAME"** in the table data, for responsive view. (Replace **TH-NAME** with your table heading text)
Example:
```
<table>
  <thead><th scope="col">TABLE HEADING</th></thead>
  <tbody>
    <tr>
      <td data-label="TABLE HEADING">Table data</td>
    </tr>
  </tbody>
</table>
```
- You can insert ad at the bottom of each post by replacing the code inside ```<div class='banner-f'>``` and ```<div class='square-f'>``` tag.
- May contain error but will be improved from time to time.
