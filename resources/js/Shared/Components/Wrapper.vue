<template>
    <div
        class="relative z-0 w-screen h-screen overflow-hidden flex flex-col bg-gray-300"
    >
        <Header />

        <Main>
            <slot />
        </Main>
    </div>
</template>

<script>
import Header from "@/Shared/Components/Header";
import Main from "@/Shared/Components/Main";

export default {
    components: {
        Header,
        Main,
    },
};
</script>
