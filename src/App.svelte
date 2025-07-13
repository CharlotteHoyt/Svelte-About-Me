<script>
  import ImageCard from "./lib/ImageCard.svelte";

  let cardData = [
    {
      image: "src/assets/twin.png",
      title: "Twin",
      description: "My twin sister is my best friend! An amusing fact is that my dad's side of the family has three sets of identical girl twins.",
    },
    {
      image: "src/assets/robotics.png",
      title: "99621A Lemon Pi",
      description: "During high school I competed in the VEX Robotics Competion on an award-winning all girls team of five!",
    },
    {
      image: "src/assets/rover.png",
      title: "TrickFire Robotics",
      description: "I am now on a team that competes in the University Rover Challenge, an international competition that challenges students to design and build rovers relevant to future Mars exploration!",
    },
    {
      image: "src/assets/hackathon.png",
      title: "Coding",
      description: "I love to code and am always seeking opportunities to develop new skills and collaborate with others!",
    },
    {
      image: "src/assets/confetti.png",
      title: "Color Lover",
      description: "I enjoy all things colorful and believe color has an extraordinary place in ordinary life!",
    },
    {
      image: "src/assets/iceCream.png",
      title: "Washington",
      description: "I live just north of Seattle in Washington state! I love the evergreen trees and even the rain. Molly Moon's has the best ice cream in the Seattle area!",
    },
  ];

  let name = "Charlotte";
  let bio = "I love coding, robotics, playing the violin, baking, and spending time with my people (and animals)! I'm a loyal light mode user, sprinkle collector, lover of color, identical twin, and total Hufflepuff."
  let favorites = ["Strawberry Ice Cream 🍦", "Giraffes 🦒", "Fall 🍂", "Yellow 💛", "Coding 👩‍💻", "Robotics 🤖", "Violin 🎻", "Baking 🧁", "My Two Silly Cats 🐱"];

  let funFacts = ["I have sectoral heterochromia!", "I rode a horse that was in a Disney movie!", "I got second place in a spelling bee in fourth grade!", "I'm scared of hiccups!"];
</script>

<style>
  * {
    background-color: #FAF0E4;
  }

  .container {
    background-color: #FAF0E4;
  }

  h1 {
    color: #FF8551;
  }

  h2 {
    color: #4EAABD;
  }

  p {
    color: #6A6767;
  }

  .container {
    max-width: 800px;
    margin: 0 auto;
    padding: 20px;
    text-align: center;
  }

  .favorites {
    display: flex;
    justify-content: center;
    gap: 15px;
    flex-wrap: wrap;
  }

  .favorite {
    background-color: #FFDEDE;
    color: #FF8551;
    font-weight: bold;
    padding: 10px 15px;
    border-radius: 5px;
  }

  .card-container {
      display: inline-flex;
      flex-wrap: wrap;
      justify-content: center;
      align-items: center;
      width: 100%;
      margin-top: -1em;
  }

  .roundedImage {
    height: 250px;
    width: 250px;
    object-fit: cover;
    overflow: hidden;
    border-radius: 50%;

    display: block;
    margin-left: auto;
    margin-right: auto;
  }
</style>

<div class="container">
  <img class="roundedImage" src="src/assets/charlotte.jpeg" draggable="false" alt="A headshot of a girl in a yellow sweater, blue top, and necklace in front of a blue wall.">
  <br>
  <h1>Hello, World! 🪩</h1>
  <p>My name is {name}! I am a student at the University of Washington Bothell.</p>
  <p>{bio}</p>

  <br>

  <h2>My Favorites</h2>
  <div class="favorites">
    {#each favorites as favorite}
      <div class="favorite">{favorite}</div>
    {/each}
  </div>

  <br>
  <br>

  <h2>Fun Facts About Me</h2>
  <div class="funFacts">
    {#each funFacts as fact}
      <p>{fact}</p>
    {/each}
  </div>

  <br>

  <h2>Get to Know Me</h2>
  <div class="card-container">
    {#each cardData as { image, title, description }}
      <ImageCard {image} {title} {description} />
    {/each}
  </div>
</div>