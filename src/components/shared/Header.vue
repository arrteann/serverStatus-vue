<template>
  <header>
    <h1>
      Server Management
      <span></span>
    </h1>
  </header>
</template>

<script>
export default {
  name: "app-header",
};
</script>

<style lang="scss" scoped>
header {
  text-align: center;
  display: flex;
  justify-content: center;
  h1 {
    text-transform: uppercase;
    border-bottom: 1px solid #3232;
    padding : {
      bottom: 5px;
    }
    position: absolute;

    span {
      display: inline-block;
      width: 5px;
      height: 5px;
      background-color: #da4824;
      padding: 2px;
      border-radius: 1000rem;
      position: absolute;
      right:-9px;
      top:0px;
    }
  }
}
</style>