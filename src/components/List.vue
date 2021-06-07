<template>
<div class="list">
    <div class="list-image">
        <img :src="card.src" />
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

</style>