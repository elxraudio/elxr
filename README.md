<!-- Existing style block with adjustments -->
<style>
body {
    background-color: black;
    color: white;
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
}

/* Hide or style the default title */
.site-title, #site-title {
    display: none; /* Or use 'color: white;' to change the color */
}

p {
    text-align: center;
    margin-top: 0;
}

.link-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    margin-top: 30px;
}

a.button {
    display: block;
    width: 120px;
    padding: 15px 0;
    margin: 10px 0;
    background-color: white;
    color: black;
    text-align: center;
    text-decoration: none;
    font-size: 13px;
    font-weight: 800;
    border-radius: 0;
    transition: background-color 0.3s;
}

a.button:hover {
    background-color: #e0e0e0;
}

/* Styles for the fact button */
a.fact-button {
    display: block;
    width: 120px;
    padding: 15px 0;
    margin: 20px 0 10px 0; /* Extra top margin for spacing */
    background-color: black;
    color: white;
    text-align: center;
    text-decoration: none;
    font-size: 20px; /* Larger font size for the star */
    font-weight: 800;
    border: 2px solid white;
    border-radius: 0;
    cursor: pointer;
    transition: background-color 0.3s, color 0.3s;
}

a.fact-button:hover {
    background-color: #333;
    color: #fff;
}

/* Styles for the fact display */
#fact-display {
    color: white;
    text-align: center;
    margin-top: 20px;
    font-size: 14px;
    padding: 0 20px;
}
</style>

<!-- Removed your own 'elxr' heading to prevent duplication -->

<p><span style="font-size: 10px;">close your eyes<br>take the <strong>elxr</strong></span></p>

<div class="link-container">
  <a href="https://open.spotify.com/artist/..." class="button">Spotify</a>
  <a href="https://music.apple.com/ca/artist/..." class="button">Apple Music</a>
  <a href="https://www.tiktok.com/@elxraudio" class="button">TikTok</a>
  <a href="https://soundcloud.com/elxr_audio" class="button">SoundCloud</a>
  <a href="https://youtube.com/@elxr_audio" class="button">YouTube</a>
  <a href="https://www.instagram.com/elxr_audio" class="button">Instagram</a>
</div>

<!-- Add the star below the links -->
<p style="text-align: center; font-size: 13px; margin-top: 10px;">✶</p>

<!-- Fact Button -->
<a class="fact-button" id="fact-button">✶</a>

<!-- Fact Display Area -->
<div id="fact-display"></div>

<!-- JavaScript to handle the fact display -->
<script>
// Array of interesting cosmos facts
const cosmosFacts = [
    "The universe is around 13.8 billion years old.",
    "There are more stars in the universe than grains of sand on Earth.",
    "A day on Venus is longer than a year on Venus.",
    "Neutron stars are so dense that a teaspoon of their material would weigh about 10 million tons.",
    "Light from distant stars and galaxies takes millions of years to reach us.",
    "Black holes can slow down time due to their immense gravity.",
    "The observable universe is about 93 billion light-years in diameter.",
    "Our galaxy, the Milky Way, is on a collision course with the Andromeda galaxy.",
    "There are rogue planets floating through space unattached to any star.",
    "Dark matter makes up about 27% of the universe, but we can't see it directly."
];

// Function to display a random fact
function displayRandomFact() {
    const factDisplay = document.getElementById('fact-display');
    const randomFact = cosmosFacts[Math.floor(Math.random() * cosmosFacts.length)];
    factDisplay.textContent = randomFact;
}

// Add event listener to the fact button
document.getElementById('fact-button').addEventListener('click', displayRandomFact);
</script>