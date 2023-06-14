<template>
    <div class="flex">
        <!-- Coluna da esquerda - Carrossel -->
        <div class="w-1/2">
            <!-- Coloque o conteúdo do carrossel aqui -->
            <!-- <banner-esquerdo :slides="slides"></banner-esquerdo> -->
        </div>

        <!-- Coluna da direita - Formulário -->
        <div class="w-1/2 p-8">
            <div class="text-center">
                <h1 class="text-2xl font-bold mb-4">Podes fazer a sua requisição preencha os campos</h1>
            </div>

            <form @submit="criaCliente">
                <!-- Campos do formulário aqui -->
            </form>
        </div>
    </div>
</template>

<script setup>


const slides = ref([
    "https://picsum.photos/633/600?blur",
    "https://picsum.photos/633/600?grayscale",
    "https://picsum.photos/633/600?blur",
    "https://picsum.photos/633/600",
    "/img/banner.jpg",
]);

const criaCliente = (e) => {
    e.preventDefault();
    // Lógica para criar cliente
};
</script>
