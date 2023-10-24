<template>
 <Sidebar/>
 <HelloWorld/>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '../components/HelloWorld.vue';
import Sidebar from '../components/Sidebar.vue';

export default defineComponent({
  name: 'HomeView',
  components: {
    HelloWorld,
    Sidebar
  },
});
</script>
