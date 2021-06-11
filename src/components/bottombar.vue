<template>
<div id="mainbody">
    <div class="linkwrap">
        <router-link to="/Impressum">
          Impressum
        </router-link>
    </div>
    <div class="linkwrap">
        <router-link to="/Impressum">
          Datenschutz
        </router-link>
    </div>
    <div class="linkwrap">
        <router-link to="/Impressum">
          Kontakt
        </router-link>
    </div>
</div>
</template>
<style scoped>
#mainbody{
    margin:0;
    margin-top:auto;
    display:flex;
    flex-direction: row;
    flex-wrap:wrap;
    justify-content: center;
    background-color:var(--maincolor);
    opacity:0.9;
    padding-block:1rem;
    font-size:min(1.5rem,4vw);
}
.linkwrap{
    flex-basis: min(33%,13rem);
    text-decoration:none;
    /* padding-inline:1vw; */
}
a{
    text-decoration: none;
    cursor: pointer;
    position: relative;
    color:rgb(85, 85, 85);
}
a::after{
    content:"";
    position:absolute;
    background-color:rgb(85, 85, 85);
    border-radius:0.3rem;
    width: 100%;
    height:2px;
    bottom: 0;
    left:0;
    transform-origin: center;
    transform:scaleX(0);
    transition:transform 200ms ease-in;
}

a:hover::after,
a:focus::after{
    transform:scalex(1);
    transform-origin:center;
    transition-duration: 200ms;
}
</style>
