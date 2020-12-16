<template>
    <app-auth-layout>
        <div>
            <div>
                <div>
                    <div class="py-12">
                        <div class="max-w-7xl mx-auto sm:px-6 lg:px-8">
                            <div>
                                <div class="sm:flex justify-between">
                                    <!-- Form Section -->
                                    <div>
                                        <div>
                                            <div>
                                                <h3 class="text-3xl text-gray-300">Create a New Account</h3>
                                            </div>
                                            <div>
                                                <form>
                                                    <div>
                                                        <label class="block">Your Name</label>
                                                        <input type="text" v-model="userData.name" />
                                                    </div>
                                                    <div>
                                                        <label>Your Email</label>
                                                        <input type="email" v-model="userData.email" />
                                                    </div>
                                                    <div>
                                                        <label>Your Phone Number</label>
                                                        <input type="tel" v-model="userData.phone" />
                                                    </div>
                                                    <div>
                                                        <label>Password</label>
                                                        <input type="password" v-model="userData.password" />
                                                    </div>
                                                    <div>
                                                        <label>Retype Password</label>
                                                        <input type="password" v-model="userData.confirm_password" />
                                                    </div>
                                                </form>
                                            </div>
                                        </div>
                                    </div>
                                    <!-- Side Image Section -->
                                    <div class="sm:hidden">

                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

    </app-auth-layout>
</template>

<script>
    import AppAuthLayout from '@/Layouts/AppAuthLayout'
    export default {
        name: "Register",
        components: {
            AppAuthLayout,
        },
        data(){
            return{
                userData:{
                    name:null,
                    email:null,
                    phone:null,
                    password: null,
                    confirm_password: null
                }
            }
        }
    }
</script>

<style scoped>

</style>
