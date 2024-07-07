<template>
  <div class="flex">
    <!-- Sidebar -->
    <div class="w-1/4 bg-[#101010] text-white p-4">
      <div class="items-center mb-6">
        <div class="w-[70px] h-[70px] rounded-2xl">
          <img
            :src="profileImage"
            alt="Profile"
            class="w-full h-[70px] object-center rounded-2xl mr-3"
          />
        </div>
        <div class="mt-3">
          <div class="font-bold">Samantha</div>
          <div class="text-sm">samantha@email.com</div>
        </div>
      </div>
      <nav class="mt-16">
        <ul>
          <li class="mb-2">
            <a
              href="#"
              class="flex items-center p-2 text-gray-400 hover:text-white"
              >Dashboard</a
            >
          </li>
          <li class="mb-2">
            <a
              href="#"
              class="flex items-center p-2 text-gray-400 hover:text-white"
            >
              Expenses</a
            >
          </li>
          <li class="mb-2">
            <a
              href="#"
              class="flex items-center p-2 text-gray-400 hover:text-white"
            >
              Wallets</a
            >
          </li>
          <li class="mb-2">
            <a
              href="#"
              class="flex items-center p-2 text-gray-400 hover:text-white"
              >Summary</a
            >
          </li>
          <li class="mb-2">
            <a
              href="#"
              class="flex items-center p-2 text-gray-400 hover:text-white"
            >
              Accounts</a
            >
          </li>
          <li>
            <a
              href="#"
              class="flex items-center p-2 text-gray-400 hover:text-white"
            >
              Settings</a
            >
          </li>
        </ul>
      </nav>
    </div>

    <!-- Main Content -->
    <div class="flex-1 p-6">
      <div class="bg-white rounded-lg p-4 shadow-md">
        <h2 class="text-xl font-bold mb-4">Expenses</h2>
        <div class="flex justify-between mb-6">
          <div>
            <div class="text-gray-600">01 - 25 March, 2020</div>
            <div class="text-sm text-gray-400">Where your money goes?</div>
          </div>
          <div class="flex items-center">
            <span class="material-icons text-gray-400 mr-2">group</span>
            <span class="text-gray-600">Share</span>
          </div>
        </div>

        <!-- Expenses List -->
        <div class="mb-4">
          <div class="flex items-center justify-between mb-2">
            <div class="flex items-center">
              <span class="material-icons text-green-500 mr-2"
                >local_grocery_store</span
              >
              <div>
                <div class="text-gray-700">Grocery</div>
                <div class="text-sm text-gray-400">
                  5:12 pm - Belanja di pasar
                </div>
              </div>
            </div>
            <div class="text-red-500">-326,800</div>
          </div>
          <div class="flex items-center justify-between mb-2">
            <div class="flex items-center">
              <span class="material-icons text-blue-500 mr-2"
                >directions_bus</span
              >
              <div>
                <div class="text-gray-700">Transportation</div>
                <div class="text-sm text-gray-400">5:12 pm - Naik bus umum</div>
              </div>
            </div>
            <div class="text-red-500">-15,000</div>
          </div>
          <div class="flex items-center justify-between mb-2">
            <div class="flex items-center">
              <span class="material-icons text-orange-500 mr-2">home</span>
              <div>
                <div class="text-gray-700">Housing</div>
                <div class="text-sm text-gray-400">5:12 pm - Bayar listrik</div>
              </div>
            </div>
            <div class="text-red-500">-185,750</div>
          </div>
        </div>

        <div class="mb-4">
          <h3 class="font-semibold text-gray-700 mb-2">
            Monday, 23 March 2020
          </h3>
          <div class="flex items-center justify-between mb-2">
            <div class="flex items-center">
              <span class="material-icons text-red-500 mr-2">restaurant</span>
              <div>
                <div class="text-gray-700">Food and Drink</div>
                <div class="text-sm text-gray-400">5:12 pm - Makan Steak</div>
              </div>
            </div>
            <div class="text-red-500">-156,000</div>
          </div>
          <div class="flex items-center justify-between">
            <div class="flex items-center">
              <span class="material-icons text-green-500 mr-2">local_play</span>
              <div>
                <div class="text-gray-700">Entertainment</div>
                <div class="text-sm text-gray-400">
                  5:12 pm - Nonton Bioskop
                </div>
              </div>
            </div>
            <div class="text-red-500">-35,200</div>
          </div>
        </div>
      </div>

      <!-- Where Your Money Goes -->
      <div class="bg-white rounded-lg p-4 shadow-md mt-6">
        <h3 class="text-xl font-bold mb-4">Where your money go?</h3>
        <div>
          <div class="flex justify-between items-center mb-2">
            <div>Food and Drinks</div>
            <div>872,400</div>
          </div>
          <div class="w-full bg-gray-200 rounded-full h-2.5 mb-4">
            <div
              class="bg-green-500 h-2.5 rounded-full"
              style="width: 70%"
            ></div>
          </div>

          <div class="flex justify-between items-center mb-2">
            <div>Shopping</div>
            <div>1,378,200</div>
          </div>
          <div class="w-full bg-gray-200 rounded-full h-2.5 mb-4">
            <div
              class="bg-yellow-500 h-2.5 rounded-full"
              style="width: 80%"
            ></div>
          </div>

          <div class="flex justify-between items-center mb-2">
            <div>Housing</div>
            <div>928,500</div>
          </div>
          <div class="w-full bg-gray-200 rounded-full h-2.5 mb-4">
            <div
              class="bg-orange-500 h-2.5 rounded-full"
              style="width: 60%"
            ></div>
          </div>

          <div class="flex justify-between items-center mb-2">
            <div>Transportation</div>
            <div>420,700</div>
          </div>
          <div class="w-full bg-gray-200 rounded-full h-2.5 mb-4">
            <div
              class="bg-blue-500 h-2.5 rounded-full"
              style="width: 40%"
            ></div>
          </div>

          <div class="flex justify-between items-center mb-2">
            <div>Vehicle</div>
            <div>50,000</div>
          </div>
          <div class="w-full bg-gray-200 rounded-full h-2.5">
            <div class="bg-red-500 h-2.5 rounded-full" style="width: 10%"></div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Dashboard",
  data() {
    return {
      profileImage: "/de65de332ec15bf450eda8bbd5c75b19.png", // Path relative to the public directory
    };
  },
};
</script>

<style scoped>
.material-icons {
  font-size: 24px;
}
</style>
