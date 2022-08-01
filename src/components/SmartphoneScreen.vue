<template>
    <div class="note-screen light-mode">
        
    </div>
</template>

<script>
export default {
  name: 'SmartphoneScreen'
}
</script>

<style>
/*Screen*/
.light-mode {
    background-image: url('/src/assets/light-mode.jpeg');
}
.dark-mode {
    background-image: url('/src/assets/dark-mode.jpeg');
}
.note-screen {
    display: flex;
    align-items: center;
    flex-direction: column;
    position: relative;
    cursor: context-menu;
    width: 97%;
    border-radius: 15px;
    height: 98%;
    background-attachment: fixed;
    background-size: contain;
    background-position: center;
}
</style>