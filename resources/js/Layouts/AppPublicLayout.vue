<template>
    <div class="min-h-screen bg-gray-800 w-full">
        <nav class="relative">
            <!-- Primary Navigation Menu -->
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-3">
                <div class="flex justify-between items-center h-16">
                    <!-- Right hand Side -->
                    <div class="flex justify-start">
                        <!-- Logo -->
                        <div class="flex-shrink flex items-center">
                            <inertia-link :href="route('home')" class="">
                                <img class="h-16 w-auto" src="/img/tdd-logo-white.png" alt="Logo">
                            </inertia-link>
                        </div>
                    </div>

                    <!-- Left hand Side -->
                    <div class="hidden sm:flex sm:items-center sm:ml-6">
                        <!-- Desktop Navigation Links -->
                        <ul class="sm:flex sm:items-center">
                            <li>
                                <jet-nav-link :href="route('home')" :active="route().current('home')" class="px-5">Home
                                </jet-nav-link>
                            </li>
                            <li>
                                <jet-nav-link href="#menu-1" class="px-5">Menu 1
                                </jet-nav-link>
                            </li>
                            <li>
                                <jet-nav-link href="#menu-2" class="px-5">Menu 2
                                </jet-nav-link>
                            </li>
                            <li >
                                <jet-nav-link href="#menu-3" class="px-5">Menu 3
                                </jet-nav-link>
                            </li>
                        </ul>
                    </div>

                    <!-- Hamburger -->
                    <div class="-mr-2 flex items-center sm:hidden">
                        <!-- Menu Toggle Button -->
                        <button type="button" @click="showingNavigationDropdown = ! showingNavigationDropdown"
                                class="inline-flex items-center justify-center p-2 rounded-md text-gray-400 hover:text-gray-500 hover:bg-gray-700 focus:outline-none focus:bg-gray-900 focus:text-gray-500 transition duration-150 ease-in-out">
                            <svg class="h-6 w-6" stroke="currentColor" fill="none" viewBox="0 0 24 24">
                                <path :class="{'hidden': showingNavigationDropdown, 'inline-flex': ! showingNavigationDropdown }" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
                                <path :class="{'hidden': ! showingNavigationDropdown, 'inline-flex': showingNavigationDropdown }" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
                            </svg>
                        </button>
                    </div>
                </div>
            </div>

            <!-- Responsive Navigation Menu -->
            <div :class="{'block': showingNavigationDropdown, 'hidden': ! showingNavigationDropdown}"
                 class="sm:hidden absolute w-full inset-x-0 transition transform bg-gray-800 shadow-lg">
                <div class="pt-2 pb-3 space-y-1 shadow">
                    <ul>
                        <li>
                            <jet-responsive-nav-link :href="route('home')" :active="route().current('home')">
                                Home
                            </jet-responsive-nav-link>
                        </li>
                        <li>
                            <jet-responsive-nav-link href="#menu-1">
                                Menu 1
                            </jet-responsive-nav-link>
                        </li>
                        <li>
                            <jet-responsive-nav-link href="#menu-2">
                                Menu 2
                            </jet-responsive-nav-link>
                        </li>
                        <li>
                            <jet-responsive-nav-link href="#menu-3">
                                Menu 3
                            </jet-responsive-nav-link>
                        </li>
                    </ul>
                </div>
            </div>
        </nav>

        <!-- Page Heading -->
        <header class="shadow">
            <div class="max-w-7xl mx-auto py-6 px-4 sm:px-6 lg:px-8">
                <slot name="header"></slot>
            </div>
        </header>

        <!-- Page Content -->
        <main>
            <slot></slot>
        </main>

        <!-- Page Footer -->
        <footer class="bg-black">
            <div class="max-w-7xl mx-auto py-6 px-4 sm:px-6 lg:px-8">
                <slot name="footer"></slot>
                <div class="sm:flex justify-between">
                    <div>
                        <!-- Footer Links and Credit -->
                        <div class="sm:flex text-center sm:text-justify">
                            <div class="sm:mr-5">
                                <p class="text-gray-200">Copyright &copy; 2020 | All rights reserved |
                                    <inertia-link href="https://desdistrict.com" title="The Design District">Desdistrict</inertia-link>
                                </p>
                            </div>
                            <div class="sm:mr-5">
                                <inertia-link class="text-gray-200" href="#terms" title="Terms of Use">Terms of Use
                                </inertia-link>
                            </div>
                            <div>
                                <inertia-link class="text-gray-200" href="#faqs" title="Frequently asked Questions">FAQs
                                </inertia-link>
                            </div>
                        </div>
                    </div>
                    <div class="text-center sm:text-justify">
                        <!-- Social -->
                        <div class="flex items-center justify-center sm:justify-content">
                            <div class="mr-3">
                                <a href="#facebook" class="text-blue-900">
                                    <logo-facebook class="h-6 w-6" w="1.5rem" h="1.5rem"/>
                                </a>
                            </div>
                            <div class="mr-3">
                                <a href="#twitter" class="text-blue-400">
                                    <logo-twitter w="1.5rem" h="1.5rem" />
                                </a>
                            </div>

                            <div class="mr-3">
                                <a href="#instagram" class="text-pink-400">
                                    <logo-instagram class="h-6 w-6" w="1.5rem" h="1.5rem" />
                                </a>
                            </div>
                            <div>
                                <a href="#youtube" class="text-red-600">
                                    <logo-youtube class="h-6 w-6" w="1.5rem" h="1.5rem"/>
                                </a>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </footer>

        <!-- Modal Portal -->
        <portal-target name="modal" multiple>
        </portal-target>
    </div>
</template>

<script>
    import JetApplicationMark from '@/Jetstream/ApplicationMark'
    import JetDropdown from '@/Jetstream/Dropdown'
    import JetDropdownLink from '@/Jetstream/DropdownLink'
    import JetNavLink from '@/Jetstream/NavLink'
    import JetResponsiveNavLink from '@/Jetstream/ResponsiveNavLink'
    import LogoFacebook from 'vue-ionicons/dist/logo-facebook.vue'
    import LogoTwitter from 'vue-ionicons/dist/logo-twitter.vue'
    import LogoInstagram from 'vue-ionicons/dist/logo-instagram.vue'
    import LogoYoutube from 'vue-ionicons/dist/logo-youtube.vue'

    export default {
        components: {
            JetApplicationMark,
            JetDropdown,
            JetDropdownLink,
            JetNavLink,
            JetResponsiveNavLink,
            LogoFacebook,
            LogoTwitter,
            LogoInstagram,
            LogoYoutube,
        },

        data() {
            return {
                showingNavigationDropdown: false,
            }
        },

        methods: {
            switchToTeam(team) {
                this.$inertia.put(route('current-team.update'), {
                    'team_id': team.id
                }, {
                    preserveState: false
                })
            },

            logout() {
                axios.post(route('logout').url()).then(response => {
                    window.location = '/';
                })
            },
        }
    }
</script>
