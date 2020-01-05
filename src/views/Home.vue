<template>
  <div class="home">
    <div class="logo">
      <Trademark />
    </div>
    <div class="content">
      <span class="message">UNDER CONSTRUCTION!</span>
      <div class="social-container">
        <SocialButtons :items="socialLinks" />
      </div>
    </div>
  </div>
</template>

<script>
import Trademark from '@/components/Trademark';
import SocialButtons from '@/components/SocialButtons';
import data from '@/data/info.json';

export default {
  name: 'Home',
  components: {
    Trademark,
    SocialButtons,
  },
  data() {
    return data;
  },
};
</script>

<style scoped lang="scss">
.home {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 1100px;

  > .logo {
    display: flex;
    align-content: center;
    justify-content: flex-end;

    width: 300px;
    height: 100%;
    user-select: none;
  }
  > .content {
    display: flex;
    flex-direction: column;
    width: 50%;
    flex-wrap: nowrap;

    > span.message {
      font-size: 40px;
      font-weight: 300;
      letter-spacing: 8px;
      margin-bottom: 4px;
      text-transform: uppercase;

      animation: message-animation 1.2s linear infinite;
      @keyframes message-animation {
        0% {
          color: var(--secundary);
        }
        50% {
          color: var(--primary);
        }
        100% {
          color: var(--secundary);
        }
      }
    }

    > .social-container {
      padding: 16px 0 0;
      width: 60%;
    }
  }

  @media (max-width: 1100px) {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    width: 100%;

    > .logo {
      height: 360px;
    }

    > .content {
      flex-direction: column-reverse;
      align-items: center;
      text-align: center;
      max-width: 360px;
      width: 100%;

      > span.message {
        font-size: 24px
      }

      > .social-container {
        padding: 0 0 32px;
        width: 80%;
      }
    }

  }
}
</style>
