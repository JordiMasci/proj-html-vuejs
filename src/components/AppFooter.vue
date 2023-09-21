<script>
export default {
  data() {
    return {
      column2Items: [
        "Contact Us",
        "Online Chat",
        "Whatsapp",
        "Telegram",
        "Snapchat",
      ],
      column3Items: ["About Us", "Blog", "Career", "Job", "In press"],
      column4Items: ["Account", "Order", "Delivery", "Payment", "Return"],
      column5Items: [
        "4500 Mercantile plaza, suite 300,fort worth,TX,76137,USA",
        "+1(817)901 3377",
        "info@example.com",
      ],
      iconClasses: ["fas fa-envelope", "fas fa-phone", "fas fa-location-arrow"],
    };
  },

  methods: {
    getIconByIndex(index) {
      const icons = ["location-arrow", "phone", "envelope"];
      return ["fas", icons[index]];
    },
    getLinkByIndex(index) {
      // Sostituire con l'URL reale
      if (index === 0) {
        return "/pagina1";
      } else if (index === 1) {
        return "/pagina2";
      } else if (index === 2) {
        return "/pagina3";
      } else if (index === 3) {
        return "/pagina4";
      } else if (index === 4) {
        return "/pagina5";
      }
    },
  },
};
</script>

<template>
  <footer class="d-flex align-items-center">
    <div class="container">
      <div class="row">
        <!-- Colonna 1 -->
        <div class="col-3">
          <h4>Get In Touch</h4>
          <p>Have a question for us? we'll answer your problem here</p>
          <font-awesome-icon :icon="['fab', 'facebook']" class="fa-icon" />
          <font-awesome-icon :icon="['fab', 'twitter']" class="fa-icon" />
          <font-awesome-icon :icon="['fab', 'instagram']" class="fa-icon" />
          <font-awesome-icon :icon="['fab', 'linkedin']" class="fa-icon" />
          <font-awesome-icon :icon="['fab', 'facebook']" class="fa-icon" />
        </div>

        <!-- Colonna 2 -->
        <div class="col-2">
          <h4>Support</h4>
          <ul>
            <li v-for="(item, index) in column2Items" :key="index">
              <a :href="getLinkByIndex(index)">{{ item }}</a>
            </li>
          </ul>
        </div>

        <!-- Colonna 3 -->
        <div class="col-2">
          <h4>About</h4>
          <ul>
            <li v-for="(item, index) in column3Items" :key="index">
              <a :href="getLinkByIndex(index)">{{ item }}</a>
            </li>
          </ul>
        </div>

        <!-- Colonna 4 -->
        <div class="col-2">
          <h4>Faq</h4>
          <ul>
            <li v-for="(item, index) in column4Items" :key="index">
              <a :href="getLinkByIndex(index)">{{ item }}</a>
            </li>
          </ul>
        </div>

        <!-- Colonna 5 -->
        <div class="col-3">
          <h4>Contact Me</h4>
          <ul>
            <li v-for="(item, index) in column5Items" :key="index" class="mb-3">
              <font-awesome-icon :icon="getIconByIndex(index)" class="icon" />
              {{ item }}
            </li>
          </ul>
        </div>
      </div>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
footer {
  background-color: black;
  color: white;
  min-height: 500px;

  a {
    color: inherit;
    text-decoration: none;
  }

  h4 {
    margin-bottom: 25px;
    color: #cc7c2b;
  }

  ul {
    padding: 0;
    margin: 0;

    li {
      line-height: 2;
      list-style: none;

      .icon {
        color: #cc7c2b;
        margin-right: 8px;
      }
    }
  }
}
</style>
