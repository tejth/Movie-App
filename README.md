# Movie App 
                    
  

Welcome to the Movie App! This is a simple web application that allows users to search for movies and view their details.

## Table of Contents

- [Features](#features)
- [Technologies Used](#technologies-used)
- [Learnings](#learning)
- [Getting Started](#getting-started)
- [Usage](#usage)
- [Contributing](#contributing)




## Features

- Users can search for movies using the search bar.
- Movie results are displayed with their titles, ratings, and overview.
- Movies are color-coded based on their ratings.

## Technologies Used

- HTML5
- CSS3
- JavaScript (ES6+)
- The Movie Database (TMDb) API for movie data

## Learning

1. Learned how to use translate and transform properties to show details of movie when user hovers over it.
2. Learned how to use "TMDB" API and fetch data using JS and display it on the frontend.

```javascript
      const API_URL =
        "https://api.themoviedb.org/3/discover/movie?sort_by=popularity.desc&api_key=ed7756aa2650fb383eb9f4724bb243d9&page=1";
      const IMG_PATH = "https://image.tmdb.org/t/p/w1280";
      const SEARCH_API =
        'https://api.themoviedb.org/3/search/movie?api_key=ed7756aa2650fb383eb9f4724bb243d9&query="';
      
      const main = document.getElementById("main");
      const form = document.getElementById("form");
      const search = document.getElementById("search");
      
      // Get initial movies
      getMovies(API_URL);
      
      async function getMovies(url) {
        const res = await fetch(url);
        const data = await res.json();
      
        showMovies(data.results);
      }
```
## Getting Started

To run this project locally, follow these steps:

1. Clone this repository to your local machine.
2. Open the `index.html` file in your web browser.

Alternatively, you can use a local development server to serve the files.

## Usage

1. Upon loading the page, you will see a search bar at the top.
2. Enter a movie title or keyword in the search bar and press Enter or click the Search button.
3. The page will display movies matching your search query.
4. Hover over a movie to see its overview.
5. Clicking on a movie will show more details.

## Example

![Movie App Screenshot](https://github.com/tejth/Movie-App/assets/110801292/a2887e8d-6791-4925-ad63-fc6efabd645a)


## Contributing

Contributions to this project are welcome! Here's how you can contribute:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature/new-feature`).
3. Make your changes.
4. Commit your changes (`git commit -am 'Add new feature'`).
5. Push to the branch (`git push origin feature/new-feature`).
6. Create a new Pull Request.


## APILinks

[Authentication Documentation](https://developer.themoviedb.org/docs/authentication-application)

[API Settings](https://www.themoviedb.org/settings/api)
