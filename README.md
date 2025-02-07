# projects
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Instagram App</title>
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css">
    <style>
        body {
            background-color: #f0f0f0;
            font-family: Arial, sans-serif;
        }
        .post-image {
            width: 100%;
            height: 300px;
            object-fit: cover;
            border-radius: 10px;
        }
        .post-caption {
            padding: 10px;
            font-size: 14px;
            color: #333;
        }
        .modal-content {
            background-color: #fff;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
        }
        .home-container {
            text-align: center;
            padding: 100px;
        }
        .home-header {
            font-size: 36px;
            font-weight: bold;
            margin-bottom: 20px;
        }
        .home-intro {
            font-size: 18px;
            color: #666;
            margin-bottom: 30px;
        }
        .nav-link {
            color: #333;
        }
        .nav-link:hover {
            color: #007bff;
        }
    </style>
</head>
<body>
    <nav class="navbar navbar-expand-lg navbar-light bg-light">
        <div class="container-fluid">
            <a class="navbar-brand" href="#">English Instagram</a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarSupportedContent">
                <ul class="navbar-nav me-auto mb-2 mb-lg-0">
                    <li class="nav-item">
                        <a class="nav-link active" aria-current="page" href="#" id="home-link">Home</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#" id="profile-link">Profile</a>
                    </li>
                </ul>
                <form class="d-flex">
                    <input class="form-control me-2" type="search" placeholder="Search" aria-label="Search">
                    <button class="btn btn-outline-success" type="submit">Search</button>
                </form>
            </div>
        </div>
    </nav>
    <div class="container">
        <div class="home-container" id="home-container">
            <h1 class="home-header">Welcome to Instagram</h1>
            <p class="home-intro">A social media platform where you can share your moments with the world.</p>
            <button class="btn btn-primary" id="explore-button">Explore</button>
        </div>
        <div class="post-feed-container" id="post-feed-container" style="display: none;">
            <div class="row">
                <div class="col-md-8">
                    <div class="post-feed">
                        <div class="post">
                            <img class="post-image" src="https://via.placeholder.com/300" alt="Post Image">
                            <div class="post-caption">This is a sample post caption.</div>
                            <button class="btn btn-primary" data-bs-toggle="modal" data-bs-target="#postModal">View Post</button>
                        </div>
                        <div class="post">
                            <img class="post-image" src="https://via.placeholder.com/300" alt="Post Image">
                            <div class="post-caption">Another sample post caption.</div>
                            <button class="btn btn-primary" data-bs-toggle="modal" data-bs-target="#postModal">View Post</button>
                        </div>
                    </div>
                </div>
                <div class="col-md-4">
                    <div class="profile-card">
                        <img src="https://via.placeholder.com/100" alt="Profile Picture">
                        <h5>Smit Patel</h5>
                        <p>Software Engineer from Canada</p>
                        <button class="btn btn-primary">Follow</button>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <div class="modal fade" id="postModal" tabindex="-1" aria-hidden="true">
        <div class="modal-dialog modal-dialog-centered">
            <div class="modal-content">
                <img class="post-image" src="https://via.placeholder.com/300" alt="Post Image">
                <div class="post-caption">This is a sample post caption.</div>
                <button class="btn btn-primary" data-bs-dismiss="modal">Close</button>
            </div>
        </div>
    </div>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/js/bootstrap.bundle.min.js"></script>
    <script>
        const homeLink = document.getElementById('home-link');
        const profileLink = document.getElementById('profile-link');
        const homeContainer = document.getElementById('home-container');
        const postFeedContainer = document.getElementById('post-feed-container');
        const exploreButton = document.getElementById('explore-button');

        homeLink.addEventListener('click', () => {
            homeContainer.style.display = 'block';
            postFeedContainer.style.display = 'none';
        });

        profileLink.addEventListener('click', () => {
            homeContainer.style.display = 'none';
            postFeedContainer.style.display = 'block';
        });

        exploreButton.addEventListener('click', () => {
            homeContainer.style.display = 'none';
            postFeedContainer.style.display = 'block';
        });
    </script>
</body>
</html>
