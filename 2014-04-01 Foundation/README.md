Experiment: Test whether our fixed-width design can be converted to a responsive design by adding Foundation classes to the layout HTML.

Result: Yes, it can be converted with minimal changes to design.

Caveats:

- Disable `#page-outer { width: 1001px; }` in styles.css, line 121.
- Topic navigation image sprites are not RWD-friendly. Recommend hiding on small screens.
- Flatten nested divs, e.g. `<div id="main" class="main-content main-leftcol-outer main-leftcol-outer-alt` to simplify responsive layout. Results in loss of top borders.
- Can't replicate precise layout dimensions using 24-column grid system. E.g. 207px wide menu becomes 208.5417 (5/24).

Steps:

1. Copy the Pure CSS proof of concept /2014-03-14 Pure CSS/Article.html.
2. Copy styles-minus-layout from /2014-03-14 Pure CSS/.
3. Download the Foundation 5.2.1 from the website.
3. Add Foundation includes to Article.html.
4. Add `row` and `large-* columns` to layout-related `<div>` tags.
5. Make sure to include our CSS include after the Foundation includes so they don't overwrite the mStoner styles.
6. NULL-out those aspects of the CSS related to layout so they don't override Foundation's definitions.

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