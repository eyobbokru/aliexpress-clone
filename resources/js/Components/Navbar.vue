<template>
  <header class="bg-gray-100">
    <nav class="container mx-auto px-8">
      <ul class="flex justify-end space-x-8 py-3 text-sm">
        <li>
          <a href="">Sell on aliexpress</a>
        </li>
        <li>
          <a href="">Help</a>
        </li>
        <li>
          <a href="" class="flex items-center">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 24 24"
              stroke-width="1.5"
              stroke="currentColor"
              class="w-5 h-5 mr-1"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                d="M21 8.25c0-2.485-2.099-4.5-4.688-4.5-1.935 0-3.597 1.126-4.312 2.733-.715-1.607-2.377-2.733-4.313-2.733C5.1 3.75 3 5.765 3 8.25c0 7.22 9 12 9 12s9-4.78 9-12z"
              />
            </svg>

            Wishlist
          </a>
        </li>
        <li class="relative">
          <a
            @mouseover="isAccountLinkHovered = true"
            href=""
            class="relative cursor-pointer"
          >
            <span
              :class="isAccountLinkHovered ? 'text-red-500' : ''"
              class="flex items-center"
            >
              <svg
                xmlns="http://www.w3.org/2000/svg"
                fill="none"
                viewBox="0 0 24 24"
                stroke-width="1.5"
                stroke="currentColor"
                class="w-5 h-5 mr-1"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  d="M15.75 6a3.75 3.75 0 11-7.5 0 3.75 3.75 0 017.5 0zM4.501 20.118a7.5 7.5 0 0114.998 0A17.933 17.933 0 0112 21.75c-2.676 0-5.216-.584-7.499-1.632z"
                />
              </svg>

              Account</span
            >
          </a>
          <div
            v-if="isAccountLinkHovered"
            @mouseleave="isAccountLinkHovered = false"
            class="absolute right-0 p-4 w-max h-max bg-gray-100"
          >
            <div class="flex space-x-2 py-2 border-b-2 border-gray-200">
              <button
                class="bg-red-500 text-white py-2 px-8 text-center font-bold rounded-sm"
              >
                Join
              </button>
              <button
                class="bg-red-100 text-red-500 py-2 px-8 text-center font-bold rounded-sm"
              >
                Sign in
              </button>
            </div>
            <ul class="my-3 text-sm">
              <li>
                <a href="/">My Orders</a>
              </li>
              <li>
                <a href="/">My Wishlist</a>
              </li>
              <li>
                <a href="/">My Coupons</a>
              </li>
              <li>
                <a href="/">Message center</a>
              </li>
            </ul>
          </div>
        </li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {
  components: {},
  props: {},

  data() {
    return {
      isAccountLinkHovered: false,
    };
  },
};
</script>