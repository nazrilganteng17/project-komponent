<template>
    <div v-if="umur > 18">
        <p>Selamat Datang {{ nama }}</p>
    </div>
    <div v-else>
        <p>Maaf Kamu Belum Cukup Umur</p>
    </div>
    <button @click="greet">Sapa</button>
</template>
<script>
export default {
    props: ['nama', 'umur'],
    methods: {
        greet() {
            alert("Haloo " + this.nama);
        }
    },
}
</script>