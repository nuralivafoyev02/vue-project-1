<template>
    <div id="intro">
        <div class="container">
            <div class="intro_left">
                <h1>Stay ahead of the curve with our forward-thinking</h1>
                <p>An award-winning SEO agency with disciplines in digital marketing, design, and website development.
                    focused on understanding you.</p>
                <div class="intro_btns">
                    <button @click="showAlert" class="btn st">Schedule Call</button>
                    <button @click="showAlert" class="btn dn">View Case Study</button>
                </div>
            </div>
            <div class="intro_right">
                <img class="rectangle_img" :src="Rectangle" alt="Rectangle">
                <img class="count_img" :src="CountImg" alt="Count">
                <img class="drivetraffic_img" :src="DriveTraffic" alt="Drive Traffic">

                <img class="topup_img" :src="TopUp" alt="Top Up">
            </div>
        </div>
    </div>
</template>
<script setup>
import TopUp from '../assets/topup.png';
import Rectangle from '../assets/Rectangle.png';
import CountImg from '../assets/count230.png';
import DriveTraffic from '../assets/drivetraffic.png';

const showAlert = () => {
    alert("Sabziyam chiqmaydi bosmang 😂");
};
</script>

<style lang="scss" scoped>
#intro {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 53px 0;
    width: 100%;

    .container {
        display: flex;
        align-items: center;
        justify-content: space-between;

        .intro_left {
            width: 50%;

            h1 {
                font-size: 72px;
                color: #010205;
                margin-bottom: 24px;
                letter-spacing: -3%;
                font-weight: 600;
            }

            p {
                font-size: 16px;
                color: #878C91;
                margin-bottom: 32px;
            }

            .intro_btns {
                display: flex;

                .btn {
                    border: none;
                    padding: 22px 41px;
                    border-radius: 70px;
                    font-weight: 700;
                    font-size: 18px;
                    cursor: pointer;
                }

                .st {
                    background-color: #010205;
                    color: #fff;
                    margin-right: 16px;
                }

                .nd {
                    background-color: none;
                    text-decoration: underline;
                }
            }
        }

        .intro_right {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            grid-template-rows: repeat(2, 1fr);
            gap: 24px;
            position: relative;

            img {
                transition: all 0.3s ease;
            animation: fadeIn .7s ease-in-out;
            }
            .topup_img {
                position: absolute;
                width: 108px;
                height: 108px;
                right: 387px;
                z-index: 4;
                animation: swim 3s ease-in-out infinite;
                
            }
            .rectangle_img {
                grid-area: 1 / 1 / 2 / 2;
                &:hover {
                    transform: translateX(-10px) rotate(-3deg);  
                }
            }
            .count_img{
                grid-area: 1 / 2 / 2 / 3;
                &:hover {
                    transform: translateX(10px) rotate(3deg);  
                }
            }
            .drivetraffic_img{
                grid-area: 2 / 1 / 3 / 3;
                &:hover {
                    transform: translateX(10px) rotate(3deg); 
                }
        }}

    }
}


</style>