<!DOCTYPE html>
<html lang="pt-br">
  <head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <style>
     .button {
        position: relative;
        display: inline-block;
        background: transparent; /* Change to transparent */
        border: none;
        cursor: pointer;
        padding: 5px;
        transition: transform 1s;
        max-height: 20%;
        max-width: 20%;
        z-index: 1;
      }
     .button:hover {
        transform: scale(1.5); /* Adjusted scale factor for better user experience on mobile devices */ z-index: 2;
      }
     .button img {
        width: 100%;
        height: 100%;
        object-fit: cover;
        border-radius: 2px 30px;
      }

     .description {
        background: #DFDACC;
        border-radius: 10px;
        bottom: 0;
        left: 0;
        padding: 10%;
        position: absolute;
        width: 80%;
        margin-bottom: 5%;
        visibility: hidden;
        opacity: 0;
        transition: visibility 0s, opacity 1s;
        color: #85764E;
        font-size: 35px;
        text-align: center; /* Center the text */
      }

     .button:hover .description {
        visibility: visible;
        opacity: 1;
      }

      /* Media queries for responsiveness */
      @media screen and (min-width: 768px) {
       .button {
          max-height: 20%;
          max-width: 20%;
          display: inline-block;
          vertical-align: top; /* Align buttons vertically on larger screens */
        }
      }

     .button:not(:first-child) {
        margin-left: 2%; /* Add margin to align buttons horizontally on larger screens */
      }

      /* Media query for stacking buttons vertically on mobile devices */
      @media screen and (max-width: 767px) {
       .button {
          max-height: 45%; /* Adjusted to better fit mobile screens */
          max-width: 90%; /* Adjusted to better fit mobile screens */
          display: block;
          margin: 0 auto; /* Center buttons horizontally on mobile devices */
        }
      }
    </style>

    <script>
      // add event listener to buttons
      document.querySelectorAll('.button')
       .forEach(button => {
          button.addEventListener('mouseover', () => {
            // animate button on hover
            button.classList.add('animate');
          });
          button.addEventListener('mouseout', () => {
            // remove animation on mouse out
            button.classList.remove('animate');
          });
        });
    </script>
  </head>
  <body>
    <button href="https://www.reveev.com.br/produtos/colecao-respire" class="button" id="button1">
      <img src="https://images.squarespace-cdn.com/content/62ed8e43a556e54dfbb1051c/ea1f2073-d7c0-4d17-9763-c825bf98198f/_N4A6058.jpg?content-type=image%2Fjpeg" alt="Image 1">
      <div class="description">
        <h3>Coleção Respire</h3>
      </div>
    </button>
  </body>
</html>
