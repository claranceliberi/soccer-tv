<template>
  <main>
    <header>
      <nav>
        <button @click="changeChannel(1)">CH 1</button>
        <button @click="changeChannel(2)">CH 2</button>
        <button @click="changeChannel(3)">CH 3</button>
        <button @click="changeChannel(4)">CH 4</button>
        <button @click="changeChannel(5)">CH 5</button>
        <button @click="changeChannel(6)">CH 6</button>
        <button @click="changeChannel(7)">CH 7</button>
        <button @click="changeChannel(8)">CH 8</button>
        <button @click="changeChannel(9)">CH 9</button>
        <button @click="changeChannel(10)">CH 10</button>
        <button @click="changeChannel(11)">CH 11</button>
        <button @click="changeChannel(12)">CH 12</button>
        <button @click="changeChannel(13)">CH 13</button>
        <button @click="changeChannel(14)">CH 14</button>
        <button @click="changeChannel(15)">CH 15</button>
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
const activeChannel = ref(1);

function changeChannel(channel: number) {
  activeChannel.value = channel;
}
</script>
