<template>
<div class="list">
        <div class="list-image">
            <img :src="card.src" />
            <div class="wrap">
                <h2 class="text-title">{{ card.title }}</h2>
                <p>{{ card.date }}</p>
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
    justify-content: space-between;
    flex-wrap: wrap;
}
.list-image{
    display: block;
    margin:  0.5rem;
    width: 220px;
    box-shadow: 0px 2px 8px #ccc;
    border-radius: 5px;
}
.list-image img {
<<<<<<< HEAD
=======
    align-items: center;
>>>>>>> 5758163ac406b69b98f4a336e5a61e075e4d6c87
    height: 300px;
    width: 100%;
    border-radius: 5px 5px 0px 0px ;
}
.wrap {
    word-wrap: break-word;
    width: 150px;
    height: 80px;
}
.wrap p {
    margin-top: 5px;
    color: rgba(0,0,0,0.6);
}
</style>
