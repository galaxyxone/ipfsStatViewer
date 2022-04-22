Start with a simple react web app/plugin that a user can install within their browser

  then stat pulling data from users ipfs node via http api requests
  
  then display users ipfs data on grafana or something similar-
  
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

-------------------------------------------------------------------------------------------------------------------------------------------------------


What is the best way to extract the file extensions of the data stored in a users IPFS node? 

![Screen Shot 2022-04-22 at 1 21 42 AM](https://user-images.githubusercontent.com/30084404/164615565-8a90ebc7-e5c7-4466-baf6-807a29c1a8f9.png)
![Screen Shot 2022-04-22 at 1 21 53 AM](https://user-images.githubusercontent.com/30084404/164615568-ef1bc88a-afab-4a46-a85b-67f2e07d0003.png)


