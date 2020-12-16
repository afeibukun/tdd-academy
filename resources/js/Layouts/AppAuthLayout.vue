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
                    <div class="flex items-center ml-6">
                        <!-- Desktop Navigation Links -->
                        <ul class="sm:flex sm:items-center">
                            <li>
                                <jet-nav-link :href="route('home')" :active="route().current('home')" class="px-5">
                                    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M7 16l-4-4m0 0l4-4m-4 4h18" />
                                    </svg>
                                    Back
                                </jet-nav-link>
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
        </nav>

        <!-- Page Content -->
        <main>
            <slot></slot>
        </main>

        <!-- Page Footer -->
        <footer class="">
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
                                <a href="#facebook" class="text-white">
                                    <logo-facebook class="h-6 w-6 bg-blue-900 rounded-full box-content p-2" w="1.5rem"
                                                   h="1.5rem"/>
                                </a>
                            </div>
                            <div class="mr-3">
                                <a href="#twitter" class="text-white">
                                    <logo-twitter
                                        class="h-6 w-6 bg-blue-400 rounded-full box-content p-2"
                                        w="1.5rem" h="1.5rem"
                                    />
                                </a>
                            </div>

                            <div class="mr-3">
                                <a href="#instagram" class="text-white">
                                    <logo-instagram class="h-6 w-6 bg-pink-400 rounded-full box-content p-2" w="1.5rem"
                                                    h="1.5rem" />
                                </a>
                            </div>
                            <div>
                                <a href="#youtube" class="text-white">
                                    <logo-youtube class="h-6 w-6 bg-red-600 rounded-full box-content p-2" w="1.5rem"
                                                  h="1.5rem"/>
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
