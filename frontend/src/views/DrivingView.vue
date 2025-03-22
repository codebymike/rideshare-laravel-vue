<script setup>

</script>
<template>
    <div class="pt-16">
        <h1 class="text-3xl font-semibold mb-4"> title </h1>
        <div>
            <div class="overflow-hidden shadow sm:rounded-md max-w-sm mx-auto text-left" v-if="!trip.is_complete">
                <div class="bg-white px-4 py-5 sm:p-6">
                    <div>
                        Gmap
                    </div>
                    <div class="mt-2">
                        <p class="text-xl">Going to <strong>pick up a passenger</strong></p>
                    </div>
                </div>
                <div class="bg-gray-50 px-4 py-3 text-right sm:px-6">
                    <button v-if="trip.is_started"
                        @click="handleCompleteTrip"
                        class="inline-flex justify-center rounded-md border border-transparent bg-black py-2 px-4 text-sm font-medium text-white shadow-sm hover:bg-gray-600 focus:outline-none">
                        Complete Trip</button>
                    <button v-else
                        @click="handlePassengerPickedUp"
                        class="inline-flex justify-center rounded-md border border-transparent bg-black py-2 px-4 text-sm font-medium text-white shadow-sm hover:bg-gray-600 focus:outline-none">
                        Passenger Picked Up</button>
                </div>
            </div>
            <div class="overflow-hidden shadow sm:rounded-md max-w-sm mx-auto text-left" v-else>
                <div class="bg-white px-4 py-5 sm:p-6">
                    <Tada />
                </div>
            </div>
        </div>
    </div>
</template>