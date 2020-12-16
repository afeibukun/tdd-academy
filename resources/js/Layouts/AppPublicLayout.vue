<template>
    <div class="min-h-screen w-full">
        <public-navbar></public-navbar>

        <main>
        <!-- Page Heading -->
        <header class="bg-blue-100">
            <div class="container mx-auto py-20 px-4 sm:px-6 lg:px-8">
                <slot name="header"></slot>
            </div>
        </header>

        <!-- Page Content -->
        <section>
            <slot></slot>
        </section>
        </main>
        <!-- Page Footer -->
        <public-footer></public-footer>
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
    import PublicNavbar from "@/Components/PublicNavbar";
    import PublicFooter from "@/Components/PublicFooter";

    export default {
        components: {
            PublicFooter,
            PublicNavbar,
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
