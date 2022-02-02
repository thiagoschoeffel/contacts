<template>
    <div class="relative overflow-hidden flex-1 flex flex-row">
        <Sidebar />

        <Content>
            <slot />
        </Content>
    </div>
</template>

<script>
import Sidebar from "../Shared/Sidebar";
import Content from "../Shared/Content";

export default {
    components: {
        Sidebar,
        Content,
    },
};
</script>
