<template>
  <div align="center"
      justify="center">
      <p>{{ message2 }}</p>
      <input v-model="message2" />

    <div>{{ message }}</div>

    <span v-bind:title="message">
      Hover your mouse over me for a few seconds to see my dynamically bound
      title!
    </span>

    <span v-if="seen">Now you see me</span>
    <!-- //in nuxt this is the syntax; we can also replace the :key="todo.text" or :key="index"
//create todo folder to store every value in the todos folder and each todo folder will be identified using the todo value -->
    <div>
      <ol>
        <li v-for="todo in todos" :key="todo">
          {{ todo.text }}
        </li>
      </ol>
    </div>
    <div>
      <p>{{ message }}</p>
      <button v-on:click="reverseMessage">Reverse Message</button>
    </div>


<Component2>  <todo-item
      v-for="item in groceryList"
      v-bind:todo="item"
      v-bind:key="item.id"
    ></todo-item></Component2>



  </div>
</template>

<script>
import Component2 from "../components/Component2"

export default {
  data() {
    return {
      message2: 'Hi I`m the child',
      message: 'Hi this is a message! :)', //when you do a this.message you access the data here so you modify it here and it updates all over but you can also be selective we'll see next
      seen: false,
      todos: [
        { text: 'This is my first element' },
        { text: 'This is my second element' },
        { text: 'This is my third element' }, // add commas after things in the <script/>
      ],
    }
  },

  methods: {
    reverseMessage: function () {
      this.message = this.message.split('').reverse().join('')
    },
  },
 components: 
    {
      Component2
    }
}
</script>
