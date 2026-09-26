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
    background: #090b10;
    color: white;
}

/* HEADER */

header {
    height: 70px;
    padding: 0 30px;
    background: #11141b;
    border-bottom: 1px solid #292e38;

    display: flex;
    align-items: center;
    justify-content: space-between;

    position: sticky;
    top: 0;
    z-index: 10;
}

.logo {
    font-size: 24px;
    font-weight: 800;
}

.logo span {
    color: #5865f2;
}

nav {
    display: flex;
    gap: 10px;
}

nav button {
    background: #1b1f2a;
    border: 1px solid #303644;
    color: white;
    padding: 9px 15px;
    border-radius: 8px;
    cursor: pointer;
}

nav button:hover {
    background: #5865f2;
}

/* HERO */

.hero {
    text-align: center;
    padding: 60px 20px 35px;

    background:
        radial-gradient(circle at top, #202638, #090b10 65%);
}

.hero h1 {
    font-size: 48px;
    margin: 0;
}

.hero p {
    color: #8b92a1;
    font-size: 17px;
}

/* SEARCH */

.search {
    max-width: 650px;
    margin: 30px auto 0;
}

.search input {
    width: 100%;
    padding: 16px;

    background: #151922;
    border: 1px solid #303644;
    border-radius: 10px;

    color: white;
    font-size: 16px;
    outline: none;
}

.search input:focus {
    border-color: #5865f2;
}

/* STATS */

.stats {
    max-width: 1000px;
    margin: 25px auto;
    padding: 0 20px;

    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 15px;
}

.stat {
    background: #131720;
    border: 1px solid #282e39;
    border-radius: 12px;
    padding: 20px;
    text-align: center;
}

.stat h2 {
    margin: 0;
    font-size: 27px;
}

.stat p {
    margin: 7px 0 0;
    color: #777f8e;
}

/* CONTROLS */

.controls {
    max-width: 1000px;
    margin: 35px auto 15px;
    padding: 0 20px;

    display: flex;
    justify-content: space-between;
    gap: 10px;
}

select {
    background: #151922;
    border: 1px solid #303644;
    color: white;

    padding: 10px;
    border-radius: 8px;
}

/* LEVEL LIST */

.container {
    max-width: 1000px;
    margin: auto;
    padding: 10px 20px 50px;
}

.level {
    display: flex;
    align-items: center;
    gap: 20px;

    background: #141821;
    border: 1px solid #292f3a;

    padding: 18px;
    margin-bottom: 12px;

    border-radius: 13px;

    transition: 0.2s;
}

.level:hover {
    transform: translateY(-3px);
    border-color: #5865f2;
}

/* TOP 3 */

.level:nth-child(1) {
    border-color: #ffd700;
}

.level:nth-child(2) {
    border-color: #bfc5cc;
}

.level:nth-child(3) {
    border-color: #cd7f32;
}

.rank {
    width: 55px;

    font-size: 25px;
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

.badges {
    display: flex;
    gap: 7px;
}

.badge {
    padding: 7px 10px;
    border-radius: 7px;

    background: #252b38;

    font-size: 12px;
    font-weight: bold;
}

.extreme {
    background: #552020;
}

.verified {
    background: #173d29;
}

/* BUTTON */

.level button {
    background: #5865f2;
    border: none;

    color: white;

    padding: 9px 12px;
    border-radius: 7px;

    cursor: pointer;
}

.level button:hover {
    opacity: 0.8;
}

/* FOOTER */

footer {
    text-align: center;
    padding: 45px;

    color: #555d6c;

    border-top: 1px solid #202530;
}

/* MOBILE */

@media (max-width: 700px) {

    header {
        padding: 0 15px;
    }

    .hero h1 {
        font-size: 34px;
    }

    .stats {
        grid-template-columns: 1fr;
    }

    .level {
        gap: 10px;
    }

    .badges {
        display: none;
    }

    .level button {
        display: none;
    }

}
</style>
</head>


<body>

<header>

    <div class="logo">
        Threshold<span>.</span>
    </div>

    <nav>

        <button onclick="showAll()">
            Levels
        </button>

        <button onclick="openDiscord()">
            💬 Discord
        </button>

    </nav>

</header>


<section class="hero">

    <h1>
        Threshold Levels List
    </h1>

    <p>
        Ranking the hardest levels in Geometry Dash.
    </p>

    <div class="search">

        <input
            id="search"
            type="text"
            placeholder="🔎 Search levels or creators..."
            oninput="updateList()"
        >

    </div>

</section>


<section class="stats">

    <div class="stat">
        <h2>100</h2>
        <p>Levels Ranked</p>
    </div>

    <div class="stat">
        <h2>78</h2>
        <p>Extreme Demons</p>
    </div>

    <div class="stat">
        <h2>24/7</h2>
        <p>List Updates</p>
    </div>

</section>


<div class="controls">

    <select id="difficulty" onchange="updateList()">

        <option value="all">
            All Difficulties
        </option>

        <option value="extreme">
            Extreme Demon
        </option>

        <option value="hard">
            Hard Demon
        </option>

        <option value="medium">
            Medium Demon
        </option>

    </select>


    <select id="sort" onchange="sortLevels()">

        <option value="rank">
            Rank
        </option>

        <option value="name">
            Name
        </option>

        <option value="creator">
            Creator
        </option>

    </select>

</div>


<main class="container" id="levels">


    <div class="level"
         data-name="Bloodbath"
         data-creator="Riot"
         data-difficulty="extreme">

        <div class="rank">
            #1
        </div>

        <div class="level-info">

            <h2>
                Bloodbath
            </h2>

            <p>
                Riot
            </p>

        </div>

        <div class="badges">

            <div class="badge extreme">
                Extreme Demon
            </div>

            <div class="badge verified">
                ✓ Verified
            </div>

        </div>

        <button onclick="openLevel('Bloodbath')">
            View
        </button>

    </div>


    <div class="level"
         data-name="Sonic Wave"
         data-creator="Sunix"
         data-difficulty="extreme">

        <div class="rank">
            #2
        </div>

        <div class="level-info">

            <h2>
                Sonic Wave
            </h2>

            <p>
                Sunix
            </p>

        </div>

        <div class="badges">

            <div class="badge extreme">
                Extreme Demon
            </div>

            <div class="badge verified">
                ✓ Verified
            </div>

        </div>

        <button onclick="openLevel('Sonic Wave')">
            View
        </button>

    </div>


    <div class="level"
         data-name="Artificial Ascent"
         data-creator="Riot"
         data-difficulty="extreme">

        <div class="rank">
            #3
        </div>

        <div class="level-info">

            <h2>
                Artificial Ascent
            </h2>

            <p>
                Riot
            </p>

        </div>

        <div class="badges">

            <div class="badge extreme">
                Extreme Demon
            </div>

        </div>

        <button onclick="openLevel('Artificial Ascent')">
            View
        </button>

    </div>


    <div class="level"
         data-name="Nine Circles"
         data-creator="Zobros"
         data-difficulty="hard">

        <div class="rank">
            #4
        </div>

        <div class="level-info">

            <h2>
                Nine Circles
            </h2>

            <p>
                Zobros
            </p>

        </div>

        <div class="badges">

            <div class="badge">
                Hard Demon
            </div>

        </div>

        <button onclick="openLevel('Nine Circles')">
            View
        </button>

    </div>


    <div class="level"
         data-name="Future Funk"
         data-creator="JonathanGD"
         data-difficulty="hard">

        <div class="rank">
            #5
        </div>

        <div class="level-info">

            <h2>
                Future Funk
            </h2>

            <p>
                JonathanGD
            </p>

        </div>

        <div class="badges">

            <div class="badge">
                Hard Demon
            </div>

        </div>

        <button onclick="openLevel('Future Funk')">
            View
        </button>

    </div>


</main>


<footer>

    Threshold Levels List © 2026

    <br><br>

    Built for the Geometry Dash community.

</footer>


<script>

function updateList() {

    const search =
        document
        .getElementById("search")
        .value
        .toLowerCase();

    const difficulty =
        document
        .getElementById("difficulty")
        .value;

    const levels =
        document
        .querySelectorAll(".level");


    levels.forEach(level => {

        const name =
            level.dataset.name.toLowerCase();

        const creator =
            level.dataset.creator.toLowerCase();

        const levelDifficulty =
            level.dataset.difficulty;


        const matchesSearch =
            name.includes(search) ||
            creator.includes(search);


        const matchesDifficulty =
            difficulty === "all" ||
            levelDifficulty === difficulty;


        if (matchesSearch && matchesDifficulty) {

            level.style.display = "flex";

        } else {

            level.style.display = "none";

        }

    });

}


function sortLevels() {

    const container =
        document.getElementById("levels");

    const levels =
        Array.from(
            container.querySelectorAll(".level")
        );

    const sort =
        document.getElementById("sort").value;


    levels.sort((a, b) => {

        if (sort === "name") {

            return a.dataset.name
                .localeCompare(b.dataset.name);

        }

        if (sort === "creator") {

            return a.dataset.creator
                .localeCompare(b.dataset.creator);

        }

        return (
            parseInt(
                a.querySelector(".rank").innerText
            )
            -
            parseInt(
                b.querySelector(".rank").innerText
            )
        );

    });


    levels.forEach(level => {

        container.appendChild(level);

    });

}


function showAll() {

    document.getElementById("search").value = "";

    document.getElementById("difficulty").value = "all";

    updateList();

}


function openDiscord() {

    window.open(
        "https://discord.com",
        "_blank"
    );

}


function openLevel(name) {

    alert(
        name +
        " — Level page coming soon!"
    );

}

</script>

</body>
</html>
