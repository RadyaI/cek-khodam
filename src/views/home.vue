<template>
    <div>

        <div class="header">
            <h1>Cek Khodam rorrr</h1>
            <p>By <a href="https://radya.fun" target="_blank">Radya </a> & <a href="https://aryaem.vercel.app"
                    target="_blank">Arya </a></p>
        </div>

        <div class="input">
            <h2>Masukkan nama kamu</h2>
            <form method="post" action="#">
                <div class="form-group">
                    <label for="name">Full Name</label>
                    <input type="text" id="name" name="name">
                </div>

                <div class="form-group">
                    <label for="email">Email Address</label>
                    <input type="email" id="email" name="email">
                </div>

                <div class="form-group">
                    <label for="bio">Bio</label>
                    <textarea id="bio" name="bio" rows="3"></textarea>
                </div>

                <div class="form-actions">
                    <button type="submit">Update Profile</button>
                </div>
            </form>
        </div>

    </div>
</template>


<style scoped>
.header {
    min-height: 150px;
    text-align: center;
    border: 1px solid;

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
    margin: 0 auto;
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
    font-size: 16px;
    letter-spacing: 2px;
    color: #fff;
    font-weight: bold;
    margin-bottom: 1rem;
}

.form-group {
    margin-bottom: 1rem;
}

.form-group label {
    display: block;
    font-size: 0.875rem;
    font-weight: 500;
    color: #6b7280;
}

.form-group input,
.form-group textarea {
    margin-top: 0.25rem;
    padding: 0.5rem;
    width: 100%;
    border: 1px solid #d1d5db;
    border-radius: 0.375rem;
}

.form-actions {
    display: flex;
    justify-content: flex-end;
}

.form-actions button {
    background: linear-gradient(144deg, #af40ff, #5b42f3 50%, #00ddeb);
    color: white;
    padding: 0.5rem 1rem;
    font-weight: bold;
    border-radius: 0.375rem;
    border: none;
    cursor: pointer;
    transition: opacity 0.3s ease;
}

.form-actions button:hover {
    opacity: 0.8;
}
</style>


<script>
export default {
    name: 'app'
}
</script>