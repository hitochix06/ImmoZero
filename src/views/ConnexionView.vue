<template>
  <div class="fondecran py-24 sm:py-32">
    <div class="mx-auto max-w-7xl px-6 lg:px-8">
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
                    id="email_address"
                    name="email"
                    type="email"
                    autocomplete="email"
                    class="min-w-0 flex-auto rounded-md border-0 px-3.5 py-2 text-gray-900 shadow-sm ring-1 ring-inset ring-white/10 focus:ring-2 focus:ring-inset focus:ring-indigo-500 sm:text-sm sm:leading-6 m-2"
                    placeholder="Adress e-mail"
                    required
                  />
                </div>
                <a
                  href="#"
                  class="mt-10 block w-full rounded-md bg-[#43B7BE] px-3 py-2 text-center text-sm font-semibold text-white shadow-sm hover:bg-indigo-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600"
                  style="text-transform: uppercase"
                  >C'est Parti !</a
                >
              </div>
            </form>
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
</style>

<script setup></script>
