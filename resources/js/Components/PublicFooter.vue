<template>
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
                                <ion-icon name="logo-facebook" class="h-6 w-6"></ion-icon>
                            </a>
                        </div>
                        <div class="mr-3">
                            <a href="#twitter" class="text-blue-400">
                                <ion-icon name="logo-twitter" class="h-6 w-6"></ion-icon>
                            </a>
                        </div>

                        <div class="mr-3">
                            <a href="#instagram" class="text-pink-400">
                                <ion-icon name="logo-instagram" class="h-6 w-6"></ion-icon>
                            </a>
                        </div>
                        <div>
                            <a href="#youtube" class="text-red-600">
                                <ion-icon name="logo-youtube" class="h-6 w-6"></ion-icon>
                            </a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </footer>

</template>

<script>
    export default {
        name: "PublicFooter"
    }
</script>

<style scoped>

</style>
