<template>
    <div>

        <!-- Header -->
        <div class="header">
            <h1>Cek Khodam rorrr</h1>
            <p>By <a href="https://radya.fun" target="_blank">Radyaif </a> & <a href="https://aryaem.vercel.app"
                    target="_blank">Aryaem </a></p>
        </div>

        <div class="input animate__animated animate__bounceIn">
            <section v-if="!state.showKhodam">
                <h2>Masukkan nama kamu</h2>
                <form @submit.prevent="submit">
                    <div class="wrap">
                        <div class="form-group">
                            <input type="text" id="name" name="name" autocomplete="off" v-model="state.isName">
                        </div>
                        <div class="form-actions">
                            <button type="submit">Cek</button>
                        </div>
                    </div>
                    <small v-if="state.warning" class="name_warning">Diisi dulu namanya dong</small>
                </form>
            </section>

            <section v-id="state.showKhodam">
                <div class="loading">
                    <section v-if="state.loading">
                        <h2 class="animate__animated animate__bounceIn">{{ state.loadingText }}</h2>
                        <div class="🤚">
                            <div class="👉"></div>
                            <div class="👉"></div>
                            <div class="👉"></div>
                            <div class="👉"></div>
                            <div class="🌴"></div>
                            <div class="👍"></div>
                        </div>
                    </section>
                    <h5 v-if="!state.loading && state.showKhodam">Khodam {{ state.isName }} adalah...</h5> <br>
                    <h2 v-if="!state.loading && state.showKhodam"> {{ state.currentKhodam }} </h2>
                    <div class="center">
                        <button v-if="!state.loading && state.showKhodam" class="reset-btn" @click="reset">Cari nama
                            lain</button>
                    </div>
                </div>
            </section>
        </div>

    </div>
</template>


<style scoped>
.header {
    min-height: 150px;
    text-align: center;
    /* border: 1px solid; */

}

.header h1 {
    padding-top: 40px;
    font-size: 32px;
    letter-spacing: 2px
        /* border: 1px solid pink; */
}

.header p {
    font-size: 14px;
    padding-top: 10px;
    /* border: 1px solid purple */
}

.header a {
    text-decoration: none;
    color: cyan;
    border-bottom: 1.5px solid rgba(0, 255, 255, 0);
    transition: all 0.6s ease 0s;
}

.header a:hover {
    border-bottom: 1.5px solid cyan;
    font-size: 15px;
}

.input {
    /* max-width: 28rem; */
    width: fit-content;
    margin: 60px auto;
    position: relative;
    overflow: hidden;
    z-index: 10;
    background: rgba(53, 53, 53, 0.57);
    border-radius: 16px;
    box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
    backdrop-filter: blur(11.3px);
    -webkit-backdrop-filter: blur(11.3px);
    border: 1px solid rgba(53, 53, 53, 1);
    padding: 35px 50px;
    border-radius: 1rem;
    box-shadow: 0 0.5rem 1rem rgba(0, 0, 0, 0.1);
}

.input::before {
    content: '';
    width: 6rem;
    height: 6rem;
    position: absolute;
    background-color: #a855f7;
    border-radius: 50%;
    z-index: -10;
    filter: blur(2rem);
}

.input::after {
    content: '';
    width: 8rem;
    height: 8rem;
    position: absolute;
    background-color: #38bdf8;
    border-radius: 50%;
    z-index: -10;
    filter: blur(1rem);
    top: 6rem;
    right: -3rem;
}

.input h2 {
    font-size: 14px;
    letter-spacing: 2px;
    color: #fff;
    font-weight: bold;
    margin-bottom: 1rem;
}

.wrap {
    display: flex;
    justify-content: space-between;
}

.form-group {
    margin-bottom: 1rem;
}

.form-group input,
.form-group textarea {
    padding: 0.5rem;
    width: 100%;
    border: 1px solid #d1d5db;
    border-radius: 0.375rem;
}

.form-actions {
    display: flex;
    justify-content: flex-end;
}

