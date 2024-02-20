<template>
  <div class="dropdown">
    <button
      class="dropbtn"
      :style="{ backgroundColor: selectedColor }"
      @click="toggleDropdown">
      Regions
    </button>
    <div class="dropdown-content" v-show="isDropdownOpen">
      <a
        v-for="option in options"
        :key="option.value"
        @click="selectLang(option)"
        >{{ option.label }}</a
      >
      <span v-if="index !== options.length - 1" class="line"></span>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isDropdownOpen: false,
      options: [
        { label: "USA", value: "en-us" },
        { label: "UK", value: "en-uk" },
        { label: "China", value: "en-cn" },
        { label: "Pakistan", value: "en-pk" },
      ],
      selectedLang: "",
    };
  },
  methods: {
    toggleDropdown() {
      this.isDropdownOpen = !this.isDropdownOpen;
    },
    selectLang(option) {
      this.selectedLang = option.value;
      let oldUrl = `${window.location.pathname}`;
      const unwantedAppend = oldUrl.lastIndexOf('/');
      oldUrl = oldUrl.substring(0,unwantedAppend);
      let newUrl = `${oldUrl}/${option.value}`;
      window.history.pushState({}, '', newUrl);
      
    },
  },
};
</script>

<style scoped>

.dropdown {
  position: relative;
  display: inline-block;
}

.dropbtn {
  color: #ffffff;
  font-size: 1.5vw;
  font-family: Impact, Haettenschweiler, "Arial Narrow Bold", sans-serif;
  background: transparent;
  box-sizing: border-box;

  background: radial-gradient(
    163.75% 163.75% at 23.45% 140%,
    #0025ce 0%,
    rgba(9, 93, 230, 0.53) 100%
  );
  box-shadow: inset 0px 9px 15px #0d93ef;
  border-radius: 100px;
}

.dropdown-content {
  display: none;
  position: absolute;
  background-color: #092530;
  border-radius: 10px;
  border: 0.4px solid white;
  min-width: 160px;
  z-index: 1;
}

.dropdown-content a {
  color: #ffffff;
  padding: 12px 16px;
  text-decoration: none;
  display: block;
  font-family: "Aeonik";
  font-style: normal;
  font-weight: 250;
  font-size: 10px;
  line-height: 19px;
  
}

.dropdown-content a:hover {
  color: #00eaff;
}

.dropdown:hover .dropdown-content {
  display: block;
}

.dropdown:hover .dropbtn {
  background-color: #092530;
}
.line {
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  height: 1px;
  background-color: white;
}
</style>
