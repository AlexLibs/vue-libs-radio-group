<template>
    <div class="vue-libs-radio-group">
        <template v-for="(label, id) in options">
            <input type="radio" v-bind:value="id" v-model="model" v-bind:id="id">
            <label class="btn btn-primary" v-bind:for="id">
                {{label}}
            </label>
        </template>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                model: this.value,
            };
        },
        props: [
            'options',
            'value',
        ],
        methods: {
        },
        components: {},
        watch: {
            model: function(){
                this.$emit('input', this.model)
            }
        }
    }
</script>

<style>
    .vue-libs-radio-group {
        padding: 8px 0;
        border: 1px solid #dc0606;
        border-radius: 30px;
        display: inline-block;
    }
    .vue-libs-radio-group input[type="radio"] {
        display: none;
    }
    .vue-libs-radio-group label {
        border-right: 1px solid #dc0606;
        cursor: pointer;
        padding: 9px;
    }
    .vue-libs-radio-group label:last-child {
        border-right: none;
        margin-right: -4px;
        border-radius: 0 30px 30px 0;
    }
    .vue-libs-radio-group label:first-of-type {
        border-radius: 30px 0 0 30px;
    }
    .vue-libs-radio-group input[type="radio"]:checked + label {
        color: white;
        background-color: #dc0606;
    }
</style>