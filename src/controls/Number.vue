<template>
    <div class="form-field">
        <div class="label form-label">{{property.title}}</div>
        <div class="form-control">
        <b-input type="number"
            :placeholder="property.placeholder"
            :min="property.min"
            :max="property.max"
            v-model="value">
        </b-input>
        </div>
    </div>
</template>
<script>
import Vue from 'vue';
export default {
    name: 'form-control-number',

    props: {
        node: Object,
        property: Object
    },

    data() {
        return {
            value: ''
        };
    },

    mounted() {
        this.value = this.node.data[this.property.name];
    }
};
</script>
