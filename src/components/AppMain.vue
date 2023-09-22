<script>
import Card from "./Card.vue";

export default {
  components: {
    Card,
  },
  data() {
    return {
      cardData: [
        {
          id: 1,
          imageSrc: "../../public/img/d-1.png",
          title: "Pet sitting",
          text: "The readable content of page when looking at its layout.",
        },
        {
          id: 2,
          imageSrc: "../../public/img/d-2.png",
          title: "Puppy Sitting",
          text: "The readable content of page when looking at its layout.",
        },
        {
          id: 2,
          imageSrc: "../../public/img/d-3.png",
          title: "Dog Walking",
          text: "The readable content of page when looking at its layout.",
        },
        {
          id: 2,
          imageSrc: "../../public/img/d-4.png",
          title: "Night Care",
          text: "The readable content of page when looking at its layout.",
        },
        {
          id: 2,
          imageSrc: "../../public/img/d-5.png",
          title: "Pet Sitting",
          text: "The readable content of page when looking at its layout.",
        },
      ],

      card1: {
        title: "Over 8000 Customers with 5-star Review",
        description:
          "It is a long established fact that a reader will be distracted by the readable content of a page when looking at its layout.",
        stars: 5,
        designerName: "Tobias May",
        designerRole: "UI/UX Designer",
        designerImage: "../../public/img/t1.png",
      },
      cardData2And3: [
        {
          title: "Great Place",
          description:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Cum, voluptatem tempora libero possimus esse beatae voluptas ullam, eius explicabo, magnam omnis expedita itaque! Ipsa, ratione eum",
          stars: 5,
          designerName: "Tobias May",
          designerRole: "UI/UX Designer",
          designerImage: "../../public/img/t1.png",
        },
        {
          title: "Great Place",
          description:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Cum, voluptatem tempora libero possimus esse beatae voluptas ullam, eius explicabo, magnam omnis expedita itaque! Ipsa, ratione eum",
          stars: 5,
          designerName: "Tobias May",
          designerRole: "UI/UX Designer",
          designerImage: "../../public/img/t1.png",
        },
      ],
    };
  },

  methods: {
    handleGetStartedClick() {
      // azione al click
    },
    handleCustomButtonClick() {
      // azione al click
    },
    previousCard() {
      // Logica per andare alla card precedente
    },
    nextCard() {
      // Logica per andare alla card successiva
    },

    getImageSrc(index) {
      const imagePaths = [
        "../../public/img/d-1.png",
        "../../public/img/d-2.png",
        "../../public/img/d-3.png",
        "../../public/img/d-4.png",
        "../../public/img/d-5.png",
      ];
      return imagePaths[index];
    },
  },
};
</script>

<template>
  <main>
    <!-- SECTION-1 -->
    <section class="welcome">
      <div
        class="section-1 container d-flex justify-content-center flex-column"
      >
        <h1>
          Welcome to <br />
          DogMilo Pets
        </h1>
        <p>
          Lorem ipsum dolor sit, amet consectetur adipisicing elit. <br />
          Ad repellendus soluta facilis.
        </p>
        <div class="d-flex">
          <button class="btn btn-custom" @click="handleGetStartedClick">
            Get Started
          </button>
          <button class="custom-square-button" @click="handleCustomButtonClick">
            <font-awesome-icon
              :icon="['far', 'circle-play']"
              bounce
              size="lg"
            />
          </button>
        </div>
      </div>
    </section>

    <!-- SECTION-2 -->
    <section class="description">
      <div class="container d-flex align-items-center">
        <div>
          <img src="../../public/img/about.png" alt="" />
        </div>
        <div class="about-us">
          <div class="d-flex about-us-icon">
            <img src="../../public/img/dog-icon.png" alt="" />
            <p>About Us</p>
          </div>
          <h2>Welcome DogMilo Pets</h2>
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Assumenda
            porro, ipsum voluptas ut minima beatae. Atque debitis veritatis
            error tempore!
          </p>
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Assumenda
            porro, ipsum voluptas ut minima beatae. Atque debitis veritatis
            error tempore!
          </p>
        </div>
      </div>
    </section>

    <!-- SECTION-3 -->
    <section>
      <div class="service">
        <div
          class="container d-flex flex-column justify-content-center align-items-center"
        >
          <p>Service</p>
          <h2>DogMilo Pet Care Services Fo Your Best Friend</h2>
          <div class="card-container">
            <Card
              v-for="(card, index) in cardData"
              :key="index"
              :imageSrc="getImageSrc(index)"
              :title="card.title"
              :text="card.text"
              class="mt-5"
            />
          </div>
        </div>
      </div>
    </section>

    <!-- SECtION-4 -->
    <section>
      <div class="choose d-flex">
        <div>
          <img src="../../public/img/why.png" alt="" />
        </div>
        <div class="container">
          <div class="d-flex about-us-icon">
            <img src="../../public/img/dog-icon.png" alt="" class="zampa" />
            <p>About Us</p>
          </div>
          <h2>Why Choose Us?</h2>
          <div class="d-flex">
            <img src="../../public/img/w-3.png" alt="" />
            <div class="p-3">
              <h4>Safety First</h4>
              <p>
                it is a long established a reader will be distructed by the
                readble content of a page when looking at its layout.
              </p>
            </div>
          </div>
          <div class="d-flex">
            <img src="../../public/img/w-2.png" alt="" class="yards" />
            <div class="p-3">
              <h4>Play Yards</h4>
              <p>
                it is a long established a reader will be distructed by the
                readble content of a page when looking at its layout.
              </p>
            </div>
          </div>
          <div class="d-flex">
            <img src="../../public/img/w-1.png" alt="" class="monitor" />
            <div class="p-3">
              <h4>Monitor Your Pets</h4>
              <p>
                it is a long established a reader will be distructed by the
                readble content of a page when looking at its layout.
              </p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- SECTION-5 -->
    <section class="review mt-5">
      <div class="container d-flex justify-content-center">
        <!-- CARD 1-->
        <div class="card border-0">
          <div class="card-body">
            <div class="d-flex about-us-icon">
              <img src="../../public/img/dog-icon.png" alt="" class="zampa-2" />
              <p>Rewview & Rating</p>
            </div>
            <h4 class="card-title">{{ card1.title }}</h4>
            <p class="card-text">{{ card1.description }}</p>
            <font-awesome-icon
              v-for="card in card1.stars"
              :key="card"
              :icon="['fas', 'star']"
              style="color: #c7c11bd9"
            />
            <div class="d-flex align-items-center">
              <img :src="card1.designerImage" alt="" class="designer" />
              <div>
                <h6>{{ card1.designerName }}</h6>
                <p>{{ card1.designerRole }}</p>
              </div>
            </div>
          </div>
        </div>

        <!-- CARD-2 e CARD-3 -->
        <div
          v-for="(card, index) in cardData2And3"
          :key="index"
          class="card backcolor"
        >
          <div class="card-body">
            <font-awesome-icon
              v-for="card in card.stars"
              :key="card"
              :icon="['fas', 'star']"
              style="color: #c7c11bd9"
            />
            <h6 class="card-title">{{ card.title }}</h6>
            <p class="card-text">{{ card.description }}</p>
            <div class="d-flex align-items-center">
              <img :src="card.designerImage" alt="" class="designer" />
              <div>
                <h6>{{ card.designerName }}</h6>
                <p>{{ card.designerRole }}</p>
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- BUTTON -->
      <div class="container text-right">
        <div class="button-container">
          <button @click="previousCard">
            <img src="../../public/img/left-arrow.png" alt="" />
          </button>
          <button @click="nextCard">
            <img src="../../public/img/next.png" alt="" />
          </button>
        </div>
      </div>
    </section>
  </main>
