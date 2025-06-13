<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Movie List (Plain JS)</title>
    <link rel="stylesheet" href="style.css"> 
</head>
<body>
    <div class="movie-list-container">
        <h1 class="movie-list-title">MOVIE LIST</h1>

        <div class="categories" id="category-buttons">
        </div>

        <form class="search-bar" id="search-form">
            <input type="text" id="search-input" placeholder="Search for movies...">
        </form>

        <div id="loader" class="loader" style="display: none;"></div>
        <div id="error-message" class="error-message" style="display: none;"></div>
        <div id="movie-grid" class="movie-grid">
        </div>
    </div>

    <script src="script.js"></script>
</body>
</html>
<style>
    body {
    margin: 0;
    font-family: Arial, sans-serif;
    background-color: #1a1a1a;
    color: #e0e0e0;
}

.movie-list-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    background-color: #2c2c2c;
    border-radius: 8px;
    padding: 20px;
    width: 100%;
    max-width: 1200px;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.5);
    margin: 20px auto;
}

h1.movie-list-title {
    text-align: center;
    color: #e0e0e0;
    margin-bottom: 30px;
    font-size: 2.5em;
    letter-spacing: 2px;
    text-shadow: 0 0 5px rgba(0, 255, 0, 0.5);
}

.categories {
    display: flex;
    justify-content: center;
    gap: 15px;
    margin-bottom: 30px;
    flex-wrap: wrap;
}

.category-button {
    background-color: #444;
    color: #e0e0e0;
    border: none;
    padding: 10px 20px;
    border-radius: 20px;
    cursor: pointer;
    font-size: 1em;
    transition: background-color 0.3s ease, transform 0.2s ease;
}

.category-button:hover {
    background-color: #555;
    transform: translateY(-2px);
}

.category-button.active {
    background-color: #008000;
    box-shadow: 0 0 8px rgba(0, 255, 0, 0.7);
}

.search-bar {
    display: flex;
    justify-content: center;
    margin-bottom: 30px;
    width: 100%;
}

.search-bar input {
    width: 80%;
    max-width: 500px;
    padding: 12px 20px;
    border: 1px solid #555;
    border-radius: 25px;
    background-color: #333;
    color: #e0e0e0;
    font-size: 1.1em;
    outline: none;
    transition: border-color 0.3s ease;
}

.search-bar input::placeholder {
    color: #aaa;
}

.search-bar input:focus {
    border-color: #008000;
}

.movie-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
    gap: 25px;
    width: 100%;
    justify-content: center;
}

.movie-card {
    background-color: #3a3a3a;
    border-radius: 8px;
    overflow: hidden;
    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.4);
    transition: transform 0.2s ease, box-shadow 0.2s ease;
    text-align: center;
    display: flex;
    flex-direction: column;
}

.movie-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.6);
}

.movie-card img {
    width: 100%;
    height: 300px;
    object-fit: cover;
    display: block;
}

.movie-card-info {
    padding: 15px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    flex-grow: 1;
}

.movie-card h3 {
    margin: 0 0 10px;
    font-size: 1.2em;
    color: #00e600;
}

.movie-card p {
    margin: 0;
    font-size: 0.9em;
    color: #bbb;
}

.loader {
    border: 8px solid #f3f3f3;
    border-top: 8px solid #008000;
    border-radius: 50%;
    width: 50px;
    height: 50px;
    animation: spin 1s linear infinite;
    margin: 50px auto;
}

@keyframes spin {
    0% { transform: rotate(0deg); }
    100% { transform: rotate(360deg); }
}

.error-message {
    text-align: center;
    color: #ff4d4d;
    font-size: 1.2em;
    margin-top: 30px;
}
</style>
<script>
    const API_KEY = '93c9a6ba'; 
const OMDb_API_URL = 'https://www.omdbapi.com/';

const categoryButtonsContainer = document.getElementById('category-buttons');
const searchForm = document.getElementById('search-form');
const searchInput = document.getElementById('search-input');
const loader = document.getElementById('loader');
const errorMessage = document.getElementById('error-message');
const movieGrid = document.getElementById('movie-grid');

let currentCategory = 'Marvel Movie';

