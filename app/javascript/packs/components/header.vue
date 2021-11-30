<template>
    <div class="min-w-full bg-black">
        <p>{{ message }}</p>
    </div>
</template>

<script>
function getMorning() {
    if (new Date().getUTCHours() > 7 && new Date().getUTCHours() < 16) {
        return true;
    }
    return false;
}

function getMorningMessage(morning) {
    if (morning) return "Have a nice day!";
    return "Time for relax.";
}

export default {
    data: function () {
        return {
            message: `Hi, you are in ${new Date().getFullYear()}`,
            morning: getMorningMessage(getMorning()),
        };
    },
};
</script>

<style scoped></style>
