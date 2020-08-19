# [GLTF Sample Viewer](https://camden-bock.github.io/aframe-geology-sample-viewer/)

This is an embeddable gltf sample viewer using an a-frame scene and a-frame asset management.

Add the following to your ``head``
```html
    <script src="https://aframe.io/releases/1.0.4/aframe.min.js"></script>
    <script src="https://unpkg.com/aframe-orbit-controls@1.2.0/dist/aframe-orbit-controls.min.js"></script>
    <script src="https://unpkg.com/aframe-supercraft-loader@1.1.3/dist/aframe-supercraft-loader.js"></script>
```

If hositng through GitHub Pages add to Body:
```html
    <!-- Geology Sample Viewer AFRAME -->
    <style>
      #geologySampleViewer {
        width:80%;
        height:80%;
      }
    </style>
    <div id="geologySampleViewer">
        <a-scene embedded transparent>
          <a-assets>
             <a-asset-item id="sample" src="assets/samplerock.gltf"></a-asset-item>
           </a-assets>
           <a-entity camera look-controls orbit-controls="target: 0 1.6 0; minDistance: 0.3; maxDistance: 180; initialPosition: 0 1.6 .4; enablePan: false"></a-entity>

           <!-- Using the asset management system.-->
          <a-gltf-model drag-rotate-component src="#sample" position="0 1.6 0"></a-gltf-model>
      </a-scene>
    </div>
    <!-- end AFRAME -->
```

If hosting through other service, add to Body:
```html
    <!-- Geology Sample Viewer AFRAME -->
    <style>
      #geologySampleViewer {
        width:80%;
        height:80%;
      }
    </style>
    <div id="geologySampleViewer">
        <a-scene embedded transparent>
          <a-assets>
             <a-asset-item id="sample" src="https://rawcdn.githack.com/camden-bock/aframe-geology-sample-viewer/476892532fac364cde92d05f2f893859873b46d6/assets/samplerock.gltf"></a-asset-item>

           </a-assets>
           <a-entity camera look-controls orbit-controls="target: 0 1.6 0; minDistance: 0.3; maxDistance: 180; initialPosition: 0 1.6 .4; enablePan: false"></a-entity>

           <!-- Using the asset management system.-->
          <a-gltf-model drag-rotate-component src="#sample" position="0 1.6 0"></a-gltf-model>
      </a-scene>
    </div>
    <!-- end AFRAME -->
```


Compatability is confirmed with D2L Brightspace Course Managment - requires plaintext html editor (no WYSG)

## Getting Started

There are two easy options for obtaining this A-Frame scene. It's then up to you to make it your own!

### <sup>Option 1:</sup> Download the ZIP kit 📦

[<img src="http://i.imgur.com/UVPZoM0.png" width="200">](https://github.com/aframevr/aframe-boilerplate/archive/master.zip)

After you have __[downloaded and extracted this `.zip` file](https://github.com/aframevr/aframe-boilerplate/archive/master.zip)__ containing the contents of this repo, open the resulting directory, and you'll be have your scene ready in these few steps:

    npm install && npm start
    open http://localhost:3000/

<hr>

### <small><sup>Option 2:</sup> Fork this Git repo 🍴🐙

Alternatively, you can __[fork this repo](https://github.com/aframevr/aframe-boilerplate/fork)__ to get started, if you'd like to maintain a Git workflow.

After you have __[forked this repo](https://github.com/aframevr/aframe-boilerplate/fork)__, clone a copy of your fork locally and you'll be have your scene ready in these few steps:

    git clone https://github.com/aframevr/aframe-boilerplate.git
    cd aframe-boilerplate && rm -rf .git && npm install && npm start
    open http://localhost:3000/

> :iphone: **Mobile pro tip:** Upon starting the development server, the URL will be logged to the console. Load that URL from a browser on your mobile device. (If your mobile phone and computer are not on the same LAN, consider using [ngrok](https://ngrok.com/) for local development and testing. [Browsersync](https://www.browsersync.io/) is also worth a gander.)

<hr>

### <small><sup>Option 3:</sup> Fork this CodePen example 🍴💾✒️

Or, you can simply __[fork this CodePen example](http://codepen.io/team/mozvr/pen/BjygdO?editors=100)__ to dive right in. Enjoy!


## Publishing your scene

If you don't already know, GitHub offers free and awesome publishing of static sites through __[GitHub Pages](https://pages.github.com/)__.

To publish your scene to your personal GitHub Pages:

    npm run deploy

And, it'll now be live at __http://`your_username`.github.io/__ :)

<hr>

To know which GitHub repo to deploy to, the `deploy` script first looks at the optional [`repository` key](https://docs.npmjs.com/files/package.json#repository) in the [`package.json` file](package.json) (see [npm docs](https://docs.npmjs.com/files/package.json#repository) for sample usage). If the `repository` key is missing, the script falls back to using the local git repo's remote origin URL (you can run the local command `git remote -v` to see all your remotes; also, you may refer to the [GitHub docs](https://help.github.com/articles/about-remote-repositories/) for more information).

<hr>

## Still need Help?

### Installation

First make sure you have Node installed.

On Mac OS X, it's recommended to use [Homebrew](http://brew.sh/) to install Node + [npm](https://www.npmjs.com):

    brew install node

To install the Node dependencies:

    npm install


### Local Development

To serve the site from a simple Node development server:

    npm start

Then launch the site from your favourite browser:

[__http://localhost:3000/__](http://localhost:3000/)

If you wish to serve the site from a different port:

    PORT=8000 npm start


## License

This program is free software and is distributed under an [MIT License](LICENSE).
