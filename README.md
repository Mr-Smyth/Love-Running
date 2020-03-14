# Love-Running

Love Running - A Responsive Website built only using CSS and HTML

1.	###Setup new Project repo and file structure on Git or Repl. Also setup on local VSC.

2.	Setup the Boilerplate:
	a.	Enter the title for the page.
	b.	Link to style sheet.
	c.	Setup the placeholders: Header, sections and footer with descriptive text.
	d.	Also set padding, margin etc to 0.

3.	###Setup the header element:
	a.	The header will consist of a logo on the left that, when clicked, will always take the user back to the home page. Wrap this in: <a> tag.
	b.	On the right we have navigation links that the user can use to explore the site. The links will always be arranged in information priority from left to right. Beginning with a separate homepage link, followed by gallery, contacts us etc. Use <nav>.

4.	###Google fonts.
	a.	Get import links for the fonts you want to use, and paste them to the top of your style sheet. (Oswald and Lato used for Love Running). Remember – Keep general style rules to the top, and get more specific as you move down.

5.	###Setup some styling for header area.
	a.	Set the fonts for the body. (#777777 is a good colour for content).
	b.	Set fonts and styling for the h and block elements as these do not automatically inherit from the body. (#555555 is good for headings.) 
	c.	Set the letter spacing for the logo (4px).
	d.	Set specific styling to the logo in h2, this should not be done in h2, as we can reuse h2 styling in rest of site. To do this we will target it with an id#
	e.	Float the logo id to left side.

6.	###Setup the list menu items.
	a.	Setup a #menu id to target the <ul> element for style, spacing etc.
	b.	If we need to reverse order the menu items we float the ul to the right, then float the li to the left.
	c.	Target the li items directly with #menu li id.
	d.	Float the li items to the right/left as required (see point b above).

7.	###Tidy Header area:
	a.	Target the menu items again with a different style. (we can target the <li> items by targeting the child of the menu id we already created. As the menu id is associated to the ul, we may target the li, by going... #menu a{} i.e the child of menu!).
	b.	We want to remove the line underneath the links (text decoration:none)
	c.	We want to inherit the colour from the provider, in this case the body.
	d.	Set a matching line-height for both the menu and the logo components. (              #logo, #menu{}) . 
	e.	By default text will automatically align itself within its line height.

8.	###Set Hero image to be contained away from header, and animate it.
	a.	Set styling to the section containing the div, to the same dimensions as the image. (#hero-outer). We will use overflow:hidden as an alternative to clear:both. The reason we will use overflow hidden is that clear:both would allow image bleed into header as the size increases by 10%.
	b.	Animate the image to zoom in by 10% (or from 1 to 1.1). Use the @keyframes rule followed by an animation name of own choosing. Set a from and to state for the animation:



			@keyframes hero-image{
			from{
			transform: scale(1);
			}
			to{
			transform: scale(1.1);
			}
			}
	c.	Add this animation rule to the class that loads the image:
		animation-name: hero-image;
		animation-duration: 5s;
		animation-fill-mode: forwards;

9.	###Setup the Cover text box, that gives a brief description. In Love running it is on the hero image.
	a.	Setup another div, with h2 and h3 for text.
	b.	Target the div with an id
	c.	Target specify the h2 with a desired font color, otherwise they will inherit default or previously set colors.
		#cover-text, #cover-text h2{
	d.	Create another style rule for the styling of the cover text box.
	e.	In Love Running i set opacity and absolute positioning, check out that for example code.

10.	###Setup page ethos or about section, the section below hero image:
	a.	We will follow Love running example here again.
	b.	Give the section the id club ethos
	c.	Create a h1 text.
	d.	Create 3 divs, 1 for left text, 1 for right text and 1 for the central image.
	e.	Give each div an id and some placeholder text.
	f.	Inkeeping with design layout, give section same dimensions as hero image.
	g.	Then style each div. In a 3 column layout like this, float left and right first then set the centre div margin to ‘0 auto’
	h.	Color these blocks so we can easily visualise them.

11.	###Add and style the content to the page ethos. 
	a.	 Left div – add heading and paragraph.
	b.	Right div – add heading and content.
	c.	We target these headings with a class, as we will be reusing it (left-about-heading & right-about-heading)
	d.	Add a hr under sub headings.
	e.	Find a better way to do the classes in this section ie combine.

12.	###Make the centre circle for containing the image:
	a.	Insert a div and style it to be a circle, rem the trick margin 0 auto to centre the circle.

13.	 ###Insert the image into the container circle:
	a.	Insert a nested div into the above container div.
	b.	Add the background image, remember to give it a height.

14.	###Insert icons beside each content block – Font Awesome.
	a.	With font awesome you link to a css stylesheet, similar to the style sheet we link to for the css. Make sure to paste in the link to font awesome before the css style link, so it will have been read into memory first.
	b.	Find the icon you want and click start using to get the link box.
	c.	Paste the link beside the text where you want it to appear.

15.	###Start to build next section, in this case meeting times.
	a.	Remove placeholder text and for love running we create 5 divs with 5 h3’s for the content, each of the 5 divs will be inline block across the screen, with a background image.
	b.	Target the parent section of the meeting times content, and give it an id of times.
	c.	Insert a background into this id in css, give it appropriate styling (see code)
	d.	Target the child of #times, to style the content.

16.	###Add social media links to the footer.
	a.	Add a ul to the footer with 4 li.
	b.	Each li will be an a link to the social media site, also inbetween the a link paste a link to a font awesome icon.
	c.	Target the ul with a class social-networks
	d.	Set a height of 150px for the footer – inkeeping with style
	e.	Set the class social networks to be aligned centre
	f.	Target the li within social networks and display inline.
	g.	Drill down to the icons: ‘.social-networks i’ and set the font size, margin, padding and color.

17.	###Setup a Gallery page:
	a.	Always keep header and footer elements constant across pages.
	b.	Create a new project file called gallery.html, at the same folder level as index.html.
	c.	Copy the contents of index into gallery, and remove the sections we do not need.
	d.	Change links and titles to suit.

18.	###Adding content to Gallery:
	a.	We will use the masonary design for the page – fixed width, no fixed height.
	b.	Create a section for the pictures, add the images directly to that section.
	c.	Clear both
	d.	Set columns, line height and column gap as required.
	e.	Photo image set to 100%.

19.	###Making site responsive to tablet or phone – Media Queries.
	a.	To achieve this we will use a CSS construct called a media query. Media queries contain styles that are only called when certain criteria are met, such as a specified screen width being reached. 
	b.	@media screen and (max width 1393px)  Why this value for a break-point? Well its the point at which our desktop site becomes distorted. Because there are so many devices available now we cannot work towards a particular screen size, instead we aim to maintain the integrity of the screen layout as you reduce the size, through multiple break-points.
	c.	Header section can be often ok at this break point, so we will concentrate on the other body elements.
	d.	Re target the css elements within the media query to reassign their values. Clear out margins reduce sizes etc. See love running code for example.
	e.	Why use float left so much???

20.	###Next media query breakpoint (943px):
	a.	First target the menu, clear left and float left, margin 30px and margin bottom 20px
	b.	Cover text, align it left 0px.
	c.	Make the club ethos 90% width.
	d.	Set left and right about headings to inherit the width (that will be from club-ethos).
	e.	Align both headings and paragraphs in center.

21.	###Resize meeting times section:
	a.	Made the boxes 100% wide and clear both to have them stacked.
	b.	Added border style and removed padding.

22.	Add Gallery Page
	a. add gallery.html

