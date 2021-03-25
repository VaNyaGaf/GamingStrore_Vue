<template>
    <div class="list-wrapper">
    <div :key="game.id" v-for="game in games" class="list-item">
        <div class="img">
            <img :src="game.imgPath" alt="Image not provided">
        </div>
        <div class="info">
            <div class="title">{{game.title}}</div>
            <div class="description">{{game.description}}</div>
            <div class="footer">
                {{game.price}}
            </div>
        </div>
    </div>
</div>

</template>

<script>

export default {
    name: 'GameList',
    props: {
        games: Array
    }
}
</script>

<style scoped>

.list-wrapper {
    margin: 0 auto;
    width: 64%;
}

.list-item {
    display: flex;
    margin: 8px 0 8px 0;
    border: 1px solid black;
    transition: 0.2s;
}

.list-item:hover {
    box-shadow: 10px 5px 5px #aaa;
}

.list-item .img {
    width: 20%;
    border: 1px solid red;
    display: flex;
}

.list-item .img img {
    width: 100%;
}

.list-item .info {
    display: flex;
    flex-direction: column;
    width: 80%;
    border: 1px solid blue;
    padding: 5px;
}

.list-item .info .title {
    font-size: 1.4rem;
    font-weight: bold;
}

</style>