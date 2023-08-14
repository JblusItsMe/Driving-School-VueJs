<template>

    <footer class="bg-white dark:bg-gray-900" style="background: #11101d">
        <div class="mx-auto w-full max-w-screen-xl p-4 py-6 lg:py-8">
            <div class="md:flex md:justify-between">
                <div class="mb-6 md:mb-0">
					<RouterLink to="/" class="flex item-center">
                        <img src="./../../public/favicon.ico" class="h-8 mr-3" alt="FlowBite Logo" />
                        <span class="self-center text-2xl font-semibold whitespace-nowrap dark:text-white">Driving School</span>
					</RouterLink>
                </div>
                <div class="grid grid-cols-2 gap-8 sm:gap-6 sm:grid-cols-3">
                    <div>
                        <h2 class="mb-6 text-sm font-semibold text-gray-900 uppercase dark:text-white">SCHEDULES</h2>
                        <ul class="text-gray-500 dark:text-gray-400 font-medium">
                            <li class="mb-4">
								<RouterLink to="/" class="hover:underline">18h-19h</RouterLink>
                            </li>
                        </ul>
                    </div>
                    <div>
                        <h2 class="mb-6 text-sm font-semibold text-gray-900 uppercase dark:text-white">Contact</h2>
                        <ul class="text-gray-500 dark:text-gray-400 font-medium">
                            <li class="mb-4">
                                <RouterLink to="/" class="hover:underline">202 XXX XXXX</RouterLink>
                            </li>
                            <li class="mb-4">
                                <RouterLink to="/" class="hover:underline">contact@drivingschool.best</RouterLink>
                            </li>
                            <li class="mb-4">
                                <RouterLink to="/" class="hover:underline">2444 Linden Boulevard</RouterLink>
                            </li>
                        </ul>
                    </div>
                    <div>
                        <h2 class="mb-6 text-sm font-semibold text-gray-900 uppercase dark:text-white">Legal</h2>
                        <ul class="text-gray-500 dark:text-gray-400 font-medium">
                            <li class="mb-4">
                                <RouterLink to="/" class="hover:underline">Privacy Policy</RouterLink>
                            </li>
                            <li>
                                <RouterLink to="/" class="hover:underline">Terms &amp; Conditions</RouterLink>
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
            <hr class="my-6 border-gray-200 sm:mx-auto dark:border-gray-700 lg:my-8" />
            <div class="sm:flex sm:items-center sm:justify-between">
          <span class="text-sm text-gray-500 sm:text-center dark:text-gray-400">© 2023 <RouterLink to="/" class="hover:underline">Driving School™</RouterLink>. All Rights Reserved.
          </span>
            </div>
        </div>
    </footer>

</template>

<script>
import Contact from "@/components/Contact.vue";

export default {
    name: "Footer",
    components: {Contact}
}
</script>

<style scoped>

</style>