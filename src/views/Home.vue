<template>
  <div class="home">
    <div class="header">
      <div class="textbackground"><h1>Produkte & Prozesse Wilke<br>durch effiziente Prozesse<br>Unternehmen stärken</h1><p>
        wir unterstützen effizient<br> und Nachhaltig
        </p>
        </div>
      <img id = "headerpic" src = "../assets/Chris-unge-Goerdeller.jpg" alt="Goerdellerring"/>
    </div>
    <div class="content">
      <h1>
        Was wir tun
      </h1>
      <div id="categories">
        <div class="category">
          <img src="../assets/people-431943_1920.jpg" alt="">
        </div>
      </div>
      <p style=width:60%;margin-inline:auto;>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolor repellendus consequuntur ab atque voluptas praesentium pariatur, autem id! At velit porro labore incidunt obcaecati molestiae iste nesciunt commodi architecto quaerat? Magnam, voluptate magni, corporis nostrum eos eaque quibusdam autem eius cumque doloremque, temporibus explicabo natus quo cupiditate? Neque commodi blanditiis veritatis dignissimos odit, quibusdam ducimus officiis dolore voluptatem temporibus necessitatibus accusamus illo accusantium doloribus fugit ipsa ad inventore labore corporis rerum tenetur natus rem sint quidem! Possimus sapiente fuga sunt atque accusamus repellat veniam nesciunt ad alias animi. Eligendi magni reprehenderit, neque accusantium est eum eos voluptate ipsa tempore quaerat libero vero aliquid placeat dicta eius amet, cupiditate iure veniam perspiciatis minima, nobis vitae soluta quibusdam molestiae. Numquam illo, voluptate aut vitae similique corrupti officiis dolore veritatis consequatur iure qui enim vero unde optio consequuntur fugiat consectetur in. Dolorum saepe tenetur iste laboriosam quis quaerat inventore laudantium eius eaque recusandae, quo repudiandae error aperiam maxime veniam consectetur in hic esse harum quos officiis corporis tempore architecto iusto? Optio, dolore mollitia libero nostrum asperiores minima fugiat quisquam laborum reiciendis rerum vitae dolores ut tempora alias at? Odit accusantium excepturi facere velit.

        Warteschlangenoptimierung
        Produktverbesserung
        Prozessberatung
      </p>
    </div>
  </div>
</template>
<style scoped>
img{
  width:min(20rem,100%);
}
.content{
  text-align: center;
}
.header{
  background:url("../assets/Chris-unge-Goerdeller.jpg");
  width:100%;
  background-size: cover;
  background-position: right center;
  height:30vw;
  overflow: hidden;
}
.textbackground{
  text-align: left;
  padding:1px;
  margin-left:-10%;
  background-color:var(--maincolor);
  width:65%;
  height:30vw;
  transform:skewX(-12deg);
  opacity: 0.8;
}
h1{
  color:var(--maincolor);
}
.textbackground h1{
  color:var(--contrast);
  margin-left:30%;
  font-size:2.5vw;
  line-height: 4vw;
  margin-top:3vw;
  transform:skewX(12deg);
  opacity:1;
}
.textbackground p{
  color:rgb(200,200,200,1);
  margin-left:33%;
  transform:skewX(12deg);
  opacity: 1;
  font-size:1.5vw;
}
#headerpic{
    visibility: hidden;
    width:100%;
    height:auto;
    align-self:right center;
  }
</style>
