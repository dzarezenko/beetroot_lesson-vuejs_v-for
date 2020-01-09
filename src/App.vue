<template>
  <div id="app">
    <ol>
      <li v-for="(person, index) in persons" :key="index">
        <span v-for="(prop, key, id) in person" :key="id">, {{key}}: {{ prop }} ({{ id }})</span>
      </li>
    </ol>

    <span v-for="n in 40" :key="n">{{ n }}&nbsp;</span>
  </div>
</template>

<script>

export default {
  name: 'app',
  data() {
    return {
      persons: [
        {
          name: "Anna",
          age: 99,
        },
        {
          name: "Dmytro",
          age: 33,
        },
        {
          name: "Illya",
          age: 23,
        },
      ],
    }
  },
}
</script>
