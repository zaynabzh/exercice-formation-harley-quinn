# exercice-formation-harley-quinn
Exercice de mise en pratique de notions de CSS
[exercice-harley-quinn.html](https://github.com/user-attachments/files/22583985/exercice-harley-quinn.html)
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <link rel="stylesheet" href="assets/exercice-harley-quinn.css">
    <title>Profil d'Harley Quinn</title>
</head>

<body>
    <header>
        <div>
            <img src="links/carte.png" alt="formes de jeu de cartes" class="forme-g">
        </div>
        <div>
            <strong>Profil d'Harley Quinn</strong>
        </div>
        <div>
            <img src="links/carte.png" alt="formes de jeu de cartes" class="forme-d">
        </div>
    </header>

    <section id="intro">[exercice-harley-quinn.css](https://github.com/user-attachments/files/22583990/exercice-harley-quinn.css)body{
    margin: auto;
    overflow-x: hidden; /* overflow-x: hidden; = désactive le scroll à droite (X = à l'horizontale) - bonne astuce pour les éléments qui sont amenés à dépasser */
}


header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    font-size: 20pt;
    height: 80px;
    padding: 0 20px;
    background-image: url(/links/texture.jpg);
    color: #fff; 
}

.forme-g{
    height: 60px;
    animation: forme-g 4s infinite;
}![texture](https://github.com/user-attachments/assets/9e97be5e-2c4a-4113-a146-da4760555b04)
<img width="1248" height="702" alt="harley-quinn" src="https://github.com/user-attachments/assets/c7ccefed-ef4c-41a3-a2e3-ff30412176ec" />
<img width="512" height="512" alt="emoticone-hq" src="https://github.com/user-attachments/assets/70154ce6-02fa-4b92-88d3-91eab5b185c3" />
<img width="600" height="600" alt="carte" src="https://github.com/user-attachments/assets/1b71278a-07dc-4fca-9477-2be7cbe36ae9" />


.forme-d{
    height: 60px;
    animation: forme-d 4s infinite;
}

#intro {
    display: flex;
    justify-content: center;
    align-items: center;
    padding-top: 100px ;
}

#intro .img {
   margin-right: 20px;
   height: 150px;
}

#intro h1 {
    background-color: white;
    color: #047A90;
    border: 1px solid #047A90;
    text-align: center;
    padding: 10px;
}

#intro a{
    text-decoration: none; /* retire le soulignement du lien sur le texte */
}

#intro h1:hover {
    background-color:#047A90 ;
    color: #fff;
    border: 1px solid #fff;
}

#intro img { 
    width: 220px;
    height: 150px;
    object-fit: cover;  /* garde les proportions de l'image, peut importe le responsive */
    transition: all 2s; /* effet de ralentit sur la modififation demandé lors du survol */
}

#intro img:hover{
    transform: scale(2) rotate(5deg); /* effet de zoom et de rotation lors du survol de l'élément*/
}

.emoticone{
    display: flex;
    justify-content: center;
}

.emoticone-hq{
    width: 100px;
    padding-top: 30px ;
    animation: emoticone-hq  10s infinite;
}

#portfolio {
    text-align: center;
}

h2{
    color: #047A90;
    border-bottom: 1px solid #047A90;
    border-top: 1px solid #047A90;
    margin: auto;
    width: 200px;
    padding: 5px;
}
/* margin: auto; = ajoute une marge auto en fonction de la dimension définit pour le contenair // width: 200px; = définit la largeur du contenair */


h2:hover{
    transform: scale(1.1);
    color: #303032;
}

.container {
    display: flex; /* agit toujours sur les enfants directs */
    flex-wrap: wrap;
    gap: 20px;
    padding: 0 20px;
    padding-top: 20px; 
}

.item{
    width: calc(50% - 10px); /* "calc" permet de palier à la problématique de marge que flex-wrap prend en compte - les 10px font parti du gap */
}    

.item .btn{
    display:block; /* ne peut pas s'aligner avec un text-align : center, nécessité d'avoir un margin auto pour l'aligner */
    margin: auto;
    width: 200px; 
    color: #fff;
    background: #303032; 
    text-decoration: none;
    border-radius:50px; 
    font-size: 20px;
    padding: 20px 0px;
    transition: all .7s;
    transition-timing-function: steps(6, end); /* nécéssité d'indiquer une valeur width de départ puis d'arrivée (dans :hover) */
}

