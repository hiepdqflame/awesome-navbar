<template>
  <ul class="wrap-navbar">
    <li><a href="#" data-title="home">Home</a></li>
    <li><a href="#" data-title="About">About</a></li>
    <li><a href="#" data-title="Bacodekiller">Bacodekiller</a></li>
    <li><a href="#" data-title="Flame">Flame</a></li>
  </ul>
</template>

<script>
export default {
  name: "NavbarFirst"
};
</script>

<style lang="scss" scoped>
.wrap-navbar {
  display: block;
  text-align: center;
  margin: 0 auto;
  padding: 0;
  width: 100%;
  min-width: 535px;
  background-color: #343e48;
  position: relative;
  &:after {
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    opacity: 0.5;
  }

  box-shadow: 0 3px 8px rgba(black, 0.5);
  li {
    margin: 0 auto;
    display: inline-block;
    list-style: none;
    padding: 0;

    a {
      display: block;
      padding: 25px;
      text-transform: uppercase;
      position: relative;
      z-index: 2;
      text-shadow: 1px 0px rgba(black, 0.4);
      color: #686f77;
      letter-spacing: 0.2em;
      text-decoration: none;
      transition: color 200ms;
      transform-style: preserve-3d;
      &:hover {
        color: #343e48;
      }
      &:after {
        content: attr(data-title);
        position: absolute;
        display: block;
        text-shadow: none;
        top: 29%;
        left: 18px;
        padding: 5px 7px;
        color: transparent;
        background: #4795c3;
        li:nth-child(2) & {
          background: #ecc64b;
        }
        li:nth-child(3) & {
          background: #0b9ea6;
        }
        li:nth-child(4) & {
          background: #f26667;
        }
        transform-origin: 50% 0%;
        backface-visibility: hidden;
        transform: translate3d(0px, 105%, 0px) rotateX(-112deg);
        transform-style: preserve-3d;
        transition: all 200ms ease;
        z-index: -1;
      }
      &:hover:after {
        transform: rotateX(0deg) translateZ(0px);
      }
    }
  }
}
</style>
