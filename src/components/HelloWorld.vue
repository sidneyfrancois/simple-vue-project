<script setup lang="ts">
import { ref, reactive, computed } from 'vue'

defineProps<{ msg: string }>()

const author = reactive({
  name: 'John Doe',
  books: [
    'Vue 2 - Advanced Guide',
    'Vue 3 - Basic Guide',
    'Vue 4 - The Mystery'
  ]
})

const count = ref(0);
const exampleReactiveObject = reactive({ employeeId: 1, employeeName: "João"});
const showTitle = ref(true);
const items = ref([{ message: 'Foo' }, { message: 'Bar' }])
const myObject = reactive({
  title: 'How to do lists in Vue',
  author: 'Jane Doe',
  publishedAt: '2016-04-10'
})

function changeEmployee() {
  exampleReactiveObject.employeeId = 2;
  exampleReactiveObject.employeeName = "Beltrano";
}

function addBook() {
  author.books.push('New book');
}

function removeBook() {
  author.books.pop();
}

function toggleShowTitle() {
  showTitle.value = !showTitle.value;
}

const publishedBooksThree = computed(() => {
  return author.books.length > 3 ? 'more than three books' : 'three or less than three books';
});

</script>

<template>
  <h1>{{ msg }}</h1>

  <template v-if="showTitle">
    <div class="card">
      <h2>{{ exampleReactiveObject.employeeId }}</h2>
      <h2>{{ exampleReactiveObject.employeeName }}</h2>
      <button type="button" @click="changeEmployee">Change object</button>
    </div>
  </template>
  <button type="button" @click="toggleShowTitle">Show/Hide</button>

  <div class="card">
    <h2>List of books, author: {{ author.name }}</h2>
    <li v-for="book of author.books">
      {{ book }}
    </li>
    <h3>The list of books has {{ publishedBooksThree }}</h3>
    <button type="button" @click="addBook">Add book</button>
    <button type="button" @click="removeBook">Remove book</button>
  </div>

  <div class="card">
    <li v-for="item of items">
      {{ item.message }}
    </li>
  </div>

  <div class="card">
    <ul>
      <li v-for="value in myObject">
        {{ value }}
      </li>
    </ul>
  </div>

  <div class="card">
    <button type="button" @click="count++">count is {{ count }}</button>
    <p>
      Edit
      <code>components/HelloWorld.vue</code> to test HMR
    </p>
  </div>

  <p>
    Check out
    <a href="https://vuejs.org/guide/quick-start.html#local" target="_blank"
      >create-vue</a
    >, the official Vue + Vite starter
  </p>
  <p>
    Install
    <a href="https://github.com/vuejs/language-tools" target="_blank">Volar</a>
    in your IDE for a better DX
  </p>
  <p class="read-the-docs">Click on the Vite and Vue logos to learn more</p>
</template>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>
