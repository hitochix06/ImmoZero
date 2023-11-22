<template>
  <div class="fondecran py-24 sm:py-32">
    <div class="mx-auto max-w-7xl px-6 lg:px-8">
      <div
        class="mx-auto mt-16 max-w-2xl rounded-3xl ring-1 ring-gray-200 sm:mt-20 lg:mx-0 lg:flex lg:max-w-none"
      >
        <div
          class="p-8 sm:p-10 lg:flex-auto"
          style="background-color: white; border-radius: 37px 0px 0px 37px"
        >
          <h1
            class="text-2xl font-bold tracking-tight text-gray-900 sm:text-3xl text-center"
          >
            SE CONNECTER
          </h1>
          <form>
            <div class="mt-6 flex flex-col max-w-md gap-x-4">
              <label for="email-address"></label>
              <input
                id="email_address"
                name="email"
                type="email"
                autocomplete="email"
                class="min-w-0 flex-auto rounded-md border-0 px-3.5 py-2 text-white shadow-sm ring-1 ring-inset ring-white/10 focus:ring-2 focus:ring-inset focus:ring-indigo-500 sm:text-sm sm:leading-6 m-2"
                placeholder="Adress e-mail"
              />
              <label for="passeword"></label>
              <input
                id="Mots de passe"
                name="Mots de passe"
                type="Mots de passe"
                autocomplete="Mots de passe"
                class="min-w-0 flex-auto rounded-md border-0 px-3.5 py-2 text-white shadow-sm ring-1 ring-inset ring-white/10 focus:ring-2 focus:ring-inset focus:ring-indigo-500 sm:text-sm sm:leading-6 m-2"
                placeholder="Mots de passe"
              />
              <p class="text-right text-sm m-2" style="color: red">
                Mots de passe oublié
              </p>
              <button
                type="submit"
                class="flex-none rounded-md bg-indigo-600 px-3.5 py-2.5 text-sm font-semibold text-white shadow-sm hover:bg-indigo-400 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-500 m-2"
              >
                Connexion
              </button>
            </div>
          </form>
        </div>
        <div
          class="-mt-2 p-2 lg:mt-0 lg:w-full lg:max-w-md lg:flex-shrink-0"
          style="background-color: #143457; border-radius: 0px 37px 37px 0px"
        >
          <div
            class="text-center ring-gray-900/5 lg:flex lg:flex-col lg:justify-center lg:py-16"
          >
            <div class="mx-auto max-w-xs px-8">
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
              <label for="email-address"></label>
              <input
                id="email_address"
                name="email"
                type="email"
                autocomplete="email"
                class="min-w-0 flex-auto rounded-md border-0 px-3.5 py-2 text-white shadow-sm ring-1 ring-inset ring-white/10 focus:ring-2 focus:ring-inset focus:ring-indigo-500 sm:text-sm sm:leading-6 m-2"
                placeholder="Adress e-mail"
              />
              <a
                href="#"
                class="mt-10 block w-full rounded-md bg-indigo-600 px-3 py-2 text-center text-sm font-semibold text-white shadow-sm hover:bg-indigo-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600"
                >C'est Parti !</a
              >
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style>
.fondecran {
  background-color: #e8eef5;
}
.bg-indigo-600 {
  background-color: #43b7be;
}
</style>

<script setup></script>
