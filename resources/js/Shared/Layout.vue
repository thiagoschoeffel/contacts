<template>
    <Wrapper>
        <slot />
    </Wrapper>
</template>

<script>
import Wrapper from "../Shared/Wrapper";

export default {
    components: {
        Wrapper,
    },
};
</script>
