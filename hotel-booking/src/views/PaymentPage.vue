<template>
  <div>
    <!-- <div> -->
    <!-- <iframe v-if="invoiceUrl" width="1000" height="1000" :src="invoiceUrl" frameborder="0"></iframe> -->
    <!-- </div> -->
    <div
      class="p-4 max-w-md bg-white rounded-lg border shadow-md sm:p-8 dark:bg-gray-800 dark:border-gray-700"
    >
      <div class="flex justify-between items-center mb-4">
        <h5 class="text-xl font-bold leading-none text-gray-900 dark:text-white">
          Booked Ballrooms
        </h5>
        <!-- <a href="#" class="text-sm font-medium text-blue-600 hover:underline dark:text-blue-500">
          View all
        </a> -->
      </div>
      <div class="flow-root">
        <ul role="list" class="divide-y divide-gray-200 dark:divide-gray-700">
          <BookingList
            v-for="each in bookedBallroom"
            :key="each.id"
            :each="each"
            class="py-3 sm:py-4"
          >
            <!-- <div class="flex items-center space-x-4">
              <div class="flex-shrink-0"></div>
              <div class="flex-1 min-w-0">
                <p class="text-sm font-medium text-gray-900 truncate dark:text-white">
                  {{ each.name }}
                </p>
                <p class="text-sm text-gray-500 truncate dark:text-gray-400">email@windster.com</p>
              </div>
              <div
                class="inline-flex items-center text-base font-semibold text-gray-900 dark:text-white"
              >
                {{ each.price }}
              </div>
            </div> -->
          </BookingList>
          <!-- <li class="py-3 sm:py-4">
            <div class="flex items-center space-x-4">
              <div class="flex-shrink-0">
                <img
                  class="w-8 h-8 rounded-full"
                  src="/docs/images/people/profile-picture-3.jpg"
                  alt="Bonnie image"
                />
              </div>
              <div class="flex-1 min-w-0">
                <p class="text-sm font-medium text-gray-900 truncate dark:text-white">
                  Bonnie Green
                </p>
                <p class="text-sm text-gray-500 truncate dark:text-gray-400">email@windster.com</p>
              </div>
              <div
                class="inline-flex items-center text-base font-semibold text-gray-900 dark:text-white"
              >
                $3467
              </div>
            </div>
          </li>
          <li class="py-3 sm:py-4">
            <div class="flex items-center space-x-4">
              <div class="flex-shrink-0">
                <img
                  class="w-8 h-8 rounded-full"
                  src="/docs/images/people/profile-picture-2.jpg"
                  alt="Michael image"
                />
              </div>
              <div class="flex-1 min-w-0">
                <p class="text-sm font-medium text-gray-900 truncate dark:text-white">
                  Michael Gough
                </p>
                <p class="text-sm text-gray-500 truncate dark:text-gray-400">email@windster.com</p>
              </div>
              <div
                class="inline-flex items-center text-base font-semibold text-gray-900 dark:text-white"
              >
                $67
              </div>
            </div>
          </li>
          <li class="py-3 sm:py-4">
            <div class="flex items-center space-x-4">
              <div class="flex-shrink-0">
                <img
                  class="w-8 h-8 rounded-full"
                  src="/docs/images/people/profile-picture-4.jpg"
                  alt="Lana image"
                />
              </div>
              <div class="flex-1 min-w-0">
                <p class="text-sm font-medium text-gray-900 truncate dark:text-white">Lana Byrd</p>
                <p class="text-sm text-gray-500 truncate dark:text-gray-400">email@windster.com</p>
              </div>
              <div
                class="inline-flex items-center text-base font-semibold text-gray-900 dark:text-white"
              >
                $367
              </div>
            </div>
          </li>
          <li class="pt-3 pb-0 sm:pt-4">
            <div class="flex items-center space-x-4">
              <div class="flex-shrink-0">
                <img
                  class="w-8 h-8 rounded-full"
                  src="/docs/images/people/profile-picture-5.jpg"
                  alt="Thomas image"
                />
              </div>
              <div class="flex-1 min-w-0">
                <p class="text-sm font-medium text-gray-900 truncate dark:text-white">
                  Thomes Lean
                </p>
                <p class="text-sm text-gray-500 truncate dark:text-gray-400">email@windster.com</p>
              </div>
              <div
                class="inline-flex items-center text-base font-semibold text-gray-900 dark:text-white"
              >
                $2367
              </div>
            </div>
          </li> -->
        </ul>
      </div>
    </div>
    <HFooter></HFooter>
  </div>
</template>

<script>
import BookingList from "../components/BookingList.vue";
import HFooter from "vue-hacktiv8-footer";
export default {
  name: "PaymentPage",
  components: {
    BookingList,
    HFooter,
  },
  async created() {
    await this.$store.dispatch("getBookedBallroom");
  },
  computed: {
    bookedBallroom() {
      return this.$store.state.bookedBallroom;
    },
    invoiceUrl() {
      return this.$store.state.invoiceUrl;
    },
  },
};
</script>

<style></style>
