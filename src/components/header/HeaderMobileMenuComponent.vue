<template>
  <div
    v-if="isMenu"
    class="absolute top-0 inset-x-0 p-2 transition transform origin-top-right md:hidden"
  >
    <div
      class="rounded-lg shadow-lg ring-1 ring-black ring-opacity-5 bg-white divide-y-2 divide-gray-50"
    >
      <div class="pt-5 pb-6 px-5">
        <div class="flex items-center justify-between">
          <div>
            <UILogoComponent />
          </div>
          <UICrossIconComponent @setIsMenu="$emit('setIsMenu')" />
        </div>
        <div class="mt-6">
          <nav class="grid gap-y-8">
            <router-link
              class="-m-3 p-3 flex items-center rounded-md hover:bg-gray-50"
              to="/"
            >
              <svg
                class="flex-shrink-0 h-6 w-6 text-indigo-600"
                xmlns="http://www.w3.org/2000/svg"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
                aria-hidden="true"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M9 19v-6a2 2 0 00-2-2H5a2 2 0 00-2 2v6a2 2 0 002 2h2a2 2 0 002-2zm0 0V9a2 2 0 012-2h2a2 2 0 012 2v10m-6 0a2 2 0 002 2h2a2 2 0 002-2m0 0V5a2 2 0 012-2h2a2 2 0 012 2v14a2 2 0 01-2 2h-2a2 2 0 01-2-2z"
                />
              </svg>
              <span class="ml-3 text-base font-medium text-gray-900">
                Home
              </span>
            </router-link>

            <router-link
              class="-m-3 p-3 flex items-center rounded-md hover:bg-gray-50"
              to="/about"
            >
              <svg
                class="flex-shrink-0 h-6 w-6 text-indigo-600"
                xmlns="http://www.w3.org/2000/svg"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
                aria-hidden="true"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M15 15l-2 5L9 9l11 4-5 2zm0 0l5 5M7.188 2.239l.777 2.897M5.136 7.965l-2.898-.777M13.95 4.05l-2.122 2.122m-5.657 5.656l-2.12 2.122"
                />
              </svg>
              <span class="ml-3 text-base font-medium text-gray-900">
                About
              </span>
            </router-link>

            <router-link
              to="/delivery"
              class="-m-3 p-3 flex items-center rounded-md hover:bg-gray-50"
            >
              <svg
                class="flex-shrink-0 h-6 w-6 text-indigo-600"
                xmlns="http://www.w3.org/2000/svg"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
                aria-hidden="true"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z"
                />
              </svg>
              <span class="ml-3 text-base font-medium text-gray-900">
                Delivery
              </span>
            </router-link>

            <a
              href="#"
              class="-m-3 p-3 flex items-center rounded-md hover:bg-gray-50"
            >
              <svg
                class="flex-shrink-0 h-6 w-6 text-indigo-600"
                xmlns="http://www.w3.org/2000/svg"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
                aria-hidden="true"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M4 6a2 2 0 012-2h2a2 2 0 012 2v2a2 2 0 01-2 2H6a2 2 0 01-2-2V6zM14 6a2 2 0 012-2h2a2 2 0 012 2v2a2 2 0 01-2 2h-2a2 2 0 01-2-2V6zM4 16a2 2 0 012-2h2a2 2 0 012 2v2a2 2 0 01-2 2H6a2 2 0 01-2-2v-2zM14 16a2 2 0 012-2h2a2 2 0 012 2v2a2 2 0 01-2 2h-2a2 2 0 01-2-2v-2z"
                />
              </svg>
              <span class="ml-3 text-base font-medium text-gray-900">
                Integrations
              </span>
            </a>

            <a
              href="#"
              class="-m-3 p-3 flex items-center rounded-md hover:bg-gray-50"
            >
              <svg
                class="flex-shrink-0 h-6 w-6 text-indigo-600"
                xmlns="http://www.w3.org/2000/svg"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
                aria-hidden="true"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M4 4v5h.582m15.356 2A8.001 8.001 0 004.582 9m0 0H9m11 11v-5h-.581m0 0a8.003 8.003 0 01-15.357-2m15.357 2H15"
                />
              </svg>
              <span class="ml-3 text-base font-medium text-gray-900">
                Automations
              </span>
            </a>
          </nav>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import UILogoComponent from "@/components/ui/UILogoComponent";
import UICrossIconComponent from "@/components/ui/UICrossIconComponent";

export default {
  name: "HeaderMobileMenuComponent",
  components: {
    UILogoComponent,
    UICrossIconComponent,
  },
  props: {
    isMenu: {
      type: Boolean,
      default: () => false,
    },
  },
};
</script>
