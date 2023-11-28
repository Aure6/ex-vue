<template>
    <div>
        <autocomplete-select :options="selectOptions" @select="handleSelect"></autocomplete-select>
    </div>
</template>

<script estup>
import AutocompleteSelect from './AutocompleteSelectComponent.vue';

export default {
    components: {
        AutocompleteSelect,
    },
    data() {
        return {
            selectOptions: [
                { value: 'option1', label: 'Option 1' },
                { value: 'option2', label: 'Option 2' },
                // ... autres options
            ],
        };
    },
    methods: {
        handleSelect(selectedValue) {
            console.log('Option sélectionnée :', selectedValue);
        },
    },
};
</script>
