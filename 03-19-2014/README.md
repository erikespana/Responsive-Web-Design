Experiment: Test whether our mStoner design can be converted to a responsive design by integrating it into Foundation's [Sidebar template](http://foundation.zurb.com/templates/sidebar.html).

Result: Inconclusive. So far it seems this approach would require recreating styles.css.

Caveats
- Foundation partially supports Internet Explorer 7 and 8.
- Can't replicate precise layout dimensions using 12-column grid system. E.g. 207px wide menu becomes 250px (3/12).

Benefits
- Foundation is set up with a (customizable) maximum width.
- Built-in JavaScript effects, including modal windows, image carousel (orbit), etc.

Procedure

* Downloaded customized Foundation 5.2.1 (checked Grid, Block Grid) http://foundation.zurb.com/develop/download.html#customizeFoundation
* Copied css/foundation.css into experiment folder and edited sidebar.html
* Added the Union logo