# Statistical Data Viewer
### This is SEMI working right now- this is a prototype repo
### _A simple chrome extension for users to visualize the data stored on their local IPFS node_
### Only the REACT and d3.js work so far, next is building it into chrome extension


[![made-with-javascript](https://img.shields.io/badge/Made%20with-JavaScript-1f425f.svg)](https://www.javascript.com)
[![](https://img.shields.io/badge/project-IPFS-blue.svg?style=flat-square)](https://ipfs.io/)

<img src="{https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB}" />

IPFS Statistical Data Viewer is a Chrome Extension that visualizes your IPFS Node with D3.js using the file_type and file_size as the sources of data to create a treemap

### Its not the most effecient program but were working to make it better! (submit issue report)

# Install Extension

- Download the build file and load it as unpacked in Chrome with your IPFS Daemon running


Note: You need to make sure you have cross origin requests allowed. You can use the following ipfs cli-commands to enable cross origin access. 


```sh
ipfs config --json API.HTTPHeaders.Access-Control-Allow-Origin '["*"]'
ipfs config --json API.HTTPHeaders.Access-Control-Allow-Methods '["GET", "POST"]'
```

## Features
- Static data visualization command to generate a graphic that is displayed to user(extension/react pulls pinlist from user via http ipfs api)
- FUTURE: Zoomable animations using D#
- FUTURE: Canvas visualizations instead of SVG

## Tech


We are building a web-app to save and monitor your data via IPFS. Our program scans your IPFS cache folder to show a detailed summary of what is stored on your IPFS node. The data will be visualized using organized colorful graphics similar to apps like Windirstat, Spacesniffer, or Disk Recon. Each file type (MP3, ZIP, EXE, JPEG, etc.) is assigned a color in a collage of rectangles that are sized depending on how much space that file type is using. 

- [IPFS] - Peer-to-peer hypermedia protocol
- [D3] - A Javascript library for visualizing data using web standards-
- [markdown-it] - Markdown parser done right. Fast and easy to extend.
- [node.js] - evented I/O for the backend
- [Express] - fast node.js network app framework [@tjholowaychuk]

## Future Project Goals

- Goal Treemap with Dynamic Interactivity(zoom into file/parent file boxes to see into child files
![Screen Shot 2022-04-07 at 6 00 34 PM](https://user-images.githubusercontent.com/30084404/162333144-4d65b53f-0df5-49ec-bc11-40ea0bf78bc8.png)



## Installation

Install the dependencies and devDependencies and start the server.

```sh
npm install
```

For production environments...

```sh
Coming soon
```


## License

MIT


[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)

   [ipfs]: <https://github.com/ipfs>
   [d3]: <https://github.com/d3/d3>
   [markdown-it]: <https://github.com/markdown-it/markdown-it>
   [node.js]: <http://nodejs.org>
   [jQuery]: <http://jquery.com>
   [express]: <http://expressjs.com>
   [AngularJS]: <http://angularjs.org>



