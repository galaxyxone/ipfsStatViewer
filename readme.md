# ipfsStatViewer(Statistical Viewer)

### _A simple chrome extension for users to visualize the data stored on their local IPFS node_

[![made-with-javascript](https://img.shields.io/badge/Made%20with-JavaScript-1f425f.svg)](https://www.javascript.com)
[![](https://img.shields.io/badge/project-IPFS-blue.svg?style=flat-square)](https://ipfs.io/)
[![Chrome Web Store](https://img.shields.io/chrome-web-store/v/leoogniilogpecgamlbafoajfcaoddja.svg)](https://chrome.google.com/webstore/detail/ipfs-stat-viewer/leoogniilogpecgamlbafoajfcaoddja)


## IPFS Statistical Data Viewer is a Chrome Extension that visualizes your IPFS Node with D3.js using the file_type and file_size as the sources of data to create a treemap


# Install Extension

[Download in the Google Chrome Store](https://chrome.google.com/webstore/detail/ipfs-stat-viewer/leoogniilogpecgamlbafoajfcaoddja)

(ignore) Add updated information about Brave Browser Integration

Important Note: You need to make sure you have cross origin requests allowed. You can use the following ipfs cli-commands to enable cross origin access. 

If 
If you want to install from source via this repo, do the following-

- Download the build file and load it as unpacked in Chrome Extension Manager
- Open extension with your IPFS Daemon running



```sh
ipfs config --json API.HTTPHeaders.Access-Control-Allow-Origin '["*"]'
ipfs config --json API.HTTPHeaders.Access-Control-Allow-Methods '["GET", "POST"]'
```
As as you have IPFS running, it should work without issue-

<img width="1239" alt="Screen Shot 2022-05-03 at 6 00 04 PM" src="https://user-images.githubusercontent.com/30084404/166586795-3a046027-4c1f-4029-880a-116fb5101f11.png">

- You should see something that looks like this depending on what you have pinned in IPFS

## Features
- Colors of boxes in treemap correlate to a file type- supporting music, photos, video, and more. 
- Box size correlates to amount of data in the file 


### In specific cases, this command is needed to get the treemap to function correctly- 

```
ipfs config --json API.HTTPHeaders.Access-Control-Allow-Origin '["http://webui.ipfs.io.ipns.localhost:48084", "http://localhost:3000", "http://127.0.0.1:5001", "https://webui.ipfs.io", "chrome-extension://leoogniilogpecgamlbafoajfcaoddja"]'
```

## Working on currently 
## Tech

 A users IPFS data is visualized using organized colorful graphics similar to apps like Windirstat, or Disk Recon. Each file type (MP3, ZIP, EXE, JPEG, etc.) is assigned a color in a collage of rectangles that are sized depending on how much space that file type is using. Treemap function provided by D3.js.  
 
 

- [IPFS] - Peer-to-peer hypermedia protocol
- [D3] - A Javascript library for visualizing data using web standards-
- [markdown-it] - Markdown parser done right. Fast and easy to extend.
- [node.js] - evented I/O for the backend
- [Express] - fast node.js network app framework [@tjholowaychuk]

## Future 

- FUTURE: Add more visualizations (pie chart and more)
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

