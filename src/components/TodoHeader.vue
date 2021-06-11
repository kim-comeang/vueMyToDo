<template>
    <div class="header">
        <h1 class="logo">My Todo</h1>
        <p class="date">{{ timestamp }}</p>
    </div>
</template>

<script>
export default {
    data() {
        return {
            timestamp: ""
        };
    },
    created() {
        const now = new Date();
        const month = now.getMonth() + 1;
        const date = now.getDate();
        const weekList = new Array("Sun.","Mon.","Tue.","Wed,","Thu.","Fri.","Sat.");
        const week = weekList[now.getDay()];
        this.timestamp = `${month}/${date} ${week}`;
    }
};
</script>

<style lang="scss" scoped>

* {
    margin: 0;
    padding: 0;
}
.header {
    display: flex;
    .logo {
        font-size: 20px;
        line-height: 20px;
    }
    .date {
        font-size: 20px;
        line-height: 20px;
    }
}

</style>