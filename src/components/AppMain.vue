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
    };
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
          <button class="btn btn-custom">Get Started</button>
          <button class="custom-square-button">
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
        <div class="container d-flex flex-column justify-content-center align-items-center">
            <p>Service</p>
            <h2>DogMilo Pet Care Services Fo Your Best Friend</h2>
            <div class="card-container">
              <Card
                v-for="(card, index) in cardData"
                :key="index"
                :imageSrc="card.imageSrc"
                :title="card.title"
                :text="card.text"
                class="mt-5"
              />
          </div>
        </div>
      </div>
    </section>

    <!-- SECtION-4 -->
    
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
</style>
