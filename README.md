# Technical Challenge

## Weather analysis 🌧️

The technical challenge consisted of working with a dataset containing flight-related information and obtaining the weather of the origin and destination cities of each flight.

## Resources 🔧
- Data Source: challenge_dataset.csv
- Software: Python 3.12.1, Jupyter Notebook, Pandas

## Process 🔀
The following steps were taken in order to carry out the technical challenge:

1. Create a repository in Github. 
2. Install the necessary programs (such as Python and Jupyter) to be able to run the code locally.
3. Import the dataset with the initial information. Review, analyze and clean it.
   - Duplicate flight numbers were removed.
   - Columns containing unneeded information were removed.
   - Columns were reorganized and renamed.
4.  Obtain the combination of unique flights, i.e., unique origins and destinations, along with the latitudes and longitudes of each. 
5.  Iterate through the combination of unique flights to get each IATA code of the flight locations along with their latitudes and longitudes.
6.  Create a list to store each combination of coordinates.
7. Build the URL to connect to OpenWeather in order to make the request
   - Create an OpenWeather account
   - Generate an API key
   - Create a config.py file and save the password for compliance in an environment variable
   - Create a .gitignore file so that the file would not be added to the repository
8. Build the code to make the API request.
   - Enable the cache to avoid duplicate consults
   - Create an empty list to store the information
   - Loop through all the coordinates
   - Create an endpoint URL with latitude and longitude for the weather data
   - Execute a request to the weather data API for each set of coordinates
   - Extract the required weather data
   - Get the city name by reverse geocoding with the same coordinates
   - Add a 1 second pause between requests so as not to exceed the request rate
   - Add an except function in case an error occurs
10. Clean and sort the columns of the DataFrame with the information obtained of the request.
11. Create a function to match the information retrieved from the request with the IATA extracted from the flight origins and destinations using the exact coordinates.
12. Add the information of the request to the original dataset of the flights by making a join on the IATA codes of the origins and destinations.
13. Clean, sort and rename the columns of the resulting DataFrame.
14. Save the information in a CSV file.

## Challenges and obstacles 💪🏼

As with every new challenge, the process presents certain difficulties that allow us to find creative and diverse ways to find solutions.

One of the main challenges wascreacquainting myself with Github and what it implies; creating a repository, cloning it to a local file, committing and pushing from the terminal without breaking anything. To solve the problems that arose from this I read the official Github documentation and looked up the bugs I was getting on Stack Overflow. 

Another challenge I faced in this test was to find the best way to work with the dataset to collect the data I needed to retreive information from OpenWeather. I tried several ways to do it and when I thought it was already solved I was able to identify certain errors that gave me clues on how to do it in a cleaner and more accurate way. 

Initially I tried to make the API request using the closest cities to the coordinates of the dataset, however it was not giving me the exact location of the IATA codes. Therefore, I had to find a way to make the request using the coordinates and not the cities. To learn how to make the request it was necessary to read the OpenWeather documentation.

Additionally, for Python syntax questions I used ChatGPT and Stack Overflow to answer questions about bugs. 

> [!TIP]
> One of my biggest learnings throughtout my journey in the world of programming is to accept that we don't have to know everything. Instead we need to have a clear goal and develop the ability to ask questions and find the answer that best suits us on the internet. We have to learn when to search for answers in the documentation, or in pages like Stack overflow, or if we require the assistance of a person. Generating knowledge is not a one-way street.







