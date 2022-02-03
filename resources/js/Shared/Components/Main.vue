<template>
    <div class="relative overflow-hidden flex-1 flex flex-row">
        <Sidebar />

        <Content>
            <slot />
        </Content>
    </div>
</template>

<script>
import Sidebar from "@/Shared/Components/Sidebar";
import Content from "@/Shared/Components/Content";

export default {
    components: {
        Sidebar,
        Content,
    },
};
</script>
