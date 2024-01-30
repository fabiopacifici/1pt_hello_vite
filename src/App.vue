<script>
export default {
  name: 'App',
  data() {
    return {
      image: 'https://logowik.com/content/uploads/images/laravel8530.jpg',
      message: 'Fabio2',
      content: 'lorem ipsum dolor',
      msg: 'lorem',
      movies: ['Matrix', 'Avatar'],
      users: [
        {
          id: 1,
          name: 'Giuseppe'
        },
        {
          id: 2,
          name: 'Isabella'
        }
      ],
      slider: {
        name: 'Mandalorian',
        images: []
      },
      name: '',
      lastname: '',
      styles: 'text-red bg-gray',
      classes: 'red',
      count: 0,
      show: true
    }
  },
  methods: {

    /* anotherFunction(){
      console.log('Another function')
    }, */

    testFunction() {
      console.log('This is a method [a function inside an object]')
      /* console.log(this.message)
      this.anotherFunction(); */
    }
  }
}
</script>

<template>
  <div>

    {{ count }}
    <button @click="count++">Click me</button>

    <!-- Live Coding 1 greetings -->

    <div>
      <label for="name">First Name</label>
      <input type="text" v-model="name">

      <label for="lastname">Last Name</label>
      <input type="text" v-model="lastname">

      <p>Ciao {{ name }} {{ lastname }}</p>
    </div>


    <img :src="image" alt="">

    <!-- Text Interpolation with mustache syntax -->
    <h1>Hello {{ message }}</h1>
    <p>{{ content }}</p>


    <!-- Two ways data binings  (v-model)-->
    <div>length: {{ msg.length }}</div>
    <input type="text" v-model="msg">



    <!-- Class Biding (v-bing) -->
    <p v-bind:class="styles">
      Lorem ipsum dolor, sit amet consectetur adipisicing elit. Beatae excepturi in tenetur repellendus ab ad accusantium
      eaque doloremque incidunt? Dolor sunt animi a nostrum reprehenderit quia dolorem numquam accusamus aliquam?
    </p>


    <p :class="classes">
      Lorem ipsum dolor, sit amet consectetur adipisicing elit. Beatae excepturi in tenetur repellendus ab ad accusantium
      eaque doloremque incidunt? Dolor sunt animi a nostrum reprehenderit quia dolorem numquam accusamus aliquam?
    </p>


    <!-- Conditional rendering -->
    <h2>Conditionals</h2>

    <p v-if="show">
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Fugit accusamus cumque inventore rem consequatur excepturi
      saepe fugiat debitis, minima, at qui quidem officia incidunt consectetur. Velit necessitatibus obcaecati excepturi
      minima.
    </p>

    <p v-if="show">
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Fugit accusamus cumque inventore rem consequatur excepturi
      saepe fugiat debitis, minima, at qui quidem officia incidunt consectetur. Velit necessitatibus obcaecati excepturi
      minima.
    </p>

    <p v-else>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Fugit accusamus cumque inventore rem consequatur excepturi
      saepe fugiat debitis, minima, at qui quidem officia incidunt consectetur. Velit necessitatibus obcaecati excepturi
      minima.
    </p>


    <p v-show="show">
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Fugit accusamus cumque inventore rem consequatur excepturi
      saepe fugiat debitis, minima, at qui quidem officia incidunt consectetur. Velit necessitatibus obcaecati excepturi
      minima.

    </p>



    <!-- Loops  in array of strings-->


    <ul>
      <li v-for="movie in movies">
        {{ movie }}
      </li>
    </ul>

    <!-- In array of objects -->
    <ul>
      <li v-for="user in users">
        {{ user.name }}

      </li>
    </ul>



    <!-- In range numerico -->
    <ul>
      <li v-for="numb in 100">{{ numb }}</li>
    </ul>


    <ul>
      <li v-for="(value, key) in slider">
        {{ key }}: {{ value }}
      </li>
    </ul>



  </div>
</template>

<style></style>
