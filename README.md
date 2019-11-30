## CS3012 Software Engineering Assignment 5: **Social Graph Project**  

Written by  
Can ZHOU (19324118)  
If there has any confusion, Please email me: zhouc@tcd.ie

## Click Here For **[Live Demo](https://can-zhou.github.io/CS3012/index.html)**

### Zoomable Sunburst: [Quick Link](!https://can-zhou.github.io/CS3012/Zoomable_Sunburst.html)
- The D3 sub-repos which star number is in the top five in total.
- Showing the latest 3 people who fork, submit issue, star to those repos (2019-11-29).
    - The innermost layer is D3.
    - The second layer shows the names of these five repos.
    - The third layer is the classification of Fork, Issue, and Stargazers.
    - The fourth level shows the name of the person who performed these actions.
- It has zoomable function as well:
    - Click on arc in order to zoom in.
    - Click on the center circle to zoom out.
    - Avoid clicking text when clicking.

### Radial Tidy Tree: [Quick Link](!https://can-zhou.github.io/CS3012/Radial_Tidy_Tree.html)
- The first ten repos of D3 are shown.
- It displays the latest issue information of each repo.
- For each issue, it describes:
   - The issue number.
   - Whether issue is locked?
   - Issue current state.
   - Who submitted it.

### Pie and Donut Charts -- Overview: [Quick Link](!https://can-zhou.github.io/CS3012/Pie_Chart_Sum.html)
-  The charts show the information of D3 sub-repos which have the top five star number.
- This is a flowing chart.  
  With this order:
    - Fork Count pie chart.
    - Disk Usage pie chart.
    - Start Count pie chart.
    - Fork Count donut chart.
    - Disk Usage donut chart.
    - Start Count donut chart.
- Charts have those functions as well:
    - Mouse over the sector / arc to focus on specific data.
    - Mouse over the label below each chart to focus on specific data.
    - Click on the label below each chart to hide specific data.

### Pie and Donut Charts -- Start Count: [Quick Link](!https://can-zhou.github.io/CS3012/Pie_Chart_Star_Count.html)
- Pie and donut charts show the total stars number of D3 sub-repos which have the top five star number.
- Charts have those functions as well:
    - Mouse over the sector / arc to focus on specific data.
    - Mouse over the label below each chart to focus on specific data.
    - Click on the label below each chart to hide specific data.

### Pie and Donut Charts -- Fork Count: [Quick Link](!https://can-zhou.github.io/CS3012/Pie_Chart_Fork_Count.html)
- Pie and donut charts show the total fork count of D3 sub-repos which have the top five star number.
- Charts have those functions as well:
    - Mouse over the sector / arc to focus on specific data.
    - Mouse over the label below each chart to focus on specific data.
    - Click on the label below each chart to hide specific data.

### Pie and Donut Charts -- Disk Usage: [Quick Link](!https://can-zhou.github.io/CS3012/Pie_Chart_Disk_Usage.html)
- Pie and donut charts show the total disk usage of D3 sub-repos which have the top five star number.
- Charts have those functions as well:
    - Mouse over the sector / arc to focus on specific data.
    - Mouse over the label below each chart to focus on specific data.
    - Click on the label below each chart to hide specific data.


## Part One - GitHub Access
### Get data from GitHub 
- I use Github GraphQL API with Node.js.
- Using node-fetch to make HTTP requests with Node.js.

## Part Two - Social Graph
### Analyse data  
- This part is to analyze raw JOSN file and change the format of JSON file which is more suitable for data visualization.
- About output file:
  - The output file is the JSON file.
  - I **intentionally** changed the output file from a JSON file to a JavaScript file.
  - Because the JavaScript cannot directly read the JSON file at the front end, it needs to interact with the backend.
  - I want to avoid interaction with the backend (avoiding operations like using AJAX)
  - So I output the JavaScript file directly. When we need to call JSON data, we can directly reference the output JavaScript file to gain the JSON data.
- I have analysed three types of data:
    1. Used for pie and donut charts.
    2. Used for radial tidy tree.
    3. Used for zoomable sunburst.

### Data visualisation [A live demo is in showcase part]
- I have visualized three types of data:
    1. pie and Donut charts.
    2. Radial tidy tree.
    3. Zoomable sunburst.
- Using D3.js and C3.js [A JavaScript library dependent on D3]

### Showcase
- A websit for live demo.
- Click here for **[Live Demo](https://can-zhou.github.io/CS3012/index.html)**

## Run the code
### Run the code in Get_data_from_GitHub
- Please make sure you have installed the Node.js.  
      If not, please download and install the Node.js: [Download Node.js](https://nodejs.org/en/)
- Get your personal access token from GitHub: [Instruction](https://help.github.com/en/github/authenticating-to-github/creating-a-personal-access-token-for-the-command-line)   
- Replace the `accessToken_has_been_deleted` in
      **app.js--line #4** (`const accessToken = 'accessToken_has_been_deleted';`)   
      with your personal GitHub access token.
- Open the terminal where the downloaded file is located.
- In terminal, type: `node app.js`
- The data will be stored in three JSON files.

### Run the code in Analyse_data 
- Please make sure you have installed the Node.js.  
  If not, please download and install the Node.js: [Download Node.js](https://nodejs.org/en/)
- Go to each floder.
- Open the terminal where the downloaded file is located.
- In terminal, type: `node app.js`
- The data will be analysed and stored in three JavaScript files.

### Run the code in Data_visualisation
- Download and click the HTML file.

### Run the code in Showcase
- Click here for **[Live Demo](https://can-zhou.github.io/CS3012/index.html)**