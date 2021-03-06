I have several goals for this page:
1. Use a homegrown framework that effectively divides the page into rows and columns
2. Use header, section, and article semantic tags. Remember that divs are not required, I can add classes to the semantic tags.
3. In the features section, have responsive article placement:
  -For a very small screen, have a small image next to a label button (polymer maybe?) that rolls out the link. Articles should be stacked.
  -For a medium screen, have a larger image and show the link without requiring a button. Articles still stacked.
  -For a large screen, unstack the articles. Put the images next to each other, with the label and link underneath.
4. Use responsive image sizes and srcset.
5. Divide the css markup into at least 2 (portfolio and responsive)css files.
6. Consider Bootstrap, but probably reject it for now.

Completed 7/17
-The paper-button is kind of neat, but is strictly a proof of concept for this project.  It makes no sense to double the number of requests and amount of data on the smallest screens. I'm ignoring the html validation error about link rel="import" per http://webcomponents.org/articles/introduction-to-html-imports/
Also ignoring the error about interactive content since I have to choose whether to use an anchor or javascript to fake an anchor; I am going with anchor.
Also not exactly sure which polymer components are truly required, so I am leaving everything bower installed for the time being.
-I will watch the bootstrap video carefully and try to understand how it handles responsive layouts, in particular the stacking and reordering that I did here.  I love stealing other people's code, but I have trouble seeing how bootstrap is better or more efficient than the approach I took here.
-I don't really understand what happens with srcset, I imagine I will go to next week's website performance office hours to see if that can help.  I think I have valid code that usually accomplishes nothing, and sometimes results in duplicate requests.
-I am ignoring the html error about article's needing headers, since in reality mine do have "headers" they just move responsively around the screen.

Received code review on 7/22:
-Used Notepad++ Edit-Blank Operations-Trim Trailing Spaces to get rid of the trailing spaces
-Got rid of a couple of extra leading spaces
-Added spaces where needed in css after :
-Renamed primary file to index.html
-Added to github
----------
-Got rid of all the paper-button references and component files - they served no real purpose, it was mostly good to know I could use bower and polymer
-Changed the alink and blink references to anchors rather than divs inside anchors (OK now that paper-buttons are gone)
-Apparently it is OK to go article-div-h3 but not OK to go article-section-h3. Who knew.
-Changed page header to div as well.  Had gone overboard in using section instead of div.
----------
TODO:
-Find appropriate places to use shorthand properties
-Try the picture srcset workaround from http://www.smashingmagazine.com/2013/05/how-to-avoid-duplicate-downloads-in-responsive-images/
-Look closely for weird/wrong spacing
-Get more feedback about using #ID css selectors
-Make sure the component files are gone from github
-Make sure everything now passes html/css tests
-Try to better understand padding vs. margins
-Make sure it still works