.item .btn:hover{
    background-image: url(/Exercices/Exercice-1/texture.jpg);
    transform: scale(.9);
    width: 100px;
}

#filmographie {
    text-align: center;
    padding: 60px 0 60px 0;
}

.ba{
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
    padding-top: 40px;  
}


footer {
    display: flex;
    align-items: center;
    justify-content: center;
    height: 40px;
    background: #303032;
    color: #fff;
}

@media (max-width:768px){
    #intro{
        flex-direction: column;
        padding-bottom: 70px;
    }

    .img{
        padding-bottom: 30px;
    }

    .container{
        flex-direction: column; 
        align-items: center;       
    }
    .item{
        width: 200px;
    }
    .bio{
        width: 90vw;
        margin: 0 auto; /* permet de centre l'élément */
    }
    iframe{
        max-width: 90vw;
        margin: 0 auto;
    }
    .ba-bis {
        padding-bottom: 50px;       
    } 
    
    .emoticone-hq{
        animation: forme-g 4s infinite ;
    }
}

@media (max-width : 1080px){
    /* .ba-bis {
       padding-bottom: 50px;       
    } */
}


@keyframes emoticone-hq{
    0% {
        transform: translateX(380px);
    }
    20%{
        transform: translateY(200px) rotate(50deg) ;
    }
    40%{
        transform: translateZ(50px) rotate(-50deg);        
    }
    60%{
        transform: translateX(-380px);
    }
    80%{
        transform: translateY(200px) rotate(360deg);
    } 
    100%{
        transform: translateX(380px);
    }
}


@keyframes forme-g {
    0%{
        transform : rotate(-40deg);
    }
    50%{
        transform: rotate(40deg);
    }
    100%{
        transform: rotate(-40deg);
    }
}

@keyframes forme-d {
    0%{
        transform : rotate(40deg);
    }
    50%{
        transform: rotate(-40deg);
    }
    100%{
        transform: rotate(40deg);
    }
}


        <div class="img">
            <a href="https://fr.wikipedia.org/wiki/Harley_Quinn" target="_blank"><img src="links/harley-quinn.jpg" alt="photo de l'actrice Margot Robbie dans le rôle d'Harley Quinn"></a>
        </div>

        <div class="bio">
            <a href="https://fr.wikipedia.org/wiki/Harley_Quinn" target="_blank"><h1>Biographie</h1></a>
            <p>Sous son pseudo se cache Harleen Quinzel, une jeune psychiatre et gymnaste talentueuse. 
            <br/> Elle obtient son diplôme universitaire puis travaille à l'asile d'Arkham. 
            <br/> C'est là-bas que son histoire va basculer, en faisant la rencontre du Joker.</p>
        </div>  
    </section>

    <div class="emoticone">
        <img src="/links/emoticone-hq.png" alt="émoticone d'Harley Quinn" class="emoticone-hq">
    </div>

    <section id="portfolio">
        <h2>Portfolio</h2>
        <div class="container">
            <div class="item">
                <a href="https://www.dc.com/characters/harley-quinn" class="btn">Projet 1</a>
            </div>

            <div class="item">
                <a href="#" class="btn">Projet 2</a>
            </div>
            
            <div class="item">
                <a href="#" class="btn">Projet 3</a>
            </div>

            <div class="item">
                <a href="#" class="btn">Projet 4</a>
            </div>
        </div>
    </section>

    <section id="filmographie">
        <h2>Filmographie</h2>
        <div class="ba">
            <div class="ba-bis">
                <iframe width="560" height="315" src="https://www.youtube.com/embed/b6Jl8YUNYek?si=QgD4zoNSki8G8qz_" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
            </div>
            <div class="ba-bas">
                <iframe width="560" height="315" src="https://www.youtube.com/embed/EJhiK5VotTY?si=c4Rt5-PrxUSDoucu" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
            </div>
        </div>     
        
        <!-- ATTENTION les dimensions d'iframe peuvent impacter le responsive -->
        
    </section>

    <footer>
        <span>Maison d'édition DC Comics</span>
    </footer>
</body>

</html>
