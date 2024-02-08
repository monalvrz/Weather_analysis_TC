# Technical Challenge

🌧️ ## Weather analysis

The technical challenge consisted of working with a dataset containing flight-related information and obtaining the weather of the origin and destination cities of each flight.

🔧 ## Resources 
- Data Source: challenge_dataset.csv
- Software: Python 3.12.1, Jupyter Notebook, Pandas

🔀 ## Process 
The following steps were taken in order to carry out the technical challenge:

1. Create a repository in Github. 
2. Install the necessary programs (such as Python and Jupyter) to be able to run the code locally.
3. Import the dataset with the initial information. Review, analyze and clean it.
   - Duplicate flights were removed.
   - Columns containing unneeded information were removed.
   - Columns were reorganized and renamed.
4.  Obtain the combination of unique flights, i.e., unique origins and destinations, along with the latitudes and longitudes of each. 
5.  Iterate through the combination of unique flights to get each IATA code of the flight locations along with their latitudes and longitudes.
6.  Create a list to store each combination of coordinates.
7. Build the URL to connect to OpenWeather in order to make the request
   - First it was necessary to create an API account
   - Obtain an API key
   - Create a config.py file and save the password there for compliance
   - Create a .gitignore file so that the file would not be added to the repository
8. Build the code to make the API request.
   - Create an empty list to store the information.
   - Loop through all the coordinates
   - Create an endpoint URL with latitude and longitude for the weather data
   - Execute a request to the weather data API for each set of coordinates
   - Extract the required weather data
   - Get the city name by reverse geocoding with the same coordinates
   - Add a 1 second pause between requests so as not to exceed the request rate
   - Add an except in case an error occurs
9. Clean and organize the columns of the DataFrame with the information obtained of the request.
10. Create a function to match the information retrieved from the request with the IATA extracted from the flight origins and destinations using the exact coordinates.
11. Add the information of the request to the original dataset of the flights by making a join from the IATA codes of the origins and destinations.
12. Clean, sort and rename the columns of the resulting DataFrame.
13. Save the information in a CSV file.

💪🏼 ## Challenges and obstacles 
