<template>
    <inertia-link :href="href" :class="classes">
        <slot></slot>
    </inertia-link>
</template>

<script>
    export default {
        props: ['href', 'active'],

        computed: {
            classes() {
                return this.active
                            ?
                    'inline-flex items-center px-1 pt-1 border-b-2 border-blue-300 text-sm font-medium leading-5 text-blue-900 focus:outline-none focus:border-blue-900 transition duration-150 ease-in-out'
                            :
                    'inline-flex items-center px-1 pt-1 border-b-2 border-transparent text-sm font-medium leading-5 text-blue-600 hover:text-blue-800 hover:border-blue-300 focus:outline-none focus:text-blue-700 focus:border-blue-400 transition duration-150 ease-in-out'
            }
        }
    }
</script>
