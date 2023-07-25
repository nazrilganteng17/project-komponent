<template>
    <div>
        <Header text="Ini Adalah Header">
            <template #footer>
                <p>Ini Adalah Slot Dari Footer</p>
            </template>
        </Header>
        <my-component nama="Ujang" umur="90">
        </my-component>
        <latihan-component nama="Mahmud" umur="19"></latihan-component>
        <latihan-dua-component></latihan-dua-component>
        <h2>WatchersComponent</h2>
        <watchers-component nama="Ujang" umur="80">
        </watchers-component>
        <h2>Event Component</h2>
        <latihan-event-component :nama="nama" :umur="umur" @greeted="onGreeted">
            <template #footer>
                <div>
                    <p>Ini Adalah Footer Latihan Event</p>
                </div>
            </template>
            <template #header>
                <div>
                    <p>Ini Adalah Header latihan Event</p>
                </div>
            </template>
        </latihan-event-component>
    </div>
</template>

<script setup>
import LatihanEventComponent from '@/components/LatihanEventComponent.vue'
import LatihanComponent from './LatihanComponent.vue';
import MyComponent from './MyComponent.vue';
import Header from './Header.vue';
import LatihanDuaComponent from './LatihanDuaComponent.vue';
import WatchersComponent from './WatchersComponent.vue';

// event
import { ref } from 'vue';
const nama = ref('John');
const umur = ref(25);

const onGreeted = () => {
    console.log('Kamu udah disapa, bro!');
};

</script>