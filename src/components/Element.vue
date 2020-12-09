<template>
    <div class="component">
        <div class='block' :style="{'background-color':color}" :data-name=name></div>
        <input class="input" type="range" name="" id="input" min="100" max="300" :data-name=name @input="changeHeight($event.target.value)">
    </div>
</template>

<script>
export default {
    name: 'Element',
    props: {
        color: String,
        name: String
    },
    methods: {
        changeHeight(value) {
            document.querySelector(`div[data-name="${this.name}"]`).style.height = value + `px`;
        }
    }
}
</script>

<style>
    .input {
        transform: rotate(270deg);
    }
    .component {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: flex-end;
        height: 450px;
    }
    .block {
        margin-bottom: 100px;
        width: 100px;
        height: 100px;
        border-radius: 10px;
        border: 2px solid black;
    }
</style>