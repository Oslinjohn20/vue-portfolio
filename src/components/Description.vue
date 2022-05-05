<template>
  <article>
    <h2>A little about me</h2>
    <p>
      <!-- Some words on what I do as a developer and proficiences -->
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Quo rerum
      exercitationem, architecto dolorum velit voluptas minima nobis iure error
      explicabo. Nam enim provident adipisci porro doloribus dolore obcaecati
      ipsa ratione.

      <span
        ref="reactive"
        @mouseenter="reactiveHighlight"
        @mouseleave="reactiveHighlightRemove"
      >
        HTML, CSS, Javascript
      </span>
      and modern framework
      <span
        ref="gdesign"
        @mouseenter="gHighlight"
        @mouseleave="gHighlightRemove"
      >
        VueJs
      </span>
      Lorem, ipsum dolor sit amet consectetur adipisicing elit. Amet debitis
      eligendi architecto dicta, nobis perferendis sed hic ullam ratione nam
      consequuntur deserunt doloribus quam animi vitae voluptatem facere id
      perspiciatis!
      <!-- Some words about what I like to achieve within creating applications -->
    </p>
    <p>
      <!-- What I do in my free time  -->
      Lorem ipsum dolor sit amet consectetur, adipisicing elit. Culpa
      praesentium alias explicabo magni libero, error perspiciatis? Maiores
      saepe impedit eveniet numquam iusto, ut perferendis architecto qui,
      voluptates debitis, fugiat beatae!
    </p>
    <ul>
      <li>
        <!-- icon/images for tech stack -->
      </li>
      <li>
        <!-- pdf download for cv -->
        <a :href="pdf" download>
          <button>CV</button>
        </a>
      </li>
    </ul>
  </article>
</template>

<script>
import { TimelineLite } from "gsap/dist/gsap";

export default {
  name: "Description",
  data() {
    return {
      pdf: require(""), // Have to put an pdf file of my cv for download from assests
    };
  },

  methods: {
    reactiveHighlight() {
      const tl = new TimelineLite();
      const { reactive } = this.$refs;
      tl.to(reactive, {
        backgroundColor: "#1a1a1a",
        color: "white",
      });
    },

    reactiveHighligthRemove() {
      const tl = new TimelineLite();
      const { reactive } = this.$refs;
      tl.to(reactive, {
        backgroundColor: "#141414",
        color: "#8d8d8d",
      });
    },

    uiHighlight() {
      const tl = new TimelineLite();
      const { uidesign } = this.$refs;
      tl.to(uidesign, {
        backgroundColor: "#1a1a1a",
        color: "white",
      });
    },

    uiHighlightRemove() {
      const tl = new TimelineLite();
      const { uidesign } = this.$refs;
      tl.to(uidesign, {
        backgroundColor: "#141414",
        color: "#8d8d8d",
      });
    },

    gHighlight() {
      const tl = new TimelineLite();
      const { gdesign } = this.$refs;
      tl.to(gdesign, {
        backgroundColor: "#1a1a1a",
        color: "white",
      });
    },

    gHighlightRemove() {
      const tl = new TimelineLite();
      const { gdesign } = this.$refs;
      tl.to(gdesign, {
        backgroundColor: "#141414",
        color: "#8d8d8d",
      });
    },
  },
};
</script>

<style scoped>
p {
  font-size: clamp(16px, 1.2vw, 1.2vw);
  line-height: 2;
  color: #9d9d9d;
}

h2 {
  font-size: clamp(24px, 3vw, 3vw);
  font-weight: 300;
  margin: 0;
}

ul {
  margin-top: clamp(3em, 4vw, 4vw);
  list-style-type: none;
  display: flex;
  justify-content: space-around;
}

img {
  height: 30px;
  border: none;
  font-size: 18px;
  font-weight: 900;
  background-color: white;
  cursor: pointer;
  transition: background-color 0.2s ease-in-out;
}

button {
  height: 30px;
  border: none;
  font-size: 18px;
  font-weight: 900;
  background-color: white;
  cursor: pointer;
  transition: background-color 0.2s ease-in-out;
}

button:hover {
  background-color: #59ff9c;
}

img:hover {
    filter: none;
}

span {
    background-color: #141414;
    margin: 0.em;
    padding: 0.3em 0.7em;
    color: #8d8d8d;
}

@media (max-width: 700px) {
    img,
    button {
        height: 20px;
    }
}
</style>