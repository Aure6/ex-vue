<script setup></script>
<template>
    <!-- <div :class="`text-${levelToSize[level]} font-bold`">
        <slot></slot>
                                                    </div> -->
    <div :class="getTitleClass">
        <slot></slot>
    </div>
</template>

<script>
export default {
    props: {
        level: {
            type: String,
            required: true,
            validator: value => ['h1', 'h2', 'h3', 'h4', 'h5', 'h6'].includes(value)
        }
    },
    computed: {
        getTitleClass() {
            // return `text-${this.level} font-bold`;

            // Utilisez les classes TailwindCSS en fonction du type de bouton
            // return {
            //     h1: '5xl',
            //     h2: '4xl',
            //     h3: '3xl',
            //     h4: '2xl',
            //     h5: 'xl',
            //     h6: 'lg',
            //     // Ajoutez d'autres classes selon vos besoins
            // };

            // Utilisez les classes TailwindCSS en fonction du type de bouton
            return {
                'text-5xl	': this.level === 'h1',
                'text-4xl': this.level === 'h2',
                'text-3xl': this.level === 'h3',
                'text-2xl': this.level === 'h4',
                'text-xl': this.level === 'h5',
                'text-lg': this.level === 'h6',
                'text-lg': this.level === 'default',
                // Ajoutez d'autres classes selon vos besoins
            };
        }
    }
};

</script>