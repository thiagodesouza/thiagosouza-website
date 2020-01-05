<template>
  <ul class="social-buttons">
    <li v-for="item in items" :key="item.icon" class="item">
      <a :href="item.url" target="_blank">
        <i :class="item.icon"></i>
      </a>
    </li>
  </ul>
</template>

<script>
export default {
  name: 'SocialButtons',
  props: {
    items: Array,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.social-buttons {
  display: flex;
  justify-content: space-between;

  list-style: none;
  width: 100%;

  > .item {
    display: flex;
    align-items: center;
    justify-content: center;

    background-color: var(--dark);
    border-radius: 50%;
    color: var(--lighter);
    cursor: pointer;
    height: 56px;
    width: 56px;
    user-select: none;

    &:hover {
      color: var(--dark);
      background-color: var(--primary);
    }

    > a {
      display: flex;
      align-items: center;
      justify-content: center;

      color: inherit;
      font-size: 20.4px;
      height: 100%;
      width: 100%;
      text-decoration: none;
    }
  }
}
</style>