</template>

<style lang="scss" scoped>
// SECTION-1
.welcome {
  background-image: url("../../public/img/b.png");
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center;
  min-height: 80vh;

  .section-1 {
    min-height: 80vh;
    color: white;

    h1 {
      margin-bottom: 20px;
    }

    p {
      font-size: 14px;
      margin-bottom: 20px;
    }

    .btn {
      font-size: 22px;
      color: gray;
    }

    // BUTTON
    /* Stile hover dei pulsanti */
    .btn-custom {
      background-color: #cc7c2b;
      color: #fff;
      border-radius: 60px;
      font-size: 22px;
      transition: background-color 0.3s, color 0.3s, transform 0.3s;
      margin-right: 15px;
    }

    .btn-custom:hover {
      background-color: cc7c2b;
      color: #fff;
      border-radius: 60px;
      transform: scale(1.1);
    }

    .custom-square-button {
      width: 60px;
      height: 60px;
      background-color: #add8e6;
      color: #fff;
      border: none;
      border-radius: 10px;
      font-size: 22px;
      transition: background-color 0.3s, color 0.3s, transform 0.3s;
    }

    .custom-square-button:hover {
      background-color: #add8e6;
      color: #fff;
      transform: scale(1.1);
    }
  }
}

// SECTION-2
.description {
  .container {
    min-height: 700px;

    img {
      height: 450px;
    }

    .about-us {
      max-width: 550px;
      margin: 0 auto;
      padding: 20px;

      h2 {
        margin: 15px 0;
      }

      p {
        line-height: 1.8;
      }

      .about-us-icon {
        height: 50px;
        align-items: center;

        img {
          height: 50px;
          margin-right: 10px;
        }
      }
    }
  }
}

// SECTION-3
.service {
  background-color: #f5f5f5;
  .container {
    min-height: 80vh;
    text-align: center;
  }
  .card-container {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 20px;
  }
}

// SECTION-4
.choose {
  .container {
    padding: 50px;
    .zampa {
      height: 50px;
    }

    h2 {
      margin-top: 18px;
      margin-bottom: 25px;
    }

    img {
      height: 150px;
    }

    .yards {
      margin-left: 130px;
    }

    .monitor {
      margin-left: 275px;
    }
  }
}

// SECTION-5
.review {
  padding: 50px;

  .backcolor {
    background-color: #f4f4f4;
  }
  .card {
    width: 25rem;

    h4 {
      margin: 15px 0;
    }

    h6 {
      margin: 15px 0;
    }

    .designer {
      width: 50px;
      height: 50px;
      border-radius: 50%;
      object-fit: cover;
      margin-right: 10px;
    }
  }

  .zampa-2 {
    height: 30px;
    margin-right: 10px;
  }

  p {
    font-size: 12px;
  }
}

.button-container {
  padding: 50px;
  margin-left: 1063px;

  button {
    background-color: #ce7c2a;
    margin-left: 10px;
  }

  img {
    width: 40px;
  }
}
</style>
