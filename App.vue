<template>
  <main>
    <header>
      <nav>
        <button @click="changeChannel(i)" v-for="i in 15" :key="i">
          CH {{ i }}
        </button>
      </nav>
    </header>
    <section>
      <iframe
        frameborder="0"
        marginheight="0"
        marginwidth="0"
        height="600"
        allowfullscreen="true"
        :src="`http://uhdstreams.club/footy/ch${activeChannel}.php`"
        scrolling="no"
        width="900"
        >Your browser does not support iframes</iframe
      >
    </section>
  </main>
</template>

<script lang="ts" setup>
useMeta({
  title: "Soccer Tv",
});

const activeChannel = ref(1);

function changeChannel(channel: number) {
  activeChannel.value = channel;
}
</script>
