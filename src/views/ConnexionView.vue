<template>
  <div class="fondecran h-screen">
    <section class="flex items-center justify-center h-full">
      <div class="w-3/4 lg:w-1/2">
        <div class="flex flex-wrap">
          <div
            class="w-full lg:w-1/2 p-4"
            style="background-color: white; border-radius: 37px 0px 0px 37px"
          >
            <form>
              <h1 class="mb-8 text-3xl text-center">Se Connecter</h1>
              <div class="mt-6 flex flex-col max-w-md gap-x-4">
                <label for="email-address"></label>
                <input
                  id="email-address"
                  name="email"
                  type="email"
                  autocomplete="email"
                  class="min-w-0 flex-auto rounded-md border-0 px-3.5 py-2 text-white shadow-sm ring-1 ring-inset ring-white/10 focus:ring-2 focus:ring-inset focus:ring-indigo-500 sm:text-sm sm:leading-6 m-2"
                  placeholder="Adress e-mail"
                />
                <label for="email-address"></label>
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
                  class="flex-none rounded-md bg-indigo-500 px-3.5 py-2.5 text-sm font-semibold text-white shadow-sm hover:bg-indigo-400 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-500 m-2"
                >
                  Connexion
                </button>
              </div>
            </form>
          </div>
          <div
            class="w-full lg:w-1/2 flex items-center justify-center text-center text-white p-4"
            style="background-color: #143457; border-radius: 0px 37px 37px 0px"
          >
            <div class="px-3 py-4 mx-4">
              <h1 class="mb-4 text-3xl">CRÉÉZ VOTRE COMPTE</h1>
              <h5>
                Vous souhaitez passer une petite annonce immobilière de
                particulier à particulier et gratuitement ?
              </h5>
              <div class="mt-6 flex flex-col max-w-md gap-x-4">
                <label for="email-address" class="sr-only">Email address</label>
                <input
                  id="email-address"
                  name="email"
                  type="email"
                  autocomplete="email"
                  class="min-w-0 flex-auto rounded-md border-0 px-3.5 py-2 text-white shadow-sm ring-1 ring-inset ring-white/10 focus:ring-2 focus:ring-inset focus:ring-indigo-500 sm:text-sm sm:leading-6 m-2"
                  placeholder="Adress e-mail"
                />
                <button
                  type="submit"
                  class="flex-none rounded-md bg-indigo-500 px-3.5 py-2.5 text-sm font-semibold text-white shadow-sm hover:bg-indigo-400 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-500 m-2"
                >
                  C'est Parti !
                </button>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>
<style>
.fondecran {
  background-color: #e8eef5;
}
.text-3xl {
  font-weight: 900;
}

.ring-white\/10 {
  --tw-ring-color: rgb(0 0 0 / 27%);
}
</style>
