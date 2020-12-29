<template>
    <div class="screen">
        <kinesis-container tag="div" class="screen__container">
            <kinesis-element
                tag="img"
                class="screen__parallax"
                :strength="40"
                :src="require('@/assets/parallax.png')"
                alt="parallax"
            />

            <p class="screen__text">
                Place mouse cursor inside container on initial page load.
                Parallax starts working only when cursor leaves container.
            </p>
        </kinesis-container>
    </div>
</template>

<script>
export default {
    data() {
        return {
            parallax: true,
        };
    },
};
</script>

<style scoped>
.screen {
    margin: 0 auto;
    min-height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
}

.screen__container {
    width: 90vw;
    height: 90vh;
    border: 1px solid #333;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    position: relative;
}

.screen__container:before {
    content: 'vue-kinesis container';
    position: absolute;
    top: 10px;
    left: 10px;
}

.screen__parallax {
    width: 100%;
    height: 100%;
    object-fit: contain;
}

.screen__text {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    width: 100%;
    max-width: 430px;
}
</style>
