<script setup>
import { ref } from 'vue'

</script>

<template>
    <div class="bodyfeed">
        <img src="https://picsum.photos/300/300" alt="Imagen obtenida de manera aleatoria" />
        <img src="https://picsum.photos/301/301" alt="Imagen obtenida de manera aleatoria" />
        <img src="https://picsum.photos/302/302" alt="Imagen obtenida de manera aleatoria" />
        <img src="https://picsum.photos/303/303" alt="Imagen obtenida de manera aleatoria" />
        <img src="https://picsum.photos/304/304" alt="Imagen obtenida de manera aleatoria" />
        <img src="https://picsum.photos/305/305" alt="Imagen obtenida de manera aleatoria" />
        <img src="https://picsum.photos/306/306" alt="Imagen obtenida de manera aleatoria" />
        <img src="https://picsum.photos/307/307" alt="Imagen obtenida de manera aleatoria" />
        <img src="https://picsum.photos/308/308" alt="Imagen obtenida de manera aleatoria" />
        <img src="https://picsum.photos/309/309" alt="Imagen obtenida de manera aleatoria" />
        <img src="https://picsum.photos/310/310" alt="Imagen obtenida de manera aleatoria" />
        <img src="https://picsum.photos/311/311" alt="Imagen obtenida de manera aleatoria" />
        <img src="https://picsum.photos/312/312" alt="Imagen obtenida de manera aleatoria" />
        <img src="https://picsum.photos/313/313" alt="Imagen obtenida de manera aleatoria" />
        <img src="https://picsum.photos/314/314" alt="Imagen obtenida de manera aleatoria" />
    </div>
</template>

<script>

// function imageDetail(event) {
//     const imgClicked = event.target
//     imgClicked.classList.add('img-detail')
// }

</script>

<style scoped>
.bodyfeed {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-gap: 10px;
    grid-auto-rows: minmax(100px, auto);
    border-top: 1px solid rgb(160, 156, 142);
    padding-top: 10px;
}

img {
    width: 300px;
    height: 300px;
    border-radius: 5px;
    cursor: pointer;
    transition: filter 0.1s, transform 0.1s;
}

img:hover {
    transform: scale(1.02, 1.02);;
    filter: brightness(50%)
}

.img-detail {
    width: 400px;
    height: 400px;
    position: absolute;
}

@media (width < 1000px) {
    .bodyfeed {
        grid-gap: 5px;
    }
    img {
        width: 30vw;
        height: 30vw;
    }
}

</style>