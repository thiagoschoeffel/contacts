<template>
    <div class="relative z-0 w-screen h-screen overflow-hidden flex flex-col">
        <Header />

        <Main>
            <slot />
        </Main>
    </div>
</template>

<script>
import Header from "../Shared/Header";
import Main from "../Shared/Main";

export default {
    components: {
        Header,
        Main,
    },
};
</script>