.form-group input {
    color: #000;
    height: 40px;
}

.form-actions button {
    height: 40px;
    background: linear-gradient(144deg, #a855f7, #5b42f3 50%, #00ddeb);
    color: white;
    padding: 0.5rem 3rem;
    margin-left: 15px;
    font-weight: bold;
    font-size: 10px;
    border-radius: 0.375rem;
    border: none;
    cursor: pointer;
    transition: opacity 0.3s ease;
}

.form-actions button:hover {
    opacity: 0.8;
}

.name_warning {
    color: yellow;
}

.loading section {
    /* border: 1px solid red; */
    display: flex;
    justify-content: center;
    align-items: center;
}

.loading section h2 {
    font-size: 30px;
}

.loading h2 {
    font-size: 30px;
    text-align: center;
}

.loading h5 {
    text-align: center
}

.reset-btn {
    background: linear-gradient(144deg, #a855f7, #5b42f3 50%, #00ddeb);
    letter-spacing: 1px;
    margin-top: 10px;
    padding: 8px 15px;
    border: none;
    border-radius: 7px;
    cursor: pointer;
    font-size: 12px;
    font-weight: 300;
}

.center {
    /* border: 1px solid white; */
    width: 100%;
    display: flex;
    justify-content: center;
}

.🤚 {
    --skin-color: #E4C560;
    --tap-speed: 0.6s;
    --tap-stagger: 0.1s;
    position: relative;
    width: 80px;
    height: 60px;
    margin-left: 80px;
}

.🤚:before {
    content: '';
    display: block;
    width: 180%;
    height: 75%;
    position: absolute;
    top: 70%;
    right: 20%;
    background-color: black;
    border-radius: 40px 10px;
    filter: blur(10px);
    opacity: 0.3;
}

.🌴 {
    display: block;
    width: 100%;
    height: 100%;
    position: absolute;
    top: 0;
    left: 0;
    background-color: var(--skin-color);
    border-radius: 10px 40px;
}

.👍 {
    position: absolute;
    width: 120%;
    height: 38px;
    background-color: var(--skin-color);
    bottom: -18%;
    right: 1%;
    transform-origin: calc(100% - 20px) 20px;
    transform: rotate(-20deg);
    border-radius: 30px 20px 20px 10px;
    border-bottom: 2px solid rgba(0, 0, 0, 0.1);
    border-left: 2px solid rgba(0, 0, 0, 0.1);
}

.👍:after {
    width: 20%;
    height: 60%;
    content: '';
    background-color: rgba(255, 255, 255, 0.3);
    position: absolute;
    bottom: -8%;
    left: 5px;
    border-radius: 60% 10% 10% 30%;
    border-right: 2px solid rgba(0, 0, 0, 0.05);
}

.👉 {
    position: absolute;
    width: 80%;
    height: 35px;
    background-color: var(--skin-color);
    bottom: 32%;
    right: 64%;
    transform-origin: 100% 20px;
    animation-duration: calc(var(--tap-speed) * 2);
    animation-timing-function: ease-in-out;
    animation-iteration-count: infinite;
    transform: rotate(10deg);
}

.👉:before {
    content: '';
    position: absolute;
    width: 140%;
    height: 30px;
    background-color: var(--skin-color);
    bottom: 8%;
    right: 65%;
    transform-origin: calc(100% - 20px) 20px;
    transform: rotate(-60deg);
    border-radius: 20px;
}

.👉:nth-child(1) {
    animation-delay: 0;
    filter: brightness(70%);
    animation-name: tap-upper-1;
}

.👉:nth-child(2) {
    animation-delay: var(--tap-stagger);
    filter: brightness(80%);
    animation-name: tap-upper-2;
}

.👉:nth-child(3) {
    animation-delay: calc(var(--tap-stagger) * 2);
    filter: brightness(90%);
    animation-name: tap-upper-3;
}

.👉:nth-child(4) {
    animation-delay: calc(var(--tap-stagger) * 3);
    filter: brightness(100%);
    animation-name: tap-upper-4;
}

@keyframes tap-upper-1 {

    0%,
    50%,
    100% {
        transform: rotate(10deg) scale(0.4);
    }

    40% {
        transform: rotate(50deg) scale(0.4);
    }
}

@keyframes tap-upper-2 {

    0%,
    50%,
    100% {
        transform: rotate(10deg) scale(0.6);
    }

    40% {
        transform: rotate(50deg) scale(0.6);
    }
}

@keyframes tap-upper-3 {

    0%,
    50%,
    100% {
        transform: rotate(10deg) scale(0.8);
    }

    40% {
        transform: rotate(50deg) scale(0.8);
    }
}

@keyframes tap-upper-4 {

    0%,
    50%,
    100% {
        transform: rotate(10deg) scale(1);
    }

    40% {
        transform: rotate(50deg) scale(1);
    }
}


@media only screen and (max-width:700px) {
    .input {
        width: 95%;
        height: fit-content;
    }

    .form-actions button {
        margin-left: 10px;
        padding: 1rem;
        display: flex;
        justify-content: center;
        align-items: center;
        font-size: 0.9rem;
    }

    .input h2 {
        font-size: 20px;
    }
}
</style>


<script>

import { reactive, onMounted } from 'vue';
import 'animate.css'

export default {
    name: 'app',
    setup() {
        const state = reactive({
            isName: null,
            warning: false,
            showKhodam: false,
            loading: false,
            loadingText: null,
            listKhodam: [
                'Sayur Sop', 'Elang Jawa', 'Gagang Pintu', 'Kucing Pusaka', 'Bantal Guling',
                'Piring Terbang', 'Kecap Manis', 'Helm Kebalik', 'Sapu Lidi', 'Kue Cubit',
                'Telur Dadar', 'Es Cendol', 'Lemari Kaca', 'Jam Dinding', 'Karet Gelang',
                'Kaleng Biskuit', 'Roti Bakar', 'Naga Emas', 'Burung Phoenix', 'Bayangan Hitam',
                'Serigala Malam', 'Elang Jawa', 'Harimau Putih', 'Raja Hutan', 'Mata Petir',
                'Singa Hitam', 'Ratu Ombak', 'Ksatria Baja', 'Angin Selatan', 'Api Biru',
                'Batu Karang', 'Ombak Merah', 'Kuda Terbang', 'Kabut Gunung', 'Lembah Hijau', 'Padang Pasir', 'Bulan Sabit',
                'Badai Pasir', 'Petir Ungu', 'Gunung Es', 'Api Unggun', 'Awan Hitam',
                'Naga Hitam', 'Serigala Putih', 'Harimau Merah', 'Elang Emas', 'Singa Laut',
                'Ombak Biru', 'Petir Merah', 'Pohon Raksasa', 'Badai Petir', 'Awan Merah',
                'Lautan Dalam', 'Gunung Merapi', 'Gagang Pintu', 'Pecel Lele', 'Vespa',' Mie Ayam',
                'Kera Hitam', 'Es Buah'
            ],
            currentKhodam: null,
        })

        function getKhodam(id) {
            let index = Math.floor(Math.random() * id)
            state.currentKhodam = `✨ ${state.listKhodam[index]} ✨`
            console.log(state.currentKhodam)
        }

        function submit() {
            if (state.isName == null) {
                state.warning = true
                state.isName = null
                console.log('Nama masih kosong')
            } else {
                state.showKhodam = true
                state.loading = true
                state.warning = false
                state.loadingText = "Hmm Sebentar..."
                setTimeout(() => {
                    state.loadingText = "Khodam kamu adalah..."
                    setTimeout(() => {
                        getKhodam(state.listKhodam.length)
                        state.loading = false
                        state.loadingText = null
                    }, 2000);
                }, 2000);
            }
        }

        function reset() {
            state.showKhodam = false
            state.isName = null
        }

        onMounted(() => {
            console.log(state.listKhodam.length)
        })
        return {
            state,
            reset,
            submit
        }
    }
}
</script>