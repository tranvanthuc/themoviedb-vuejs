<template>
<div class="list">
        <div class="list-image">
            <img :src="card.src" />
            <div class="wrap">
                <h2 class="text-title">{{ card.title }}</h2>
                <h2 class="text-date">{{ card.date }}</h2>
            </div>
        </div>
</div>
</template>

<script>
export default {
    name: 'List',
    props: ['card', 'index']
}
</script>

<style>
.container{
    display: flex;
    height: 430px;
    width: 100%;
    padding: 30px;
    justify-content: center;
}
.list-image{
    display: block;
    margin:  0.5rem;
    width: 75%;
    box-shadow: 0px 2px 8px #ccc;
    border-radius: 5px;
}
.list-image img {
    display: flex;
    align-items: center;
    height: 300px;
    width: 100%;
    border-radius: 5px;
}
.wrap {
    word-wrap: break-word;
    width: 150px;
}
</style>