There are several options to build AR experiences with [A-Frame](https://aframe.io/docs/1.0.0/introduction/) today. This guide is a living community effort. If you find inaccurate or out-of-date information you're more than welcome to suggest changes.

# WebXR

Browsers are shipping [experimental AR extensions](https://immersive-web.github.io/webxr-ar-module/) of the [WebXR specification](https://immersive-web.github.io/webxr/). You can start using them today keeping in mind that these features are still under discussion and evolving rapidly. You will be using cutting-edge technology and your feedback will help shape the API that will eventually become part of the standard.

- List of APIs with capabilities and limitations: There are a number of "incubating" features that are not approved by working group as standards yet. [Here is a list of many of them.](https://immersive-web.github.io/#feature-incubations)
- Browser, device compatibility and necessary flags: [Available Chrome 78 behind a flag](https://www.chromestatus.com/feature/5450241148977152), [Instructions for Enabling Experimental AR Support](https://immersiveweb.dev/chrome-support.html#experimental-ar-flags)
- Link to quick start examples: [Chromium WebXR Test](https://storage.googleapis.com/chromium-webxr-test/r740830/proposals/phone-ar.html), [WebXR AR Proposal Samples](https://immersive-web.github.io/webxr-samples/proposals/), [Model Viewer AR Mode](https://modelviewer.dev/examples/augmented-reality.html)

Pros:
- Potential for very high performance AR tracking by leveraging native device AR capabilities
- No cost or licensing fees

Cons:
- Experimental, not part of a ratified standard and inconsistent browser and device support
- Very limited device support (specific Android phones)
- Limited library support (no simple A-Frame examples yet for commonly used AR features)

# ar.js

[ar.js](https://github.com/jeromeetienne/AR.js/blob/master/README.md) is based on a JavaScript implementation of [ARToolKit](https://github.com/artoolkitx/jsartoolkit5) providing marker and images based tracking using the smartphone's built-in camera.

- Link to quick start example: [Follow these 2 steps to try it out now](https://github.com/jeromeetienne/AR.js/blob/master/README.md#try-it-on-mobile)

Pros:
- Supported on most devices with a browser with WebRTC support (to enable camera access from JavaScript). This represents a large range of consumer devices available today such as mainstream Apple iOS and Android devices.
- No cost or licensing fees
- Good library support with many [A-Frame components and examples](https://github.com/jeromeetienne/AR.js/tree/master/aframe#aframe-ar)

Cons:
- Requires use of [2D markers](https://github.com/jeromeetienne/AR.js/#what-marker-based-means)
- Limited performance relying on JavaScript port of ARToolKit

# 8th Wall

[8th Wall](https://www.8thwall.com/) uses a home-grown JavaScript [SLAM](https://en.wikipedia.org/wiki/Simultaneous_localization_and_mapping) solution compatible with any smartphone camera. It provides 6DoF positional tracking, surface and light estimation, world points, hit tests and image based tracking.

- Link to quick start example: [Extensive list of A-Frame demos with source code](https://github.com/8thwall/web/tree/master/examples/aframe)

Pros:
- Supported on most devices with a browser with WebRTC support (to enable camera access from JavaScript). This represents a large range of consumer devices available today such as mainstream Apple iOS and Android devices.
- High quality tracking and performance via proprietary SLAM algorithm
- Best mix of performance and breadth of device compatibility on the market as of early 2020
- Robust library integration, including this [extensive list of A-Frame demos with source code](https://github.com/8thwall/web/tree/master/examples/aframe)

Cons:
- Commercial product with license fees scaling on usage
