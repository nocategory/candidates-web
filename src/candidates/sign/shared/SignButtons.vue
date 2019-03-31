<template>
  <div class="sign--buttons">
    <router-link :to="{path: '/sign/up'}">
      <a class="btn btn--colorful">SIGN UP</a>
    </router-link>
    <router-link :to="{path: '/sign/in'}">
      <a class="btn btn--grey">LOGIN</a>
    </router-link>
  </div>
</template>

<script>
import Button from '@/core/components/form/Button';
import SignHeader from '@/candidates/sign/shared/SignHeader.vue';

export default {
  components: {
    Button,
    SignHeader
  }
};
</script>

<style lang="postcss" scoped src="@/core/components/form/Button.css"></style>
<style lang="postcss" scoped>
  .sign-header__signup {
    position: relative;
    z-index: 1;
    display: block;
    width: 200px;
    height: 50px;
    padding-top: 15px;
    padding-bottom: 15px;
    font-size: 16px;
    font-family: var(--ff-font);
    color: #fff;
    text-align: center;
    border-radius: 50px;
    border: 0;
    background-color: #009EB7;
    cursor: pointer;
    outline: 0;
    text-transform: uppercase;
    box-sizing: border-box;
    &::after {
      content: '';
      position: absolute;
      z-index: -1;
      top: 0;
      right: 0;
      bottom: 0;
      left: 0;
      border-radius: 50px;
      background-image: linear-gradient(to right, #009eb7 0%, #80deea 100%);
      opacity: 1;
      transition: opacity .3s ease;
    }
    &:hover,
    &:focus {
      &::after {
        opacity: 0;
      }
    }
    @media (--phoneLarge-viewport) {
      margin: 0 auto;
    }
  }
  .sign--buttons {
    flex-direction: row;
    display: flex;
    align-items: center;
    a {
      margin: 0 4px;
    }
  }
</style>
