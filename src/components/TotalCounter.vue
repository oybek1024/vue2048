<template>
    <div class="actions">
        <div class="stats">
            <div class="score">Score: {{ info.score }}</div>
        </div>
        <div class="buttons">
            <button class="btn" v-if="info.gameState !== 'RUNNING'" @click="startGame">Start Game</button>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        info: { numMoves: Number, highest: Number, score: Number, gameState: String, timeDiff: Number },
    },
    methods: {
        startGame() {
            this.$emit("startGame");
        },
    },
};
</script>
<style scoped lang="scss">

.actions {
    display: flex;
    flex-direction: column;
    width: 100%;

    .stats {
        --font-size: 1.2em;

        display: flex;
        justify-content: space-between;
        flex-wrap: wrap;

        .score {
            padding: 10px;
            font-size: var(--font-size);
            font-weight: bold;
            line-height: 2em;
        }
    }

    .buttons {
        display: flex;
        justify-content: flex-end;
        margin: 10px 0;
    }

    .btn {
        color: white;
        background-color: yellowgreen;
        padding: 10px 30px;
        font-size: 12px;
        
    }
}

@media screen and (min-width: 355px) and (max-width: 499px) {
    .actions .stats {
        --font-size: 1em;
    }
}
</style>
