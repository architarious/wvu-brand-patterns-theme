Diversity
==================

**Theme Name:** Diversity

**Theme Description:** Theme for the WVU Division of Diversity, Equity and Inclusion.

**Developers name(s):** Adam Johnson

**Stash repository URL:** [https://stash.development.wvu.edu/projects/CST/repos/diversity/browse](https://stash.development.wvu.edu/projects/CST/repos/diversity/browse)

**Dependencies necessary to work with this theme:** [Prepros](http://alphapixels.com/prepros/) (Sass & Autoprefixer)

Currently using Prepros v4.2.0.

## How to get started:

1. Donwload [Prepros](http://alphapixels.com/prepros/).
1. [Download the Prepros Chrome Extension](https://chrome.google.com/webstore/detail/bnlfjdjbjiabcgkkjaicjepbhhmeonlm). Then, in Chrome, go to Tools > Extensions then find the Prepros extension in the list. Check "Allow access to file URLs."
1. Open Prepros and drag the project's folder onto the app (alternatively, you can click "Add New Project" in the app).
1. To enable live refresh, click on the cog icon on the bottom right side of the app window and checking the use custom server option. Enter `http://diversity.lvh.wvu.edu:8080/` in the "Server URL" field, or whatever the Primary Domain is that you specified within your local environment. 
  * Note: Don't forget to use `http` before the url.
  * Port `8080` refers to the CleanSlate Designer box. Change this to `8000` if you have the full CleanSlate box.
1. To auto vendor prefix the CSS, in Prepros, click on `styles.scss`. Check the box in the sidebar that says "Auto Prefix CSS".
1. We want Prepros to ignore all `*.js` and `*.md` files (we'll let CleanSlate minify our JS). To do that, open the project in Prepros and click the cog/settings icon. Click "Project Filters" and paste `*.js, *.md` into the box. Now close/quit and reopen Prepros. Hit the refresh icon to see your changes. All Markdown and Javascript files should dissapear from the list.

**Other notes, comments, or reminders:**

This theme uses the `cleanslate-designer` box for a local development environment.

This theme uses the BEM syntax for classes. BEM stands for Block, Element, Modifier. It helps us organize this project more efficiently. Here's an example of the structure:

    .block{}
    .block__element{}
    .block--modifier{}

And for a real world example:

    .site-search{} /* Block */
    .site-search__field{} /* Element */
    .site-search--full{} /* Modifier */

To get up to speed on the BEM syntax, read [MindBEMding - getting your head 'round BEM syntax](http://csswizardry.com/2013/01/mindbemding-getting-your-head-round-bem-syntax/)

All utility/helper classes have a `.u-*` prepended to them to distinguish them from the rest of the pack.

### Updating the Icon Font

This theme uses part of the Icomoon Free icon font from [Icomoon.io](http://icomoon.io/app/#/select). If you need to update it, you can either manually select the font from the Icomoon App, or upload the `selection.json` file to Icomoon. The `selection.json` file is in `public/fonts-icomoon-free`. I've placed the CSS for the Icomoon font in the `scss/vendor` directory—although, you'll notice that the styles come mostly from `styles.css` included within the package.

If you do update the font, be sure to dump the entire unzipped archive into the `public/fonts-icomoon-free` directory so that it's easy to update later.