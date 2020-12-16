<template>
    <app-public-layout>
        <template #header>
            <div class="relative pt-10 pb-10 flex content-center items-center justify-center">
                <div class="">
                    <div class="py-10 sm:py-10">
                        <div class="flex justify-between items-center">
                            <div class="sm:w-6/12 w-full">
                                <h2 class="font-semibold text-3xl sm:text-5xl  text-gray-400 leading-tight mb-5">
                                    <span class="block xl:inline">Acquire relevant</span>
                                    <span class="block text-yellow-400 xl:inline">digital skills</span>
                                </h2>
                                <p class="text-gray-700 mb-10">
                                    The Desdistrict Academy provides world class digital learning content to help
                                    learners improve their skills and be ready to provide value.
                                </p>
                                <div class="flex items-center justify-start">
                                    <div class="rounded-md">
                                        <inertia-link href="/register"
                                                      class="w-full flex items-center justify-center px-8 py-2 border border-transparent font-medium rounded-md text-white bg-blue-800 hover:bg-blue-900 hover:shadow-lg text-sm md:text-lg md:px-10">
                                            Get Started
                                        </inertia-link>
                                    </div>
                                    <div class="rounded-md ml-3">
                                        <inertia-link href="#Learn-More"
                                                      class="w-full flex items-center justify-center px-8 py-2 border border-transparent text-sm font-medium rounded-md text-blue-700 bg-blue-200 hover:bg-blue-300 hover:text-blue-900 hover:shadow-lg  md:text-lg md:px-10">
                                            Learn More
                                        </inertia-link>
                                    </div>
                                </div>
                            </div>
                            <div class="hidden sm:block">
                                <div>
                                    <img src="/img/elearning-illustration.svg">

                                </div>
                            </div>
                        </div>

                    </div>
                </div>
            </div>
        </template>

        <div>
            <div>
                <div>
                    <!-- featured section -->
                    <div class="pb-12 bg-blue-100">
                        <div class="container mx-auto sm:px-6 lg:px-8">
                            <div class="overflow-hidden mb-10">
                                <div class="sm:flex justify-between item-center">
                                    <div class="sm:w-1/3 w-full">
                                        <div
                                            class="sm:rounded-md shadow sm:shadow-lg px-5 py-10 bg-gradient-to-r from-gray-900 to-gray-800 h-full">
                                            <div>
                                                <ion-icon name="layers-outline"
                                                          class="h-10 w-10 text-gray-400"></ion-icon>
                                            </div>
                                            <div class="mt-5">
                                                <h3 class="text-gray-200 text-lg">Up-to-date and Relevant Course
                                                    Materials </h3>
                                            </div>
                                        </div>
                                    </div>
                                    <div class="sm:w-1/3 w-full">
                                        <div
                                            class="sm:rounded-md shadow sm:shadow-lg px-5 py-10 bg-gradient-to-r from-gray-900 to-gray-800 h-full sm:mx-5">
                                            <div>
                                                <ion-icon name="rocket-outline" class="h-10 w-10 text-gray-400"></ion-icon>
                                            </div>
                                            <div class="mt-5">
                                                <h3 class="text-gray-200 text-lg">Top-Notch Learning Support Services</h3>
                                            </div>
                                        </div>
                                    </div>
                                    <div class="sm:w-1/3 w-full">
                                        <div
                                            class="sm:rounded-md shadow sm:shadow-lg px-5 py-10 bg-gradient-to-r from-gray-900 to-gray-800 h-full">
                                            <div>
                                                <ion-icon name="desktop-outline" class="h-10 w-10 text-gray-400"></ion-icon>
                                            </div>
                                            <div class="mt-5">
                                                <h3 class="text-gray-200 text-lg">Interactive and Remarkable Learning Experience</h3>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                    <!-- CTA Section -->
                    <div class="py-20 bg-gray-900">
                        <div class="container mx-auto px-4 sm:px-6 lg:px-8 py-15">
                            <div class="sm:flex items-center justify-between">
                                <div class="sm:w-5/12">
                                    <div>
                                        <div>
                                            <h2 class="text-3xl sm:text-5xl text-gray-100 font-bold">
                                                Ready to begin your digital up-skill journey?
                                            </h2>
                                        </div>
                                        <div>
                                            <p class="text-gray-300">

                                            </p>
                                        </div>
                                    </div>
                                </div>
                                <div class="mt-3 sm:mt-0">
                                    <div class="rounded-md shadow">
                                        <inertia-link href="/register"
                                                      class="w-full flex items-center justify-center px-8 py-3 border border-transparent text-base font-medium rounded-md text-white bg-blue-800 hover:bg-blue-900 md:py-4 md:text-lg md:px-10">
                                            Get Started
                                        </inertia-link>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </app-public-layout>
</template>

<script>
    import AppPublicLayout from '@/Layouts/AppPublicLayout'
    import Welcome from '@/Jetstream/Welcome'

    export default {
        components: {
            AppPublicLayout,
            Welcome,
        },
    }
</script>
