<template>
    <body>
        <div class="flex">
            <!-- Coluna da esquerda - Carrossel -->
            <div class="w-1/2">

                <!-- Coloque o conteúdo do carrossel aqui -->
                <banner-esquerdo>

                </banner-esquerdo>
            </div>

            <!-- Coluna da direita - Formulário -->
            <div class=" cores w-1/2 p-8">
                <div class="text-center">
                    <h1 class="text-2xl font-bold mb-4">Podes fazer a sua requisição preencha os campos</h1>
                </div>
                <form @submit="criaCliete">
                    <div class="space-y-12" id="form11">
                        <!-- o campo de usuário -->

                        <div class="mt-10 grid grid-cols-1 gap-x-6 gap-y-8 sm:grid-cols-6">
                            <div class="sm:col-span-2 sm:col-start-1">
                                <label for="nome" class="block text-sm font-medium leading-6 text-gray-900">Nome /
                                    Empresa*</label>
                                <div class="mt-2">
                                    <input type="text" name="nome" v-model="nome" id="nome" autocomplete="nome"
                                        class="block w-full rounded-md border-0 py-1.5 text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-indigo-600 sm:text-sm sm:leading-6" />
                                </div>
                            </div>
                            <div class="sm:col-span-2">
                                <label for="email" class="block text-sm font-medium leading-6 text-gray-900">Email*</label>
                                <div class="mt-2">
                                    <input type="email" name="email" v-model="email" id="email" autocomplete="email"
                                        class="block w-full rounded-md border-0 py-1.5 text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-indigo-600 sm:text-sm sm:leading-6" />
                                </div>
                            </div>
                            <div class="sm:col-span-2">
                                <label for="contacto"
                                    class="block text-sm font-medium leading-6 text-gray-900">Contacto*</label>
                                <div class="mt-2">
                                    <input type="contacto" name="contacto" id="contacto" autocomplete="contacto"
                                        class="block w-full rounded-md border-0 py-1.5 text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-indigo-600 sm:text-sm sm:leading-6" />
                                </div>
                            </div>
                            <div class="sm:col-span-2 sm:col-start-1">
                                <label for="data" class="block text-sm font-medium leading-6 text-gray-900">Data a
                                    Requisitar*</label>
                                <div class="mt-2">
                                    <input type="date" name="data" id="data" autocomplete="data"
                                        class="block w-full rounded-md border-0 py-1.5 text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-indigo-600 sm:text-sm sm:leading-6" />
                                </div>
                            </div>
                            <div class="sm:col-span-2">
                                <label for="Local" class="block text-sm font-medium leading-6 text-gray-900">Local de
                                    partida*</label>
                                <div class="mt-2">
                                    <input type="text" name="Local" id="Local" autocomplete="Local"
                                        class="block w-full rounded-md border-0 py-1.5 text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-indigo-600 sm:text-sm sm:leading-6" />
                                </div>
                            </div>
                            <div class="sm:col-span-2">
                                <label for="destino" class="block text-sm font-medium leading-6 text-gray-900">Destino
                                    da
                                    Viatura*</label>
                                <div class="mt-2">
                                    <input type="text" name="destino" id="destino" autocomplete="destino"
                                        class="block w-full rounded-md border-0 py-1.5 text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-indigo-600 sm:text-sm sm:leading-6" />
                                </div>
                            </div>
                            <div class="sm:col-span-2 sm:col-start-1">
                                <label for="passageiros" class="block text-sm font-medium leading-6 text-gray-900">Nº de
                                    Passageiros*</label>
                                <div class="mt-2">
                                    <input type="text" name="passageiros" id="passageiros" autocomplete="passageiros"
                                        class="block w-full rounded-md border-0 py-1.5 text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-indigo-600 sm:text-sm sm:leading-6" />
                                </div>
                            </div>
                            <div class="sm:col-span-2">
                                <label for="estimativa" class="block text-sm font-medium leading-6 text-gray-900">Estimativa
                                    Entrega*</label>
                                <div class="mt-2">
                                    <input type="date" name="estimativa" id="estimativa" autocomplete="estimativa"
                                        class="block w-full rounded-md border-0 py-1.5 text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-indigo-600 sm:text-sm sm:leading-6" />
                                </div>
                            </div>
                            <div class="sm:col-span-2">
                                <label for="partida" class="block text-sm font-medium leading-6 text-gray-900">Horas
                                    de Partida Viatura*</label>
                                <div class="mt-2">
                                    <input type="day" name="partida" id="partida" autocomplete="partida"
                                        class="block w-full rounded-md border-0 py-1.5 text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-indigo-600 sm:text-sm sm:leading-6" />
                                </div>
                            </div>
                            <div class="sm:col-span-3">
                                <label for="first-name" class="block text-sm font-medium leading-6 text-gray-900">Horas
                                    de Entrega Viatura*</label>
                                <div class="mt-2">
                                    <input type="text" name="first-name" id="first-name" autocomplete="given-name"
                                        class="block w-full rounded-md border-0 py-1.5 text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-indigo-600 sm:text-sm sm:leading-6" />
                                </div>
                            </div>
                        </div>
                        <div class="border-b border-gray-900/10 pb-12">
                            <div class="mt-10 grid grid-cols-1 gap-x-6 gap-y-8 sm:grid-cols-6">
                                <div class="col-span-full">
                                    <label for="about"
                                        class="block text-sm font-medium leading-6 text-gray-900">Menssagem</label>
                                    <div class="mt-2">
                                        <textarea id="about" name="about" rows="3"
                                            placeholder="Nao tem a viatura que desjejas, lista aqui."
                                            class="block w-full rounded-md border-0 py-1.5 text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-indigo-600 sm:text-sm sm:leading-6"></textarea>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div>
                        <button type="submit" id="btn11"
                            class="btn flex w-full justify-center rounded-md bg-indigo-600 px-3 py-1.5 text-sm font-semibold leading-6 text-white shadow-sm hover:bg-indigo-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600">Submeter</button>
                        <p class="mt-3 text-sm leading-6 text-gray-600 flex justify-center">Todos campos com (*) são
                            obrigatórios.</p>
                    </div>
                </form>
            </div>
        </div>
    </body>
