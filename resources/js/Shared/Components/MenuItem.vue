<template>
    <button
        v-if="subItems.length > 0"
        type="button"
        class="w-full px-6 py-3 rounded hover:bg-gray-900 transition duration-300 ease-in-out"
        :class="{ 'bg-gray-900': $page.url.startsWith(link) }"
        @click="handleShowSubItems"
    >
        <div
            class="w-full flex justify-between items-center text-md font-medium text-gray-300"
        >
            <div class="flex items-center">
                <slot />
            </div>

            <IconPlus
                v-if="subItems.length > 0 && !showSubItems"
                class="w-4 h-4"
            />

            <IconMinus
                v-if="subItems.length > 0 && showSubItems"
                class="w-4 h-4"
            />
        </div>

        <div
            class="w-full mt-3"
            :class="showSubItems ? 'flex flex-col' : 'hidden'"
        >
            <Link
                v-for="subItem in subItems"
                :key="subItem.title"
                :href="subItem.link"
                class="w-full px-1 py-3 text-left text-sm text-gray-300 hover:text-white transition duration-300 ease-in-out"
            >
                {{ subItem.title }}
            </Link>
        </div>
    </button>

    <Link
        v-else
        :href="link"
        class="w-full px-6 py-3 flex items-center rounded text-md font-medium text-gray-300 hover:bg-gray-900 transition duration-300 ease-in-out"
        :class="{ 'bg-gray-900': $page.url.startsWith(link) }"
    >
        <slot />
    </Link>
</template>

<script>
import { Link } from "@inertiajs/inertia-vue3";

import IconPlus from "@/Shared/Icons/Plus";
import IconMinus from "@/Shared/Icons/Minus";

export default {
    components: {
        Link,
        IconPlus,
        IconMinus,
    },

    props: {
        link: {
            type: String,
            default: "/",
        },
        subItems: {
            type: Array,
            default: [],
        },
    },

    data() {
        return {
            showSubItems: false,
        };
    },

    methods: {
        handleShowSubItems() {
            this.showSubItems = !this.showSubItems;
        },
    },
};
</script>
