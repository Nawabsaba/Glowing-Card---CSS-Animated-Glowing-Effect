# Glowing-Card---CSS-Animated-Glowing-Effect : -
🔥 Glowing Card – CSS Animated Glowing Effect [Only CSS] | HTML & CSS Tutorial

Want to create a beautiful animated glowing card using only CSS? In this video, learn how to design a modern glowing card with attractive neon light effects and smooth CSS animations.

✨ In This Video:
01. Create a Glowing Card Using HTML & CSS
02. Pure CSS Animated Glowing Effect
03. Add Neon Border Effects
04. CSS Glow Animation
05. Smooth Hover Effects
06. Create Modern Card UI Design
07. Attractive Animated Border Effects
08. No JavaScript Required!

💻 Technologies Used:
1) HTML5
2) CSS3
3) CSS Animations
4) CSS Hover Effects
5) Pure CSS Styling

# Youtube Video Thumbnail Image : - 
![image alt](https://github.com/Nawabsaba/Glowing-Card---CSS-Animated-Glowing-Effect/blob/7b4c5cb0d40c457be5fbf0da2a94622f4062a6c7/Youtube%20video%20Thumbnail.jpeg)

# Avater PNG Image : -
![image alt](https://github.com/Nawabsaba/Glowing-Card---CSS-Animated-Glowing-Effect/blob/cd4cb20ee9ad73fab8a4b9bb4b16a68b490c239d/avatar.png)

# HTML Program : -
      <!DOCTYPE html>
      <html lang="en">
      <head>
         <meta charset="UTF-8">
         <meta http-equiv="X-UA-Compatible" content="IE=edge">
         <meta name="viewport" content="width=device-width, 
         initial-scale=1.0">
         <link rel="stylesheet" href="style.css">
         <title>Glowing Card | Amith Thoughts </title>
     </head>
     <body>

      <div class="card">
          <div class="image-container">
              <img src="avatar.png" alt="avatar">
          </div>

        <h2>Glowing Card</h2>
        <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. 
          Tenetur inventore aliquam non alias, 
          expedita laboriosam obcaecati id fuga repudiandae. 
          Facere quia doloribus, 
          iusto voluptate cumque perferendis perspiciatis 
          architecto eum recusandae.</p>
        <a href="#">Read More...</a>

        <div class="icons">
            <ion-icon name="logo-facebook"></ion-icon>
            <ion-icon name="logo-instagram"></ion-icon>
            <ion-icon name="logo-github"></ion-icon>
            <ion-icon name="logo-twitter"></ion-icon>
        </div>


        <script type="module" src="https://unpkg.com/ionicons@5.5.2/dist/ionicons/ionicons.esm.js"></script>
       <script nomodule src="https://unpkg.com/ionicons@5.5.2/dist/ionicons/ionicons.js"></script>
       </div>
     </body>
     </html>

# CSS Program : -
      :root {
        --card-height:  65vh;
        --card-width:   calc(var(--card-height) / 1.5);
        --bg:           25 28 41;
        --color:        88 199 250;
    }

    body {
        min-height: 100vh;
        background: rgba(var(--bg) / 90%);
        display: flex;
        align-items: center;
        flex-direction: column;
        padding-top: 2rem;
        padding-bottom: 2rem;
        box-sizing: border-box;
        font-family: Roboto;
    }

     .card {
        background: rgba(var(--bg));
        width: var(--card-width);
        height: var(--card-height);
        padding: 30px;
        position: relative;
        border-radius: 6px;
        color: rgba(var(--color) / 60%);
        cursor: pointer;
        text-align: center;
        margin-top: 30px;
    }

      .card img {
         width: 120px;
         border-radius: 50%;
    }

     .image-container {
         background-color: rgba(var(--color) / 30%);
         padding: 10px;
         margin: -20px;
         margin-bottom: 20px;
         border-radius: 7px;
    }

    .card p  {
        text-align: left;
    }

     .card a {
        color: rgba(var(--color) / 60%);
       text-decoration: none;
    }

    .icons ion-icon {
        font-size: 2.5rem;
        margin: 5px;
        margin-top: 20px;
    }

    @keyframes spin {
        0% {
           --rotate: 0deg;
          }
        100% {
          --rotate: 360deg;
        }
    }

      .card::before {
         content: "";
         width: 104%;
         height: 102.7%;
         border-radius: 8px;
         background-image: linear-gradient(
         var(--rotate),
         #5ddcff,
         #3c67e3 43%,
         #4e00c2
       );
        position: absolute;
        z-index: -1;
        top: -1.3%;
        left: -2%;
        animation: spin 2.5s linear infinite;
    }

    .card::after {
       position: absolute;
       content: "";
       top: calc(var(--card-height) / 6);
       left: 0;
       right: 0;
       z-index: -1;
       height: 100%;
       width: 100%;
       margin: 0 auto;
       transform: scale(0.8);
       filter: blur(calc(var(--card-height) / 6));
       background-image: linear-gradient(
        var(--rotate),
        #5ddcff,
        #3c67e3 43%,
        #4e00c2
      );
       opacity: 1;
       transition: opacity 0.5s;
      animation: spin 2.5s linear infinite;
    }

    @property --rotate {
       syntax: "<angle>";
       initial-value: 132deg;
      inherits: false;
    }

     .card:hover:before,
     .card:hover:after {
       animation: none;
       opacity: 0;
    }
