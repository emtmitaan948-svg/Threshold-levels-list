<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Threshold Levels List</title>

<style>
* {
    box-sizing: border-box;
}

body {
    margin: 0;
    font-family: Arial, sans-serif;
    background: #0b0d12;
    color: white;
}

/* HEADER */

header {
    background: #11141b;
    border-bottom: 1px solid #292e3a;
    padding: 18px 30px;
    display: flex;
    align-items: center;
    justify-content: space-between;
}

.logo {
    font-size: 24px;
    font-weight: bold;
}

nav {
    display: flex;
    gap: 10px;
}

button {
    border: none;
    border-radius: 8px;
    padding: 10px 15px;
    background: #5865F2;
    color: white;
    cursor: pointer;
    font-weight: bold;
}

button:hover {
    opacity: 0.85;
}

/* HERO */

.hero {
    text-align: center;
    padding: 55px 20px 35px;
}

.hero h1 {
    font-size: 45px;
    margin: 0;
}

.hero p {
    color: #8d94a3;
}

/* SEARCH */

.search {
    max-width: 650px;
    margin: 25px auto;
}

.search input {
    width: 100%;
    padding: 15px;
    border-radius: 10px;
    border: 1px solid #303644;
    background: #151923;
    color: white;
    font-size: 16px;
    outline: none;
}

.search input:focus {
    border-color: #5865F2;
}

/* LIST */

.container {
    max-width: 1000px;
    margin: auto;
    padding: 20px;
}

.level {
    display: flex;
    align-items: center;
    gap: 20px;
    background: #141821;
    border: 1px solid #282e3a;
    border-radius: 12px;
    padding: 18px;
    margin-bottom: 12px;
    transition: 0.2s;
}

.level:hover {
    transform: translateY(-2px);
    border-color: #5865F2;
}

.rank {
    width: 50px;
    font-size: 24px;
    font-weight: bold;
    text-align: center;
}

.level-info {
    flex: 1;
}

.level-info h2 {
    margin: 0;
    font-size: 20px;
}

.level-info p {
    margin: 6px 0 0;
    color: #858c9b;
}

.difficulty {
    background: #252b38;
    padding: 8px 12px;
    border-radius: 7px;
    font-size: 13px;
    font-weight: bold;
}

/* FOOTER */

footer {
    text-align: center;
    padding: 45px 20px;
    color: #666d7a;
}

/* MOBILE */

@media (max-width: 650px) {

    header {
        padding: 15px;
    }

    .hero h1 {
        font-size: 34px;
    }

    .level {
        gap: 12px;
    }

    .difficulty {
        display: none;
    }
}
</style>
</head>

<body>

<header>

    <div class="logo">
        Threshold
    </div>

    <nav>
        <button onclick="openDiscord()">💬 Discord</button>
    </nav>

</header>


<section class="hero">

    <h1>Threshold Levels List</h1>

    <p>
        The hardest levels, ranked by difficulty.
    </p>

    <div class="search">
        <input
            type="text"
            id="searchBar"
            placeholder="🔎 Search levels or creators..."
            onkeyup="searchLevels()"
        >
    </div>

</section>


<main class="container" id="levelList">


    <div class="level">

        <div class="rank">
            #1
        </div>

        <div class="level-info">
            <h2>Level Name</h2>
            <p>Creator Name</p>
        </div>

        <div class="difficulty">
            Extreme Demon
        </div>

    </div>


    <div class="level">

        <div class="rank">
            #2
        </div>

        <div class="level-info">
            <h2>Another Level</h2>
            <p>Creator Name</p>
        </div>

        <div class="difficulty">
            Extreme Demon
        </div>

    </div>


    <div class="level">

        <div class="rank">
            #3
        </div>

        <div class="level-info">
            <h2>Third Level</h2>
            <p>Creator Name</p>
        </div>

        <div class="difficulty">
            Extreme Demon
        </div>

    </div>


    <div class="level">

        <div class="rank">
            #4
        </div>

        <div class="level-info">
            <h2>Fourth Level</h2>
            <p>Creator Name</p>
        </div>

        <div class="difficulty">
            Extreme Demon
        </div>

    </div>


    <div class="level">

        <div class="rank">
            #5
        </div>

        <div class="level-info">
            <h2>Fifth Level</h2>
            <p>Creator Name</p>
        </div>

        <div class="difficulty">
            Extreme Demon
        </div>

    </div>


</main>


<footer>

    Threshold Levels List © 2026

</footer>


<script>

function searchLevels() {

    let input = document
        .getElementById("searchBar")
        .value
        .toLowerCase();

    let levels = document
        .getElementsByClassName("level");

    for (let i = 0; i < levels.length; i++) {

        let text = levels[i]
            .innerText
            .toLowerCase();

        if (text.includes(input)) {

            levels[i].style.display = "flex";

        } else {

            levels[i].style.display = "none";

        }

    }

}


function openDiscord() {

    window.open(
        "https://discord.com",
        "_blank"
    );

}

</script>

</body>
</html>
