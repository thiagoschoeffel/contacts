<template>
    <Wrapper>
        <slot />
    </Wrapper>
</template>

<script>
import Wrapper from "@/Shared/Components/Wrapper";

export default {
    components: {
        Wrapper,
    },
};
</script>
