# INDEX.HTML EXPLANATION

**HTML Structure:**

* `<!DOCTYPE html> ... </html>`: Defines the document as an HTML document.
* `<html lang="en"> ... </html>`: The root element of the HTML document, specifying the language as English.
* `<head> ... </head>`: The header section containing meta information about the document.
  * `<meta charset="UTF-8">`: Defines the character encoding as UTF-8 for proper display of characters.
  * `<meta name="viewport" content="width=device-width, initial-scale=1.0">`: Sets the viewport meta tag to ensure the page responds properly to different screen sizes.
  * `<title>Weather App</title>`: Sets the title of the webpage to "Weather App".
  * `<link rel="stylesheet" href="./style.css">`: Links an external stylesheet named "style.css" for styling the application's appearance.
* `<body> ... </body>`: The main content section of the webpage.
  * `<div class="card"> ... </div>`: A main container element with the class "card" likely representing the overall weather information card.
    * `<div class="search"> ... </div>`: A section for search functionality with the class "search".
      * `<input type="text" placeholder="Enter City Name Here" spellcheck="false">`: An input field for the user to enter the city name. It has a placeholder text and spellcheck is disabled.
      * `<button><img src="./images/search.png" alt="image-1"></button>`: A button to trigger the search for weather data. It contains an image likely representing a search icon.
    * `<div class="error"> ... </div>`: A section for displaying error messages with the class "error". It contains a paragraph element with the error message "Invalid City Name". This section is initially hidden (see styles).
    * `<div class="weather"> ... </div>`: A section for displaying weather information with the class "weather". This section is initially hidden (see styles).
      * `<img src="./images/rain.png" class="weather-icon" alt="image-2">`: An image element for the weather icon. It has an initial image likely representing rain and an alt text for accessibility.
      * `<h1 class="temp">22°C</h1>`: A heading element with the class "temp" displaying the temperature (initially set to 22°C).
      * `<h2 class="city">New York</h2>`: A heading element with the class "city" displaying the city name (initially set to New York). This is likely a placeholder value.
      * `<div class="details"> ... </div>`: A container element with the class "details" for displaying humidity and wind information.
        * `<div class="col"> ... </div>` (repeated twice): A column element with the class "col" used twice for humidity and wind details.
          * `<img src="./images/humidity.png" alt="image-3">`: An image element for the humidity icon.
          * `<div> ... </div>`: A container for humidity details.
            * `<p class="humidity">50%</p>`: A paragraph element with the class "humidity" displaying the humidity percentage (initially set to 50%).
            * `<p>Humidity</p>`: A paragraph element displaying the label "Humidity".
          * Similar structure for wind details using different image and labels.

**JavaScript Functionality:**

* `const apiKey ="3aa08224e6382d45e37a335d83919309";`: Stores your OpenWeatherMap API key in a constant variable named `apiKey`. Replace this with your own API key for the application to work.
* `const apiUrl ="https://api.openweathermap.org/data/2.5/weather?lat={lat}&lon={lon}&units=metric&q=";`: Defines the base URL for the OpenWeatherMap API with placeholders for latitude (`{lat}`), longitude (`{lon}`), and city name (`q`). The units are set to metric.
* `const searchBox = document.querySelector(".search input");`: Uses `document.querySelector` to select the input element within the search section and stores it in the `searchBox` constant.
* `const searchBtn = document.querySelector(".search button");`: Similar to above, selects the search button element and stores it in `searchBtn`.
* `const weatherIcon = document.querySelector
