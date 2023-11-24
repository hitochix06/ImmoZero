<template>
  <div class="py-3 px-1 fondimage">
    <div class="max-w-md mx-auto rounded-lg overflow-hidden md:max-w-xl">
      <div class="md:flex">
        <div class="w-full p-10">
          <h1
            class="text-3xl font-semibold text-white dark:text-white uppercase text-center py-5"
          >
            L'immoblier gratuit entre particuliers
          </h1>

          <div
            class="relative z-0 shadow-xl bg-white overflow-hidden rounded-lg"
          >
            <input
              type="search"
              id="search"
              v-model="searchValue"
              @input="search"
              class="block p-2.5 w-full z-20 text-sm text-gray-900 bg-gray-50 rounded-lg border-s-gray-50 border-s-2 border border-gray-300 focus:ring-blue-500 focus:border-blue-500 dark:bg-gray-700 dark:border-s-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:border-blue-500"
              placeholder="Recherchez dans vos annonces"
              required
            />
          </div>
          <div class="container mx-auto flex justify-center mt-10">
            <button
              @click="$router.push('/connexion')"
              type="button"
              class="text-white bg-[#43B7BE] hover:bg-[#3b5998]/90 focus:ring-4 focus:outline-none focus:ring-[#3b5998]/50 font-medium rounded-lg text-sm px-5 py-2.5 text-center inline-flex items-center dark:focus:ring-[#3b5998]/55 me-2 mb-2"
            >
              <div class="uppercase">Dépose une annonce</div>
            </button>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- Creation de carte pour les annonces -->
  <div class="bg-white">
    <div
      class="mx-auto max-w-2xl px-4 py-16 sm:px-6 sm:py-24 lg:max-w-7xl lg:px-8"
    >
      <h2 class="text-2xl font-bold tracking-tight text-gray-900">
        Notre Sélection
      </h2>
      <h3>Biens immobiliers à vendre de particulier à particulier</h3>

      <div class="mt-6 grid grid-cols-1 lg:grid-cols-2 gap-x-6 gap-y-10">
        <div
          v-for="item in data"
          :key="item.id"
          class="group relative shadow-xl bg-white overflow-hidden rounded-lg"
        >
          <!-- code gere image -->
          <div
            class="aspect-h-1 aspect-w-1 w-full overflow-hidden rounded-md bg-gray-200 lg:aspect-none lg:h-60"
          >
            <img
              src="https://cf.bstatic.com/xdata/images/hotel/max1024x768/295090917.jpg?k=d17621b71b0eaa0c7a37d8d8d02d33896cef75145f61e7d96d296d88375a7d39&o=&hp=1"
              class="h-full w-full object-cover object-center lg:h-full lg:w-full"
            />
          </div>
          <div class="mt-4 flex justify-between">
            <div>
              <h1 class="text-lg text-black-900 m-5">
                {{ item.title }}
              </h1>
              <p class="mt-1 text-sm text-black-900 m-5">
                {{ item.description }}
              </p>
              <p class="mt-1 text-sm m-5 uppercase text-gray-900">
                {{ item.location }}
              </p>
            </div>
            <p class="text-lg font-medium m-5 text-gray-900">
              {{ item.price }}€
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- sections -->
  <div
    class="py-3 bg-[#E8EEF5] flex flex-col md:flex-row justify-center items-center"
  >
    <div class="w-full md:w-1/2 flex justify-center px-5 py-4">
      <img
        src="../../assets/images/image1.jpg"
        alt="Image description"
        class="w-full md:w-3/4 rounded-lg"
      />
    </div>
    <div class="w-full md:w-1/2 flex flex-col md:text-left px-4">
      <h4>Un site immobilier de particulier à particulier !</h4>
      <p>
        Contrairement aux autres portails
        <span>
          immobiliers, ImmoZero est un site gratuit uniquement destiné aux
          particuliers.</span
        >
        Aucune agence n'est tolérée afin que propriétaires et futurs acheteurs y
        trouvent tous leur intérêt financier : pas de frais d'agence et des
        affaires de particulier à particulier !
      </p>
    </div>
  </div>
</template>

<style scoped>
.fondimage {
  background-image: url("../../assets/images/fondecran.png");
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  background-attachment: fixed;
  height: 50vh;
}
</style>

<script setup>
import { ref, onMounted } from "vue";
import axios from "axios";

const data = ref("");

// barre de recherche
const searchValue = ref("");

// fonction de recherche
const search = async () => {
  try {
    const token = localStorage.getItem("token");
    const response = await axios.get(
      "https://apihackaton1.osc-fr1.scalingo.io/properties",
      {
        headers: {
          Authorization: `Bearer ${token}`,
        },
      }
    );
    data.value = response.data.filter(
      (item) =>
        item.title.includes(searchValue.value) ||
        item.description.includes(searchValue.value) ||
        item.location.includes(searchValue.value) ||
        item.price.toString().includes(searchValue.value)
    );
  } catch (error) {
    console.error("Erreur lors de la recherche: ", error);
  }
};

onMounted(async () => {
  try {
    const response = await axios.get(
      "https://apihackaton1.osc-fr1.scalingo.io/properties"
    );
    data.value = response.data.filter(
      (item) =>
        item.title.includes(searchValue.value) ||
        item.description.includes(searchValue.value) ||
        item.location.includes(searchValue.value) ||
        item.price.toString().includes(searchValue.value)
    );
    console.log(data.value);
  } catch (error) {
    console.error("Erreur lors de la récupération des annonces: ", error);
  }
});
</script>
