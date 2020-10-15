<template>
  <div class="wrapper">
    <div class="row">
      <div>SERVER STATUS</div>
      <div :class="{ green: state, red: !state }">
        {{ status }}
      </div>
      <div><a @click="changeState()">CHECK AGAIN</a></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "app-server",
  data() {
    return {
      status: "OFFLINE",
      state: false,
    };
  },
  watch: {
    status: function () {
      if (this.status == "ONLINE") {
        this.state = true;
      } else {
        this.state = false;
      }
    },
  },
  methods: {
    changeState: function () {
      setTimeout(() => {
        this.status =
          this.status == "ONLINE"
            ? (this.status = "OFFLINE")
            : (this.status = "ONLINE");
      }, 1500);
    },
  },
};
</script>

<style lang="scss" scoped>
.wrapper {
  align-self: start;
  &:not(:first-child) {
    margin: {
      top: 25px;
    }
  }
}
.row {
  display: grid;
  grid-template-columns: repeat(3, auto);
}
a {
  color: white;
  background: #312e31;
  padding: 8px 14px;
  border-radius: 5px;
  font-size: 0.9rem;
  cursor: pointer;
  user-select: none;
}
.red {
  color: #f33e31e7;
}
.green {
  color: #12c255;
}
</style>