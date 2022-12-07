<template>
    <span class="user">
        <!--<span class="name">Ironhack</span>-->
        <span class="name">{{ tweet.name}}</span>
        <span class="handle">@{{ tweet.handle}}</span>
    </span>
</template>

<script>
    export default {
    props: ["tweet"],
    };
</script>