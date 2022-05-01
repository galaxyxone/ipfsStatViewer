# This repo is a collection of various notes and information dedicated to the development of the IPFS-Stat-Viewer project.
## Start with a simple React Chrome Extension that a user can install within their browser that monitors a users local IPFS Node.

--------------------------------------------------------------------------------------------------------------------------------------------------------
### Things being built right now 

- A transformation function to map data to D3's Treemap graph API.

- A pluggable declarative TreeMapGroup component for React, which utilizes D3 for the graph. (File size correlated to box size) (Color corresponds with name of file) (.png is color x, .pdf is color y)
  
- Plug everything into React-Chrome Extension- Cross your fingers it all works together once its built!
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

-------------------------------------------------------------------------------------------------------------------------------------------------------


What is the best way to extract the file extensions of the data stored in a users IPFS node? 

![Screen Shot 2022-04-22 at 1 21 42 AM](https://user-images.githubusercontent.com/30084404/164615565-8a90ebc7-e5c7-4466-baf6-807a29c1a8f9.png)
![Screen Shot 2022-04-22 at 1 21 53 AM](https://user-images.githubusercontent.com/30084404/164615568-ef1bc88a-afab-4a46-a85b-67f2e07d0003.png)

### Date: April 23rd 2022 5:27am

So after wrapping up the React and D3- querrying the IPFS network is resulting in a "size" of zero, which d3 intreprets as nothing(no box) so tomorrow when you wake up, its your job to figure out what a query is returning that! Hopefully its not that complicated!

- All updates are added 

### Date: April 24th 2022 4:38pm

https://discuss.ipfs.io/t/solved-file-size-comparison-for-file-synchronization/4767 

- This discussion shows a working file size 
- Add the new findings- ipfs files stat /nameoffile
   
   command: "ipfs files stat /chortle.jpeg"
   
   
   
### Message to Discord about file-size return as a zero

 Hey @lidel#4314 and @Elpranocotro#4529 so I have a different question about the returned file size from the files LS API. The returned string does not have a listed file size. Is it normal for the response to have a zero file size? After some digging I found that in cmd, if you use "ipfs files stat /filename" it returns a Size and CumulativeSize value for the CID's you specify.

Would it be sufficient to say that I would need to use a separate command/shell to get the file size returned or could I just have something wrong in my apps code? 

--------------------------------------------------------------------------------------------------------------------------------------------------------
## Sprint Done! 

1. So the API should be working but for some reason its not- make sure to write a issue about it- 
2. Add sprint into Chrome extension now- 

### react_d3_treemap_v2.zip
- For now I just solved the problem using a utility fetch handler-
- Few updates to js and react
- Fixed IPFS response
# Functioning React App

I have three files saved in my IPFS Repo
<img width="1235" alt="Screen Shot 2022-05-01 at 12 12 31 AM" src="https://user-images.githubusercontent.com/30084404/166133229-07430341-4d4a-4ec0-bbf5-b5c9af22c3e0.png">

Changes ASAP:

1. Build into Chrome-Extension now
2. List file_size of zero in a sub-menu maybe for informations sake
3. Re-Factor EVERYTHING
4. Index of what colors are what files- 
5. Readouts of Sizes of Data-
6. More information- more granularity



