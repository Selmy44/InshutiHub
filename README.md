# InshutiHub
InshutiHub is a movie platform for watching online movies
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>InshutiHub</title>
    <style>
        /* Inline CSS for simplicity (not recommended for large projects) */
        body {
            font-family: Arial, sans-serif;
            background-color: powderblue;
            margin: 0;
            padding: 0;
        }

        header {
            background-color: olive;
            color: #fff;
            padding: 10px;
            text-align: center;
        }

        #movie-list {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 20px;
            padding: 20px;
        }

        .movie-card {
            background-color: #fff;
            border: 1px solid #ddd;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
            border-radius: 5px;
            width: 250px;
            padding: 10px;
        }

        .movie-card img {
            max-width: 100%;
            height: auto;
        }

        .movie-title {
            font-weight: bold;
            margin: 10px 0;
        }

        .movie-description {
            margin-bottom: 10px;
        }

        /* Add more CSS styles for responsiveness and interactivity as needed */
    </style>
</head>
<body>
    <header>
        <h1>Welcome to InshutiHub</h1>
    </header>
    <div id="movie-list">
        <!-- Movie cards will be dynamically generated here using JavaScript -->
    </div>

    <script>
        // Sample movie data (you would typically fetch this from a server)
        const movies = [
            {
                title: 'Movie 1',
                description: 'Description of Movie 1',
                imageUrl: 'https://via.placeholder.com/150',
            },
            {
                title: 'Movie 2',
                description: 'Description of Movie 2',
                imageUrl: 'https://via.placeholder.com/150',
            },
            {
                title: 'Movie 3',
                description: 'Description of Movie 3',
                imageUrl: 'https://via.placeholder.com/150',
            },
        ];

        // Function to generate movie cards and append them to the movie list
        function renderMovies() {
            const movieList = document.getElementById('movie-list');
            movieList.innerHTML = '';

            movies.forEach((movie) => {
                const movieCard = document.createElement('div');
                movieCard.classList.add('movie-card');

                const image = document.createElement('img');
                image.src = movie.imageUrl;

                const title = document.createElement('div');
                title.classList.add('movie-title');
                title.textContent = movie.title;

                const description = document.createElement('div');
                description.classList.add('movie-description');
                description.textContent = movie.description;

                movieCard.appendChild(image);
                movieCard.appendChild(title);
                movieCard.appendChild(description);

                movieList.appendChild(movieCard);
            });
        }

        // Initial rendering of movie list
        renderMovies();
    </script>
</body>
</html>