const categories = [
    { name: 'Marvel Movie', query: 'Marvel' },
    { name: 'Funny Movie', query: 'comedy' },
    { name: 'Animation Movie', query: 'animation' },
    { name: 'Web Series Movie', query: 'series' }
];

function showLoader() {
    loader.style.display = 'block';
    errorMessage.style.display = 'none';
    movieGrid.innerHTML = '';
}

function hideLoader() {
    loader.style.display = 'none';
}

function showErrorMessage(message) {
    errorMessage.textContent = message;
    errorMessage.style.display = 'block';
    movieGrid.innerHTML = '';
}

function hideErrorMessage() {
    errorMessage.style.display = 'none';
}

function createMovieCard(movie) {
    const movieCard = document.createElement('div');
    movieCard.classList.add('movie-card');

    const posterSrc = movie.Poster !== 'N/A' ? movie.Poster : 'https://via.placeholder.com/200x300?text=No+Image';

    movieCard.innerHTML = `
        <img src="${posterSrc}" alt="${movie.Title}">
        <div class="movie-card-info">
            <h3>${movie.Title}</h3>
            <p>${movie.Year}</p>
            <p>${movie.Type}</p>
        </div>
    `;
    return movieCard;
}

async function fetchMovies(query, type = '') {
    showLoader();
    hideErrorMessage();
    try {
        const response = await fetch(${OMDb_API_URL}?s=${query}&type=${type}&apikey=${API_KEY});
        if (!response.ok) {
            throw new Error(HTTP error! status: ${response.status});
        }
        const data = await response.json();

        movieGrid.innerHTML = '';

        if (data.Response === 'True' && data.Search) {
            data.Search.forEach(movie => {
                movieGrid.appendChild(createMovieCard(movie));
            });
        } else {
            showErrorMessage(data.Error || "No movies found for this category or search term.");
        }
    } catch (err) {
        console.error("Error fetching movies:", err);
        showErrorMessage("Failed to fetch movies. Please check your internet connection or API key.");
    } finally {
        hideLoader();
    }
}

function renderCategoryButtons() {
    categoryButtonsContainer.innerHTML = '';
    categories.forEach(cat => {
        const button = document.createElement('button');
        button.classList.add('category-button');
        button.textContent = cat.name;
        if (cat.name === currentCategory) {
            button.classList.add('active');
        }
        button.addEventListener('click', () => {
            currentCategory = cat.name;
            searchInput.value = '';
            updateActiveCategoryButton();
            
            let typeParam = '';
            if (cat.name.includes('Series')) {
                typeParam = 'series';
            } else if (cat.name.includes('Movie')) {
                typeParam = 'movie';
            }
            fetchMovies(cat.query, typeParam);
        });
        categoryButtonsContainer.appendChild(button);
    });
}

function updateActiveCategoryButton() {
    document.querySelectorAll('.category-button').forEach(button => {
        if (button.textContent === currentCategory) {
            button.classList.add('active');
        } else {
            button.classList.remove('active');
        }
    });
}

searchForm.addEventListener('submit', (event) => {
    event.preventDefault();
    const searchTerm = searchInput.value.trim();
    if (searchTerm) {
        currentCategory = '';
        updateActiveCategoryButton();
        fetchMovies(searchTerm);
    } else {
        currentCategory = 'Marvel Movie';
        updateActiveCategoryButton();
        const defaultCategory = categories.find(cat => cat.name === currentCategory);
        let typeParam = '';
        if (defaultCategory.name.includes('Series')) {
            typeParam = 'series';
        } else if (defaultCategory.name.includes('Movie')) {
            typeParam = 'movie';
        }
        fetchMovies(defaultCategory.query, typeParam);
    }
});

document.addEventListener('DOMContentLoaded', () => {
    renderCategoryButtons();
    const defaultCategory = categories.find(cat => cat.name === currentCategory);
    let typeParam = '';
    if (defaultCategory.name.includes('Series')) {
        typeParam = 'series';
    } else if (defaultCategory.name.includes('Movie')) {
        typeParam = 'movie';
    }
    fetchMovies(defaultCategory.query, typeParam);
});
</script>


