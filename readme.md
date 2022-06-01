# Statistical Data Viewer 

### _A simple chrome extension for users to visualize the data stored on their local IPFS node_

[![made-with-javascript](https://img.shields.io/badge/Made%20with-JavaScript-1f425f.svg)](https://www.javascript.com)
[![](https://img.shields.io/badge/project-IPFS-blue.svg?style=flat-square)](https://ipfs.io/)

[Download in the Google Chrome Store](https://chrome.google.com/webstore/detail/ipfs-stat-viewer/leoogniilogpecgamlbafoajfcaoddja)



## IPFS Statistical Data Viewer is a Chrome Extension that visualizes your IPFS Node with D3.js using the file_type and file_size as the sources of data to create a treemap


# Install Extension


- Download the build file and load it as unpacked in Chrome Extension Manager
- Open extension with your IPFS Daemon running

Important Note: You need to make sure you have cross origin requests allowed. You can use the following ipfs cli-commands to enable cross origin access. 


```sh
ipfs config --json API.HTTPHeaders.Access-Control-Allow-Origin '["*"]'
ipfs config --json API.HTTPHeaders.Access-Control-Allow-Methods '["GET", "POST"]'
```
As as you have IPFS running, it should work without issue-

<img width="1239" alt="Screen Shot 2022-05-03 at 6 00 04 PM" src="https://user-images.githubusercontent.com/30084404/166586795-3a046027-4c1f-4029-880a-116fb5101f11.png">

- You should see something that looks like this depending on what you have pinned in IPFS

## Features
- Static data visualization command to generate a graphic that is displayed to user(extension/react pulls pinlist from user via http ipfs api)

## Tech


We are building a web-app to save and monitor your data via IPFS. Our program scans your IPFS cache folder to show a detailed summary of what is stored on your IPFS node. The data will be visualized using organized colorful graphics similar to apps like Windirstat, Spacesniffer, or Disk Recon. Each file type (MP3, ZIP, EXE, JPEG, etc.) is assigned a color in a collage of rectangles that are sized depending on how much space that file type is using. 

- [IPFS] - Peer-to-peer hypermedia protocol
- [D3] - A Javascript library for visualizing data using web standards-
- [markdown-it] - Markdown parser done right. Fast and easy to extend.
- [node.js] - evented I/O for the backend
- [Express] - fast node.js network app framework [@tjholowaychuk]

## Future 

- FUTURE: Zoomable animations using D#
- FUTURE: Canvas visualizations instead of SVG


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



