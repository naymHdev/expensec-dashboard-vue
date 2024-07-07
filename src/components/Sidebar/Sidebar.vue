<template>
  <div class="flex font-poppins">
    <!-- Sidebar -->
    <div class="w-1/4 bg-[#101010] text-white p-5">
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
    <div class="flex gap-5 justify-between bg-white rounded-lg shadow-md">
      <div class="p-5 w-full">
        <div class="flex items-center justify-between">
          <div>
            <h2 class="text-4xl font-bold mb-2 text-[#262A41]">Expenses</h2>
          </div>
          <div>
            <a-avatar-group shape="square">
              <a-avatar style="background-color: #fde3cf">A</a-avatar>
              <a-avatar style="background-color: #f56a00">K</a-avatar>
              <a-tooltip title="Ant User" placement="top">
                <a-avatar style="background-color: #87d068">
                  <template #icon><UserOutlined /></template>
                </a-avatar>
              </a-tooltip>
              <a-avatar> + </a-avatar>
            </a-avatar-group>
          </div>
        </div>

        <!-- State and more content -->
        <section>
          <div class="p-6">
            <h2 class="mt-4 text-lg font-semibold text-gray-800">Today</h2>
            <div
              class="flex items-center my-4"
              v-for="item in todayExpenses"
              :key="item.id"
            >
              <div
                :class="`w-10 h-10 rounded-full flex items-center justify-center text-white mr-4 ${iconColor(
                  item.category
                )}`"
              ></div>
              <div class="flex-1">
                <div class="flex justify-between text-base text-gray-800">
                  <span>{{ item.category }}</span>
                  <span>{{ item.amount }}</span>
                </div>
                <div class="flex justify-between text-sm text-gray-500">
                  <span>{{ item.time }}</span>
                  <span>{{ item.description }}</span>
                </div>
              </div>
            </div>
            <h2 class="mt-4 text-lg font-semibold text-gray-800">
              Monday, 23 March 2020
            </h2>
            <div
              class="flex items-center my-4"
              v-for="item in previousExpenses"
              :key="item.id"
            >
              <div
                :class="`w-10 h-10 rounded-full flex items-center justify-center text-white mr-4 ${iconColor(
                  item.category
                )}`"
              ></div>
              <div class="flex-1">
                <div class="flex justify-between text-base text-gray-800">
                  <span>{{ item.category }}</span>
                  <span>{{ item.amount }}</span>
                </div>
                <div class="flex justify-between text-sm text-gray-500">
                  <span>{{ item.time }}</span>
                  <span>{{ item.description }}</span>
                </div>
              </div>
            </div>
          </div>
        </section>

        <div class="flex justify-between mb-6">
          <div>
            <div class="text-gray-600">01 - 25 March, 2020</div>
          </div>
        </div>

        <!-- Expenses List -->
      </div>

      <!-- today section -->
      <div class="bg-[#F9FAFC] p-5 rounded-r-lg w-2/4">
        <h3 class="text-xl font-bold pt-3">Where your money go?</h3>
        <div class="mt-8 space-y-12">
          <div>
            <div class="flex justify-between items-center">
              <div>Food and Drinks</div>
              <div>872,400</div>
            </div>
            <div class="w-full bg-gray-200 mt-3 rounded-full h-2.5">
              <div
                class="bg-green-500 h-2.5 rounded-full"
                style="width: 70%"
              ></div>
            </div>
          </div>

          <div>
            <div class="flex justify-between items-center">
              <div>Shopping</div>
              <div>1,378,200</div>
            </div>
            <div class="w-full bg-gray-200 mt-3 rounded-full h-2.5">
              <div
                class="bg-green-500 h-2.5 rounded-full"
                style="width: 80%"
              ></div>
            </div>
          </div>

          <div>
            <div class="flex justify-between items-center">
              <div>Housing</div>
              <div>928,500</div>
            </div>
            <div class="w-full bg-gray-200 mt-3 rounded-full h-2.5">
              <div
                class="bg-green-500 h-2.5 rounded-full"
                style="width: 60%"
              ></div>
            </div>
          </div>

          <div>
            <div class="flex justify-between items-center">
              <div>Transportation</div>
              <div>420,700</div>
            </div>
            <div class="w-full bg-gray-200 mt-3 rounded-full h-2.5">
              <div
                class="bg-green-500 h-2.5 rounded-full"
                style="width: 40%"
              ></div>
            </div>
          </div>

          <div>
            <div class="flex justify-between items-center">
              <div>Vehicle</div>
              <div>50,000</div>
            </div>
            <div class="w-full bg-gray-200 mt-3 rounded-full h-2.5">
              <div
                class="bg-green-500 h-2.5 rounded-full"
                style="width: 10%"
              ></div>
            </div>
          </div>
        </div>

        <!-- User Saves Section -->
        <section class="bg-[#EDF0F5] rounded-2xl p-5 mt-28 relative">
          <div class="absolute -top-11">
            <div class="flex items-center justify-between">
              <div>
                <img :src="icon2" alt="Profile" />
              </div>
              <div>
                <img :src="icon1" alt="Profile" />
              </div>
            </div>
          </div>
          <h2 class="text-xl font-semibold py-2 mt-[40px]">Save more money</h2>
          <p class="text-sm font-medium text-[#404852]">
            eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim
            ad minim.
          </p>
          <button
            class="w-full py-3 bg-black rounded-2xl text-white font-medium mt-5"
          >
            VIEW TIPS
          </button>
        </section>
      </div>
    </div>
  </div>
</template>

<script>
import { Avatar, Tooltip } from "ant-design-vue";
import { UserOutlined, AntDesignOutlined } from "@ant-design/icons-vue";

export default {
  name: "Dashboard",
  components: {
    "a-avatar": Avatar,
    "a-tooltip": Tooltip,
    UserOutlined,
    AntDesignOutlined,
  },
  data() {
    return {
      profileImage: "/de65de332ec15bf450eda8bbd5c75b19.png",
      icon1: "/serv.png",
      icon2: "/shorteg-box.png",
      todayExpenses: [
        {
          id: 1,
          category: "Grocery",
          time: "5:12 pm",
          description: "Belanja di pasar",
          amount: "-326.800",
        },
        {
          id: 2,
          category: "Transportation",
          time: "5:12 pm",
          description: "Naik bus umum",
          amount: "-15.000",
        },
        {
          id: 3,
          category: "Housing",
          time: "5:12 pm",
          description: "Bayar Listrik",
          amount: "-185.750",
        },
      ],
      previousExpenses: [
        {
          id: 4,
          category: "Food and Drink",
          time: "5:12 pm",
          description: "Makan Steak",
          amount: "-156.000",
        },
        {
          id: 5,
          category: "Entertainment",
          time: "5:12 pm",
          description: "Nonton Bioskop",
          amount: "-35.200",
        },
      ],
    };
  },
  methods: {
    iconColor(category) {
      switch (category) {
        case "Grocery":
          return "bg-blue-500";
        case "Transportation":
          return "bg-purple-500";
        case "Housing":
          return "bg-red-500";
        case "Food and Drink":
          return "bg-orange-500";
        case "Entertainment":
          return "bg-green-500";
        default:
          return "bg-gray-500";
      }
    },
  },
};
</script>

<style scoped>
.material-icons {
  font-size: 24px;
}
</style>
