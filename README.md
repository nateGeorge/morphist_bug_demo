# morphist_bug_demo
Demo for Morphist bug.

I found that when using Morphist with the ['Creative' bootstrap theme](https://startbootstrap.com/template-overviews/creative/), there is a weird bug that makes the header image/div jump up a bit when the text fades out.  It seems this happens if the `<h1>` tag is instead a `<p>` tag, and with outher transitions than fadeOutRight.  I used [Node.js http-server](https://www.npmjs.com/package/http-server) (`npm install http-server -g`, then `cd startbootstrap-creative-gh-pages` then `http-server`) to serve it (but first noticed the bug in a Flask app I'm prototyping).

I noticed the jump becomes much smaller when adding `display:inline-block;` to the style of the `<ul>` block, but it's still there.  Then, when I added `<br />` elements before and after the `<ul>` block, the jump was gone.
