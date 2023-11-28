<template>
    <div>
        <label for="autocomplete">Recherche :</label>
        <input type="text" id="autocomplete" v-model="searchTerm" @input="filterOptions" />

        <select v-model="selectedOption" @change="$emit('select', selectedOption)">
            <option v-for="option in filteredOptions" :key="option.value" :value="option.value">
                {{ option.label }}
            </option>
        </select>
    </div>
</template>

<script setupc>
import { ref, watch } from 'vue';

export default {
    props: {
        options: {
            type: Array,
            required: true,
        },
    },
    emits: ['select'],
    setup(props) {
        const searchTerm = ref('');
        const selectedOption = ref(null);

        const filteredOptions = ref(props.options);

        const filterOptions = () => {
            const search = searchTerm.value.toLowerCase();
            filteredOptions.value = props.options.filter(
                (option) => option.label.toLowerCase().includes(search)
            );
        };

        watch(searchTerm, filterOptions);

        return {
            searchTerm,
            selectedOption,
            filteredOptions,
        };
    },
};
</script>