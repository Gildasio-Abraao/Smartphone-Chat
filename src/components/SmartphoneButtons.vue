<template>
    <div class="botoes">
        <div class="vol"></div>
        <div class="power"></div>
    </div>
</template>

<script>
export default {
  name: 'SmartphoneButtons'
}
</script>

<style scoped>
/*buttons*/
.botoes {
    position: absolute;
    margin-top: 105px;
    margin-left: 285px;
}
.vol {
    width: 4px;
    height: 75px;
    border-top-right-radius: 20px;
    border-bottom-right-radius: 20px;
    background-color: #191818;
    cursor: pointer;
}
.power {
    width: 4px;
    height: 30px;
    background-color: #191818;
    border-top-right-radius: 20px;
    border-bottom-right-radius: 20px;
    margin-top: 20px;
    cursor: pointer;
}
</style>