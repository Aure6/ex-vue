<script setup></script>
<template>
    <button class="p-4 bg-slate-200" :class="buttonClasses">
        <slot></slot>

    </button>
</template>

<script>
export default {
    props: {
        type: {
            type: String,
            default: "default", // Valeur par défaut pour le type de bouton
        },
    },
    computed: {
        buttonClasses() {
            // Utilisez les classes TailwindCSS en fonction du type de bouton
            return {
                'bg-blue-500 text-white': this.type === 'primary',
                'bg-green-500 text-white': this.type === 'success',
                'bg-red-500 text-white': this.type === 'danger',
                'bg-gray-500 text-white': this.type === 'secondary',
                'bg-gray-300 text-gray-700': this.type === 'default',
                // Ajoutez d'autres classes selon vos besoins
            };
        },
    },
};
</script>