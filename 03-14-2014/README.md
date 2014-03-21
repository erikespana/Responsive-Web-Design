A test to see whether our mStoner design can be converted to a responsive design by adding Pure CSS classes to the layout HTML.

1. Start with the current template.
2. Replace the layout-related <div> tags with Pure CSS classes.
3. Create a copy of styles.css
4. Only include the Grids component of the Pure CSS framework.
5. NULL-out those aspects of the CSS related to layout so they don't override the Pure definitions.
6. Make sure to include the styles.css after the Pure file so the Pure styles don't overwrite the mStoner styles.

March 17, 2014
* Compare to:
	http://www.union.edu/news/stories/2014/03/success-scholars-to-focus-on-stem.php
* Consolidated:
`	<div id="main">
		<div class="main-content">
			<div class="main-leftcol-outer main-leftcol-outer-alt">
				...
			</div>
		</div>
	</div>`

Into:
`	<div id="main" class="pure-g main-content main-leftcol-outer main-leftcol-outer-alt">
		...
	</div>`
 Resulted in the loss of aspects of the top border. 

* Transformed
`	<div class="main-leftcol">
	</div>
	<div class="main-maincol">
	</div>`
	
Into:
`	<div class="pure-u-5-24">
	</div>
	<div class="pure-u-19-24">
	</div>`