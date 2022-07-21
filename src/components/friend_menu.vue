<template>
    <ul>
        <li><a href="#">HOME</a></li>
        <li><a href="#">ABOUT US</a></li>
        <li><a href="#">SERVICES</a></li>
        <li><a href="#">HELP</a></li>
    </ul>
</template>


<script>
</script>

<style scoped>
body {
    background: black;
}
ul{
    display: flex;
    position: fixed;
    align-items: center;
    list-style: none;
    width: 100%;
    background: rgb(217, 96, 96);
    padding: 15px;
    z-index: 5;
}

li {
    margin: 10px;
}
a {
    font-family: sans-serif;
    text-decoration: none;
    color: #ffff;
    font-weight: bolder;
}
</style>
