<template>
  <nav>
    <div class="px-4 py-4 w-full flex item-center justify-between">
      <div class="flex item-center">
        <button
          class="hover:bg-light flex item-center justify-center p-3 rounded-full"
        >
          <img src="../assets/logo.png" alt="logo" class="h-6 w-6" />
        </button>
        <button
          v-for="btn in buttons"
          :key="btn.key"
          :class="`${
            selectedBtn === btn.key
              ? 'bg-dark text-white'
              : 'text-dark hover:bg-light'
          } font-semibold px-4 ml-1 mr-1 py-2 rounded-full`"
        >
          {{ btn.name }}
        </button>
      </div>
      <div class="flex-grow ml-4 mr-5">
        <span class="material-icons absolute mt-3 ml-3 text-muted">search</span>
        <input
          type="text"
          placeholder="Search"
          class="text-muted w-full pl-10 rounded-full hover:bg-lightHover bg-light p-3"
        />
      </div>
      <div class="flex item-center">
        <button
          class="hover:bg-light flex item-center justify-center p-3 rounded-full"
        >
          <span class="material-icons">notifications</span>
        </button>
        <button
          class="hover:bg-light flex item-center justify-center p-3 rounded-full"
        >
          <span class="material-icons">textsms</span>
        </button>
        <button
          class="hover:bg-light flex item-center justify-center p-3 rounded-full"
        >
          <v-avatar color="green" size="25">
            <span class="white--text caption">B</span>
          </v-avatar>
        </button>

        <button
          class="hover:bg-light flex item-center justify-center p-3 rounded-full"
        >
          <v-expansion-panels>
            <v-expansion-panel >
           <v-expansion-header>
           <span class="material-icons">expand_more</span>
           </v-expansion-header>
              <v-expansion-panel-content>
                Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
                eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut
                enim ad minim veniam, quis nostrud exercitation ullamco laboris
                nisi ut aliquip ex ea commodo consequat.
              </v-expansion-panel-content>
            </v-expansion-panel>
          </v-expansion-panels>
        </button>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      buttons: [
        { name: "Home", key: "home" },
        { name: "Create", key: "create" },
      ],
      selectedBtn: "home",
    };
  },
};
</script>

<style></style>
