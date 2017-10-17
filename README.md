# Working-with-Youtube-API
This is an experimental project to use youtube video as background element to a webpage
This reademe file is intended as a collection of notes to the obstacles encountered during production.


The project aims to utilize youtube video as a background playback 


- HTML
  
  * note: In general the structure of the page follows a trilogical pattern, where it follows the order of "Header" "Body" "Footer".               However in cases where "Footer" is unnecessary, the "Footer" is reserved
  
  Tags in hierarchical pattern:
  
  <body> ---> <header> | <main> | <footer>
  
    <header> ----> <section.container> ----> <div.link-to-index> | <nav>

    <main> -----> <section.content-header> | <section.content-body> 

      <section.content-header> ----->  /* video banner */  <div.album-box> | <iframe>
      <section.content-body> ----->  /* text & image content */  <article.content-body> | <ul.image-gallery> 
    
    <footer> -----> <section.container> -----> <div.info> | <div.external-links>
    
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
  

- JavaScript

  * note: tbd
  
  











/*	the trick to hide youtube logo is to create a huge iframe box, then offset the position of the 
	video content, while setting the wrapping box's overflow value to hidden */


/* .video-player--banner {
  position: absolute;
  /* (240 - 160) / 2 = 40 */


/*
  top: -40px;
  left: -50%;
  width: 200%;
  height: calc(720px + 40px);
} */


/* however, this approach will create potential layout inconsistency problems or other related issues
   I can't think about atm. Another approach demonstrated in another example is to use css attribute
   pointer-events: none; to disable youtube hover */


/* Unfortunately as great as this method is it creates a few draw backs:
	1, the option to pause the video play by clicking on the video is is disabled as well
	(which now thinking about it I realize I might be able to add it back by creating a transparent
	layer on top of the video as event listener to pause the video, which also means that we probably
	don't need the pointer-events: none)

	2, the youtube logo and the info icon still shows up onload */


/*
@media (min-screen: 1280px) {


};

*/
