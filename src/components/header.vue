<template>
    <header>
      <div class="container">
                <nav>
            <div class="left_nav">
                <a href="#">
                    <img :src="SiteLogo" alt="Site Logo" />
                </a>
                <ul>
                    <li><a v-a-tooltip.hover title="Tooltip content" href="#">Service</a></li>
                    <li><a href="#">Agency</a></li>
                    <li><a href="#">Case Study</a></li>
                    <li><a href="#">Resources</a></li>
                    <li><a href="#">Contact</a></li>
                </ul>
            </div>
            <div class="right_nav">
                <button @click="showAlert" class="login_btn">Get started</button>
                <button @click="showAlert" class="signup_btn"><img :src="Ring" alt="Ring Icon"></button>
            </div>
        </nav>
      </div>
    </header>
</template>
<script setup>
import SiteLogo from '../assets/sitelogo.png';
import Ring from '../assets/ring.svg';

const showAlert = () => {
    alert("Sabziyam chiqmaydi bosmang 😂");
};
</script>

<style lang="scss" scoped>
header {
  width: 100%;
  background-color: transparent;
  display: flex;
  align-items: center;
  padding: 20px 40px;
  nav {
    display: flex;
    justify-content: space-between;
    width: 100%;
    .left_nav {
      display: flex;
      align-items: center;
      gap: 33px;
      img {
        height: 40px;
        margin-right: 20px;
      }
      ul {
        display: flex;
        list-style: none;
        li {
          margin-right: 20px;
          a {
            text-decoration: none;
            color: #020407;
            font-weight: 500;
            transition: color 0.3s ease;
            &:hover {
              color: #99EA48; /* Example hover color */
            }
          }
        }
      }
    }
    .right_nav {
      display: flex;
      align-items: center;
      gap: 9px;

      .login_btn, 
      .signup_btn {
        background-color: transparent;
        border: 2px solid #010205;
        color: #010205;
        padding: 13px 35px;
        cursor: pointer;
        font-weight: 500;
        transition: all 0.3s ease;
        &:hover {
          background-color: #010205;
          color: #fff;
        }
      }
      .signup_btn {
        display: flex;
        align-items: center;
        border-radius: 50px;
        padding: 0;
        transition: all 0.3s ease;
        &:hover{
          animation: ring 4s .7s ease-in infinite;
        }
        img {
          width: 50px;
          height: 50px;
        }
      }
    }
  }
}
</style>