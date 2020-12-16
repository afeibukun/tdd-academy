<template>
    <nav
        class="top-0 absolute z-50 w-full flex flex-wrap items-center justify-between px-2 py-3 navbar-expand-lg"
    >
        <!-- Navbar content -->
        <div
            class="container px-4 mx-auto flex flex-wrap items-center justify-between"
        >
            <div class="w-full relative flex justify-between lg:w-auto lg:static lg:block lg:justify-start">
                <inertia-link :href="route('home')" class="">
                    <img class="h-10 md:h-16 w-auto" src="/img/tdd-logo-coloured.png" alt="Logo">
                </inertia-link>
                <button
                class="cursor-pointer text-xl leading-none px-3 py-1 border border-solid border-transparent rounded bg-transparent block lg:hidden outline-none focus:outline-none"
                type="button"
                v-on:click="toggleNavbar()"
                >
                    <ion-icon name="menu-outline" class="text-blue-800"></ion-icon>
                </button>
            </div>
            <div
                class="lg:flex flex-grow items-center bg-white lg:bg-transparent lg:shadow-none"
                v-bind:class="{'hidden': !showMenu, 'block': showMenu}"
            >
                <ul class="flex flex-col lg:flex-row list-none lg:ml-auto">
                    <li class="flex items-center">
                        <jet-nav-link :href="route('home')" :active="route().current('home')"
                                      class="px-3 py-4 lg:py-2 flex items-center text-xs uppercase font-bold">Home
                        </jet-nav-link>

                    </li>

                    <li class="flex items-center">
                        <jet-nav-link href="#explore" class="px-3 py-4 lg:py-2 flex items-center text-xs uppercase font-bold">Explore
                        </jet-nav-link>
                    </li>
                    <li class="flex items-center">
                        <jet-nav-link href="#Partner" class="px-3 py-4 lg:py-2 flex items-center text-xs uppercase font-bold">Partner
                        </jet-nav-link>
                    </li>
                    <li class="flex items-center">
                        <jet-nav-link href="#search"
                                      class="px-3 py-4 lg:py-2 flex items-center text-xs uppercase font-bold">
                            <ion-icon name="search-outline"></ion-icon>
                        </jet-nav-link>
                    </li>
                    <li class="flex items-center">
                        <jet-nav-link href="#sign-in"
                                      class="px-3 py-4 lg:py-2 flex items-center text-xs uppercase font-bold">Sign In
                        </jet-nav-link>
                    </li>

                    <li class="flex items-center">
                        <jet-nav-link href="#sign-up"
                                      class="px-3 py-4 lg:py-2 flex items-center text-xs uppercase font-bold">Sign Up
                        </jet-nav-link>
                    </li>
                </ul>
            </div>
        </div>
    </nav>
</template>

<script>
    import JetNavLink from '@/Jetstream/NavLink'
    import JetResponsiveNavLink from '@/Jetstream/ResponsiveNavLink'
    export default {
        name: "PublicNavbar",
        components:{
            JetNavLink,
            JetResponsiveNavLink,
        },
        data() {
            return {
                showMenu: false
            }
        },
        methods: {
            toggleNavbar: function(){
                this.showMenu = !this.showMenu;
            }
        }
    }
</script>

<style scoped>

</style>
