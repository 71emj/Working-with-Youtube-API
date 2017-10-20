# Working-with-Youtube-API
This is an experimental project using youtube video as background element to a webpage
This reademe file is intended as a collection of notes to the obstacles encountered during production.


The project aims to utilize youtube video as a background playback 


- HTML
  
  * note: In general the structure of the page follows a trilogical pattern, where it follows the order of "Header" "Body" "Footer".               However in cases where "Footer" is unnecessary, the "Footer" is reserved
  
  Tags in hierarchical pattern:
  
    \<body> ---> \<header> | \<main> | \<footer>
  
    \<header> ----> \<section.container> ----> \<div.link-to-index> | \<nav>

    \<main> -----> \<section.content-header> | \<section.content-body>
      
      <section.content-header> ----->  /* video banner */  <div.album-box> | <iframe>
      <section.content-body> ----->  /* text & image content */  <article.content-body> | <ul.image-gallery> 
    
    \<footer> -----> \<section.container> -----> \<div.info> | \<div.external-links>
    
      <div.info> -----> <a.link-to-index(in this project, only to the top)> | <p.copyright-info>
      <div.external-links> -----> <div.link-group-one> | <div.link-group-two>....
      
      
   * note: The general pattern still needs a lot of tweeking (still pretty messy when it comes to higher branches), 
           will have to draw out a clearer pattern for future implementation.
           
    
- CSS
  
  * note: The structure and the selector naming still suffers a great deal of chaos, will have to look into different techniques
          to create a more organize pattern (perhaps it's time to learn SCSS).
    
  tricks in handling youtube iframe:
  
  iframe {
    The technique I use to create a clean youtube player window is using a smaller box to crop, thus concealing the (ugly)
    youtube logo. However this technique creates a huge mess in layout, resulting in a endless train wreck of media queries.
  }
  
  * note-for-future-reference: originally the image gallery is designed to be able to enlarge with a single page isolation effect 	     (balck, translucent background with image full size in the center of the page and scrollable), however as it turned out the             structure of the html and associated style rule makes it an incrediblly complex operation thus causing me to forfeit the attempt.

- JavaScript

  * note: there are two js file links to the page. As part of another project the webpage inherit the script that is used to define 	     common visual effect share across all pages of the project. The main 


























  



