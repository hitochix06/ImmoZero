<template>
  <div class="bg-[#E8EEF5] py-2 sm:py-4">
    <div class="mx-auto max-w-7xl px-1 lg:px-8">
      <div
        class="mx-auto mt-16 max-w-full rounded-3xl ring-1 ring-gray-200 sm:mt-20 lg:mx-0 flex flex-col lg:flex-row"
      >
        <div
          class="-mt-2 p-5 lg:mt-0 lg:w-auto lg:max-w-full lg:flex-shrink-0 h-auto flex-grow lg:flex-grow rounded-l-lg"
          style="background-color: #ffffff"
        >
          <div
            class="text-center ring-gray-900/5 lg:flex lg:flex-col lg:justify-center lg:py-16"
          >
            <form>
              <div class="mx-auto max-w-xs">
                <h1
                  class="text-2xl font-bold tracking-tight text-gray-900 sm:text-3xl"
                  style="color: rgb(0, 0, 0); text-transform: uppercase"
                >
                  Se connecter
                </h1>

                <div class="mt-6 flex items-baseline justify-center gap-x-2">
                  <label for="email-address"></label>
                  <input
                    id="email_address"
                    name="email"
                    type="email"
                    autocomplete="email"
                    class="min-w-0 flex-auto rounded-md border-2 px-3.5 py-2 text-gray-900 shadow-sm ring-1 ring-inset ring-white/10 focus:ring-2 focus:ring-inset focus:ring-indigo-500 sm:text-sm sm:leading-6 m-2"
                    placeholder="E-mai"
                    required
                  />
                </div>
                <div class="mt-6 flex items-baseline justify-center gap-x-2">
                  <label for="password"></label>
                  <input
                    id="password"
                    name="password"
                    type="password"
                    autocomplete="current-password"
                    class="min-w-0 flex-auto rounded-md border-2 px-3.5 py-2 text-gray-900 shadow-sm ring-1 ring-inset ring-white/10 focus:ring-2 focus:ring-inset focus:ring-indigo-500 sm:text-sm sm:leading-6 m-2"
                    placeholder="Mot de passe"
                  />
                </div>
                <div class="flex justify-end">
                  <a href="#" class="text-sm m-2" style="color: red">
                    Mots de passe oublié
                  </a>
                </div>
                <RouterLink
                  to="user"
                  class="mt-10 block w-full rounded-md bg-[#43B7BE] px-3 py-2 text-center text-sm font-semibold text-white shadow-sm hover:bg-indigo-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600"
                  style="text-transform: uppercase"
                  >Connexion
                </RouterLink>
              </div>
            </form>
          </div>
        </div>

        <!-- formulaire d'inscription -->
        <div
          class="-mt-2 p-2 lg:mt-0 lg:w-auto lg:max-w-full lg:flex-shrink-0 h-auto flex-grow lg:flex-grow rounded-r-lg"
          style="background-color: #143457"
        >
          <div
            class="text-center ring-gray-900/5 lg:flex lg:flex-col lg:justify-center lg:py-16"
          >
            <form>
              <div class="mx-auto max-w-xs">
                <h1
                  class="text-2xl font-bold tracking-tight text-gray-900 sm:text-3xl"
                  style="color: white"
                >
                  CRÉÉZ VOTRE COMPTE
                </h1>

                <p
                  class="mt-6 flex items-baseline justify-center gap-x-2"
                  style="color: white"
                >
                  Vous souhaitez passer une petite annonce immobilière de
                  particulier à particulier et gratuitement ?
                </p>
                <div class="mt-6 flex items-baseline justify-center gap-x-2">
                  <label for="email-address"></label>
                  <input
                    v-model="email"
                    id="email_address"
                    name="email"
                    type="email"
                    autocomplete="email"
                    class="min-w-0 flex-auto rounded-md border-0 px-3.5 py-2 text-gray-900 shadow-sm ring-1 ring-inset ring-white/10 focus:ring-2 focus:ring-inset focus:ring-indigo-500 sm:text-sm sm:leading-6 m-2"
                    placeholder="Adress e-mail"
                    required
                  />
                </div>
                <button
                  @click="handleClick"
                  type="button"
                  class="mt-10 block w-full rounded-md bg-[#43B7BE] px-3 py-2 text-center text-sm font-semibold text-white shadow-sm hover:bg-indigo-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600"
                >
                  <div style="text-transform: uppercase">C'est Parti !</div>
                </button>
              </div>
            </form>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- création du formulaire inscription modal -->
  <div class="container mx-auto">
    <div class="flex justify-center">
      <form
        v-show="isOpen"
        class="absolute inset-0 flex items-center justify-center bg-gray-700 bg-opacity-50"
      >
        <div class="w-full md:w-2/3 lg:w-3/5 p-6 bg-white rounded-md shadow-xl">
          <div class="flex items-center justify-between">
            <h3
              class="text-2xl"
              style="text-transform: uppercase; font-weight: 700"
            >
              Formulaire d'inscription
            </h3>
            <svg
              @click="isOpen = false"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 24 24"
              fill="currentColor"
              className="w-6 h-6 "
              width="30"
              height="30"
              style="cursor: pointer"
            >
              <path
                fillRule="evenodd"
                d="M5.47 5.47a.75.75 0 011.06 0L12 10.94l5.47-5.47a.75.75 0 111.06 1.06L13.06 12l5.47 5.47a.75.75 0 11-1.06 1.06L12 13.06l-5.47 5.47a.75.75 0 01-1.06-1.06L10.94 12 5.47 6.53a.75.75 0 010-1.06z"
                clipRule="evenodd"
              />
            </svg>
          </div>
          <div class="mt-4">
            <div class="mt-10 grid grid-cols-1 gap-x-6 gap-y-8 sm:grid-cols-6">
              <div class="sm:col-span-3">
                <div class="mt-2">
                  <label
                    for="first-name"
                    class="block text-sm font-medium leading-6 text-gray-900"
                    >NOM</label
                  >
                  <input
                    type="text"
                    name="first-name"
                    id="first-name"
                    autocomplete="given-name"
                    class="min-w-full flex-auto rounded-md border-2 px-3.5 py-2 text-gray-900 shadow-sm ring-1 ring-inset ring-white/10 focus:ring-2 focus:ring-inset focus:ring-indigo-500 sm:text-sm sm:leading-6 m-2"
                    placeholder="Titre"
                    required
                  />
                </div>
              </div>

              <div class="sm:col-span-3">
                <div class="mt-2">
                  <label for="email">Email</label>
                  <input
                    v-model="email"
                    type="email"
                    name="email"
                    id="email"
                    autocomplete="off"
                    class="min-w-full flex-auto rounded-md border-2 px-3.5 py-2 text-gray-900 shadow-sm ring-1 ring-inset ring-white/10 focus:ring-2 focus:ring-inset focus:ring-indigo-500 sm:text-sm sm:leading-6 m-2"
                    placeholder="Email"
                    required
                  />
                </div>
              </div>

              <div class="sm:col-span-3 py-2">
                <div class="mt-2">
                  <label
                    for="password"
                    class="block text-sm font-medium leading-6 text-gray-900"
                    >Mot de passe</label
                  >
                  <input
                    id="password"
                    name="password"
                    type="password"
                    autocomplete="off"
                    class="min-w-full flex-auto rounded-md border-2 px-3.5 py-2 text-gray-900 shadow-sm ring-1 ring-inset ring-white/10 focus:ring-2 focus:ring-inset focus:ring-indigo-500 sm:text-sm sm:leading-6 m-2"
                    placeholder="Mot de passe"
                    required
                  />
                </div>
              </div>
            </div>

            <button
              @click="isOpen = false"
              class="px-6 py-2 text-blue-800 border border-blue-600 rounded"
            >
              Annuler
            </button>
            <button class="px-6 py-2 ml-2 text-[#fff] bg-[#43B7BE] rounded">
              Ajouter
            </button>
          </div>
        </div>
      </form>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";
const isOpen = ref(false);
const email = ref(""); // Ajoutez cette ligne

// Ajoutez cette fonction
const resetEmail = () => {
  email.value = "";
};

const handleClick = () => {
  resetEmail();
  isOpen.value = true;
};
</script>
