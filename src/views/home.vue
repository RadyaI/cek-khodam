<template>
    <div>

        <!-- Header -->
        <div class="header">
            <h1>Cek Khodam rorrr</h1>
            <p>By <a href="https://radya.fun" target="_blank">Radyaif </a> & <a href="https://aryaem.vercel.app"
                    target="_blank">Aryaem </a></p>
        </div>

        <div class="input">
            <h2>Masukkan nama kamu</h2>
            <form>
                <div class="wrap">
                    <div class="form-group">
                        <input type="text" id="name" name="name" autocomplete="off">
                    </div>
                    <div class="form-actions">
                        <button type="submit">Cek</button>
                    </div>
                </div>
            </form>
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
    max-width: 28rem;
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
    padding: 2rem;
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
    margin-right: 15px;
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

@media only screen and (max-width:700px) {
    .input {
        width: 95%;
        height: fit-content;
    }

    .form-actions button {
        margin-left: 10px;
    }

    .input h2{
        font-size: 20px;
    }
}
</style>


<script>
export default {
    name: 'app'
}
</script>