# Code.js

Adds a link which when clicked, shows a dropdown list of anything you want. Script writes anchor to the DOM for ease of use. Link hover color defined in data-color. ID of codejs is req for color to work. Update your own code.js script to globally update your code list on your sites.

## Usage

On whichever sites you choose, add a link to your code.js file in place of where you want the link to appear:

````
<script type="text/javascript" src="http://mysite.com/code.js" data-color="#ddd" id="codejs"></script>
````

The script tag <b>must</b> have <code>codejs</code> set as the <code>id</code> attribute, and if you want to have a dropdown color, you must set <code>data-color</code> respectively.

The only public function is <code>scriptsDropup.create</code> which takes in three parameters:

<ul>
	<li>String that represents the <code>InnerHTML</code> of link</li>
	<li>Array of arrays[Link innerHTML, href] that represent your links</li>
	<li>String representing CSS color of the dropup hover</li>
</ul>

````
scriptsDropup.create('More Code by @jakiestfu', [
    ['Sparky.js', 'http://sparkyjs.com'],
    ['Slow.js', 'http://lab.jakiestfu.com/slowjs/'],
    ['Blur.js V2', 'http://jakiestfu.com/2012/10/01/blurjs-take-ii/'],
    ['Context.js', 'http://contextjs.com/'],
    ['Blur.js', 'http://blurjs.com/'],
    ['Docs.js', 'http://docsjs.com/'],
    ['Code.js', 'http://lab.jakiestfu.com/code.js']
], document.getElementById('codejs').dataset['color']);
````

Since all of this is contained in one file, any pages that need to include this list should only include the JS file. Then you update your JS file with whatever you see fit.

This was created to allow myself (a developer) an easy way to link to other code I've written, but can be used for many things.

Styling inspired by Twitters Bootstrap