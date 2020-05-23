<template>
  <div class="w3-container w3-black w3-padding-64 w3-xxlarge" id="menu">
    <div class="w3-content">
      <h1 class="w3-center w3-jumbo" style="margin-bottom:64px">THE MENU</h1>
      <div class="w3-row w3-center w3-border w3-border-dark-grey">
        <a id="myLink" @click="change('Pizza') ">
          <div class="w3-col s4 tablink w3-padding-large w3-hover-red">Pizza</div>
        </a>
        <a @click="change('Pasta') ">
          <div class="w3-col s4 tablink w3-padding-large w3-hover-red">Pasta</div>
        </a>
        <a @click="change('Starter') ">
          <div class="w3-col s4 tablink w3-padding-large w3-hover-red">Starter</div>
        </a>
      </div>

      <div
        id="Pizza"
        v-bind:style="{ display: v1 }"
        class="w3-container menu w3-padding-32 w3-white"
      >
        <h1>
          <b>Margherita</b>
          <span class="w3-right w3-tag w3-dark-grey w3-round">$12.50</span>
        </h1>
        <p class="w3-text-grey">Fresh tomatoes, fresh mozzarella, fresh basil</p>
        <hr />

        <h1>
          <b>Formaggio</b>
          <span class="w3-right w3-tag w3-dark-grey w3-round">$15.50</span>
        </h1>
        <p class="w3-text-grey">Four cheeses (mozzarella, parmesan, pecorino, jarlsberg)</p>
        <hr />

        <h1>
          <b>Chicken</b>
          <span class="w3-right w3-tag w3-dark-grey w3-round">$17.00</span>
        </h1>
        <p class="w3-text-grey">Fresh tomatoes, mozzarella, chicken, onions</p>
        <hr />

        <h1>
          <b>Pineapple'o'clock</b>
          <span class="w3-right w3-tag w3-dark-grey w3-round">$16.50</span>
        </h1>
        <p class="w3-text-grey">Fresh tomatoes, mozzarella, fresh pineapple, bacon, fresh basil</p>
        <hr />

        <h1>
          <b>Meat Town</b>
          <span class="w3-tag w3-red w3-round">Hot!</span>
          <span class="w3-right w3-tag w3-dark-grey w3-round">$20.00</span>
        </h1>
        <p
          class="w3-text-grey"
        >Fresh tomatoes, mozzarella, hot pepporoni, hot sausage, beef, chicken</p>
        <hr />

        <h1>
          <b>Parma</b>
          <span class="w3-tag w3-grey w3-round">New</span>
          <span class="w3-right w3-tag w3-dark-grey w3-round">$21.50</span>
        </h1>
        <p class="w3-text-grey">Fresh tomatoes, mozzarella, parma, bacon, fresh arugula</p>
      </div>

      <div
        id="Pasta"
        v-bind:style="{ display: v2 }"
        class="w3-container menu w3-padding-32 w3-white"
      >
        <h1>
          <b>Lasagna</b>
          <span class="w3-tag w3-grey w3-round">Popular</span>
          <span class="w3-right w3-tag w3-dark-grey w3-round">$13.50</span>
        </h1>
        <p class="w3-text-grey">Special sauce, mozzarella, parmesan, ground beef</p>
        <hr />

        <h1>
          <b>Ravioli</b>
          <span class="w3-right w3-tag w3-dark-grey w3-round">$14.50</span>
        </h1>
        <p class="w3-text-grey">Ravioli filled with cheese</p>
        <hr />

        <h1>
          <b>Spaghetti Classica</b>
          <span class="w3-right w3-tag w3-dark-grey w3-round">$11.00</span>
        </h1>
        <p class="w3-text-grey">Fresh tomatoes, onions, ground beef</p>
        <hr />

        <h1>
          <b>Seafood pasta</b>
          <span class="w3-right w3-tag w3-dark-grey w3-round">$25.50</span>
        </h1>
        <p class="w3-text-grey">Salmon, shrimp, lobster, garlic</p>
      </div>

      <div
        id="Starter"
        v-bind:style="{ display: v3 }"
        class="w3-container menu w3-padding-32 w3-white"
      >
        <h1>
          <b>Today's Soup</b>
          <span class="w3-tag w3-grey w3-round">Seasonal</span>
          <span class="w3-right w3-tag w3-dark-grey w3-round">$5.50</span>
        </h1>
        <p class="w3-text-grey">Ask the waiter</p>
        <hr />

        <h1>
          <b>Bruschetta</b>
          <span class="w3-right w3-tag w3-dark-grey w3-round">$8.50</span>
        </h1>
        <p class="w3-text-grey">Bread with pesto, tomatoes, onion, garlic</p>
        <hr />

        <h1>
          <b>Garlic bread</b>
          <span class="w3-right w3-tag w3-dark-grey w3-round">$9.50</span>
        </h1>
        <p class="w3-text-grey">Grilled ciabatta, garlic butter, onions</p>
        <hr />

        <h1>
          <b>Tomozzarella</b>
          <span class="w3-right w3-tag w3-dark-grey w3-round">$10.50</span>
        </h1>
        <p class="w3-text-grey">Tomatoes and mozzarella</p>
      </div>
      <br />
    </div>
  </div>
</template>
<style scoped>
</style>
<script>
export default {
  data() {
    return {
      v1: "block",
      v2: "none",
      v3: "none"
    };
  },
  methods: {
    change: function(val) {
      switch (val) {
        case "Pizza":
          this.v1 = "block";
          this.v2 = "none";
          this.v3 = "none";
          break;
        case "Pasta":
          this.v1 = "none";
          this.v2 = "block";
          this.v3 = "none";
          break;
        case "Starter":
          this.v1 = "none";
          this.v2 = "none";
          this.v3 = "block";
          break;
      }
    }
  }
};
</script>

