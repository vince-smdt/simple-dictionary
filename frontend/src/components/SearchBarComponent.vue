<template>
  <div id="outer-search-bar">
    <label>Word to lookup: </label>
    <div id="search-bar">
      <img src="../assets/search.svg" alt="Search Icon" />
      <input type="text" v-model="word" />
    </div>
    <button type="button" id="lookup-button" @click="$emit('search', word)">
      Look up
    </button>
  </div>
</template>

<script>
export default {
  name: "SearchBar",
  data() {
    return {
      word: "",
    };
  },
};
</script>

<style scoped>
#outer-search-bar label,
#search-bar input,
#lookup-button {
  font-size: 20px;
  font-family: "Roboto Mono";
  color: white;
  transition: background 0.1s ease-in;
}

#outer-search-bar,
#search-bar {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 5px;
}

#search-bar {
  padding: 5px;
  border: white solid 2px;
  border-radius: 5px;
}

#search-bar:hover {
  background: #0c2146;
}

#search-bar input {
  background: transparent;
  color: white;
  border: none;
}

#search-bar input:focus {
  outline: none;
}

#lookup-button {
  background: transparent;
  border: white solid 2px;
  border-radius: 5px;
  padding: 5px;
  cursor: pointer;
}

#lookup-button:hover {
  background: #0c2146;
}
</style>
