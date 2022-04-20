# This repo is a collection of various notes and information dedicated to the development of IPFS-Stat-Viewer
## Start with a simple React Chrome Extension that a user can install within their browser that monitors a users local IPFS Node.

--------------------------------------------------------------------------------------------------------------------------------------------------------
### Things being built right now 

- A transformation function to map data to D3's Treemap graph API.

- A pluggable declarative TreeMapGroup component for React, which utilizes D3 for the graph. (File size correlated to box size) (Color corresponds with name of file) (.png is color x, .pdf is color y)
  
- Then stat pulling data from users ipfs node via http api requests
  
- Then display users ipfs data on grafana or something similar-

--------------------------------------------------------------------------------------------------------------------------------------------------------
  
## Building an extension from scratch

To start- adapt a visualization API(D3) to display what types of data are stored on a users node by using the file_type and file_size as the sources of data

This first https://www.youtube.com/watch?v=2LhoCfjm8R4

https://thenishchalraj.medium.com/dynamically-embed-grafana-dashboards-in-a-react-component-483b9ecd1dcd



  DATA REQUIRED: FilesList/getTitle
  
  
look at filesList.js


  const getTitle = (filesPathInfo, t) => {
  const parts = []

    if (filesPathInfo) {
      parts.push(filesPathInfo.realPath)
    }


Zoomable Circle Packing- D3 Library

https://observablehq.com/@d3/zoomable-circle-packing

Pie Chart- D3 Library

https://observablehq.com/@d3/pie-chart

Treemap

https://observablehq.com/@d3/treemap

use the same IPFS CORS api that is used on the ipfs-webui
https://github.com/ipfs/ipfs-webui
https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS

Configure IPFS API CORS headers
You must configure your IPFS API at http://127.0.0.1:5001 to allow cross-origin (CORS) requests from your dev server at http://localhost:3000

Similarly if you want to try out pre-release versions at https://dev.webui.ipfs.io you need to add that as an allowed domain too.

-----------------------------------------------------------------------------------------------------------------------------------------------------------

export CIDS to a newline delimited file.
  - use the following command "ipfs pin ls -q > pinlist.txt

Then use D3.js to look at the pinlist and create a map from that-
  - make sure that the filename can come as well maybe? then maybe file size too hopefully
 
 
 To use this chart outside of Observable, go to the @d3/treemap notebook, then copy-paste the entire function Treemap including the copyright notice into your application. You’ll also need to install (e.g., yarn add d3) and import (e.g., import * as d3 from "d3") D3; see D3’s README for details. To render a chart, pass Treemap an array of data and any desired options; it will return an SVG element that you can insert into the DOM.
 
import {Treemap} from "@d3/treemap"

Then call Treemap(data, options) as shown above.

To customize this chart, click the  Fork button at the top of the page to create your own copy of this notebook and save your changes. To run a cell, click the play button  in the top-right corner of the editor, or use Command-S (⌘S) or Shift-Enter (⇧↩).

If you have any questions or suggestions, please sign-in to leave a comment. Click the cell menu  to the left of any cell, then click  Add comment.



-------------------------------------------------------------------------------------------------------------------------------------------------------

