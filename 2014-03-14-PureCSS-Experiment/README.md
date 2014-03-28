Experiment: Test whether our mStoner design can be converted to a responsive design by adding Pure CSS classes to the layout HTML.

Result: Yes, it can be converted with minimal changes to design.

Caveats:

- Disable `#page-outer { width: 1001px; }` in styles.css, line 121.
- Topic navigation image sprites are not RWD-friendly. Recommend hiding on small screens.
- Flatten nested divs, e.g. `<div id="main" class="main-content main-leftcol-outer main-leftcol-outer-alt` to simplify responsive layout. Results in loss of top borders.
- Can't replicate precise layout dimensions using 24-column grid system. E.g. 207px wide menu becomes 208.5417 (5/24).

Procedure:

1. Download http://www.union.edu/news/stories/2014/03/success-scholars-to-focus-on-stem.php.
2. Download http://www.union.edu/_css/styles.css and replace relative with absolute links.
3. Add `<link href="http://yui.yahooapis.com/pure/0.4.2/grids-min.css" rel="stylesheet" />`.
4. Add `pure-g-r` and `pure-u-*-*` to layout-related `<div>` tags.
5. Make sure to include the styles.css after the Pure file so the Pure styles don't overwrite the mStoner styles.
6. NULL-out those aspects of the CSS related to layout so they don't override the Pure definitions.

March 17, 2014
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