</template>
<script setup>
import { ref } from "vue";
import { ChevronDownIcon } from "@heroicons/vue/20/solid";
import { Switch, SwitchGroup, SwitchLabel } from "@headlessui/vue";


const agreed = ref(false);
</script>

<script>
import BannerEsquerdo from "../carrousel/BannerEsquerdo.vue";

export default {
    name: "ConteudoDireito",
    components: {
        BannerEsquerdo
    },
    data() {
        return {
            images: ["/img/banner.jpg"],
        };

    },
    data() {
        return {
            nome: '',
            email: '',
            contacto: '',
            data: '',
            local: '',
            destino: '',
            passageiros: '',
            estimativa: '',
            partida: '',
            firstName: '',
            about: ''
        }
    },
    methods: {
        async criaCliete(e) {
            e.preventDefault();
            const data = {
                nome: this.nome,
                email: this.email,
                contacto: this.contacto,
                data_requisica: this.data_requisica,
                local_partida: this.local_partida,
                destino_viatura: this.destino_viatura,
                passageiro: this.passageiro,
                estimativa_entrega: this.estimativa_entrega,
                horas_partida: this.horas_partida,
                horas_entrega: this.horas_entrega,
                menssage: this.menssage
            }
            console.log(data);
        }
    },
    data: () => ({
        slides: [
            "https://picsum.photos/633/600?blur",
            "https://picsum.photos/633/600?grayscale",
            "https://picsum.photos/633/600?blur",
            "https://picsum.photos/633/600",
            "/img/banner.jpg",
        ],
    }),
};
// aqui slide
</script>

<style scoped>
/*.bodes {
    display: flex;
    flex-direction: column;
    height: 100%;
}
*/
.texto {
    background-color: #fff;

    /* or 97% */
    display: flex;
    color: #f68e13;
    padding: 20px;
}

.cores {
    background-color: #f68e13;
}

h1 {
    font-family: "Rubik";
    font-style: normal;
    font-weight: 900;
    font-size: 32px;
    line-height: 31px;
    text-align: center;
    letter-spacing: -0.005em;
}

.direita {
    background-color: #f68e13;

}

.btn {
    background-color: #626b36;
}

#form11 {
    margin: auto 21px auto 25px;
}

p,
label {
    color: #fff;
}

input,
textarea {
    background-color: #e9d3d3;
    border-radius: 0;
}

textarea {
    margin-bottom: -15px;
}

button {
    background: #626b36;
    border-radius: 42px;

    width: 253px;
    margin-bottom: -10px;
}

#btn11 {
    margin-left: 30%;

}

#btn11:hover {
    background-color: #0c1f38;
    color: #fff;
}

.nova {
    height: 100%;
}
</style>
