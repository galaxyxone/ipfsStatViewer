Start with a simple react web app/plugin that a user can install within their browser

  then stat pulling data from users ipfs node via http api requests
  
  then display users ipfs data on grafana or something similar-
  
## Building an extension from scratch

To start- adapt a grafana API to display a bar graph displaying what types of data are stored on a users node by using the file_type and file_size as the sources of data

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
