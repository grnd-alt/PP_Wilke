<template>
<div>
    <h1>Anscheinend hast du dich verlaufen</h1>
    <h2><router-link to="/">Hier</router-link> geht es wieder in bekannte Gewässer</h2>
</div>
</template>
<style scoped>
p,h1{
    color:var(--maincolor);
}
a{
    text-decoration: none;
    color:var(--maincolor);
    cursor: pointer;
    position: relative;
}
a::after{
    content:"";
    position:absolute;
    background-color:var(--maincolor);
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
    z-index:-1;
}
</style>
