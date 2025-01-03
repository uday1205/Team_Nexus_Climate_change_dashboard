**PROJECT : CLIMATE CHANGE DASHBOARD**

**TEAM NEXUS**

 **Team Members : HARSH SINGH, 
                  SHARMA UDAY, 
                  VIHIR SHAH, 
                  PRAJAPATI YASH, 
                  JEET PATEL**

             
The objective of a Climate Change Dashboard is to provide a centralized platform that enables users to monitor,
analyze, and visualize key climate data and trends. By tracking essential indicators such as temperature changes the dashboard help
users better understand the impacts of climate change. It also allows for the tracking of mitigation and adaptation efforts, 
such as climate resilience projects, ensuring that interventions are on track.
Designed to support informed decision-making, the dashboard offers actionable insights for policymakers, businesses, and the public,
fostering greater awareness, accountability, and collaboration. Ultimately, the dashboard serves as a tool to promote 
data-driven actions that mitigate climate risks and enhance global climate resilience. 

||**Tools and Libraries used :**||

The libraries used in our python scripts 
pyngrok(ngrok)
matplotlib.pyplot
flask(lask, render_template_string, request, jsonify)
pandas
io
base64
numpy
cborne

||**Data Source :**||

https://data.giss.nasa.gov/gistemp/graphs_v4/

kaggle.com

||**Execution Steps**||
1. Clone the Repository
First, clone the repository to your local machine or GitHub
2. Install Required Dependencies
Install the required dependencies using pip. Ensure that you have Flask, pandas, and matplotlib installed. You can do this by running:
3. Prepare the Dataset
Ensure that your dataset (e.g., climate_data.csv) is available and accessible. The dataset should contain columns like:

Country (name of the country),
Year (the year of data),
Temperature columns (e.g., F1960, F1961, etc., which represent temperature change for each year).
Make sure the dataset is in the correct format and placed in the same directory as your Flask app or adjust the file path accordingly in the code
4. Run the Flask Application
5. Access the Application in a Browser
Open your web browser and go to:

||**Result summary**||

The image depicts a section of a climate change dashboard hosted on an interactive web application. At the top, there is a dropdown menu labeled
"Select Year for Top 10 Hottest Countries," with the year 1988 selected. Below the dropdown is a green button labeled "Generate Top 10 Hottest Countries Chart."
The main content of the dashboard is a bar chart titled "Top 10 Hottest Countries in 1988." The chart showcases the temperature changes (in °C) for the top 10
countries that experienced the highest temperatures during that year. Tunisia, Algeria, and Canada are among the top three, with temperature changes exceeding 1.2°C
, while other countries, including Malta, Libya, and Australia, follow closely. The chart uses orange bars to represent the data visually, with the x-axis listing the 
countries and the y-axis showing the temperature change values.

The image shows another section of the Climate Change Dashboard. At the top, it features input options to select a start year, an end year, and a country for analysis. 
The start year is set to 1961, the end year to 2022, and the selected country is Bhutan. A blue button labeled "Generate Temperature Plot" allows users to create a visual
representation of the data. Below these inputs, there is a line graph titled "Temperature Change for Bhutan (1961–2022)." The graph displays annual temperature change trends 
in Bhutan over the selected period. The x-axis represents the years, while the y-axis indicates the temperature changes in degrees Celsius (°C). The line chart, drawn in blue,
shows a general upward trend, signifying an increase in temperature change over time.

||**Challenges faced**||
1. Handling Data Availability Issues
Challenge: The user selects a year range or countries that do not have corresponding data in the dataset, leading to a "No data available" message also due the the spaces in the .csv and .xlsx files.
Solution: Ensured that the dataset is properly loaded, and validate user input. If no data is found for the selected range or countries, display a friendly error message (e.g., "No data available for the selected range and countries"). You can also use try-except blocks to catch these errors
2. AJAX Request Failures
Challenge: AJAX requests might fail due to incorrect data being sent or errors in the backend route. This can lead to the browser not displaying the plot or receiving an error message.
Solution: Ensure that the frontend correctly sends the required data (start year, end year, countries) via the AJAX request. On the backend, handle the data correctly and return a well-formed response. Use error handling in the backend to catch any unexpected issues.
3. Incorrect Plot Generation
Challenge: The plot might not be generated correctly or might not show up at all.
Solution: Check the backend code to ensure that the matplotlib plot is being created and saved correctly in memory. Make sure the data passed to matplotlib is in the expected format (e.g., numerical data for temperature changes). Also, ensure that the plot is being returned as a base64-encoded image so it can be displayed on the frontend.
4. Multiple Year Ranges and Countries
Challenge: If the user selects multiple countries or a range of years, the code needs to handle these dynamic inputs properly, which might introduce complexity.
Solution: On the frontend, allow multiple countries to be selected and pass them as an array to the backend. On the backend, handle the array of countries and process data accordingly.
5. Plot Styling and Aesthetics
Challenge: The plots may not be styled or formatted properly.
Solution: You can improve the styling of the plots using matplotlib's built-in features. Customize the colors, labels, and axes to make the plots more readable and visually appealing.
