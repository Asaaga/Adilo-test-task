<template>
    <button @click="handleClick()" :style="{ background: color, color: textColor }" class="btn">{{ text }}</button>
</template>

<script>

export default {
    name: 'Button',
    props: {
        text: String,
        color: String,
        textColor: String,
    },
    methods: {
        async handleClick() {
            const stream = await navigator.mediaDevices.getDisplayMedia({
                video: {
                    mediaSource: "screen"
                }
            })
            const data = [];
            const mediaRecorder = new MediaRecorder(stream);

            mediaRecorder.ondataavailable = (e) => {
                data.push(e.data)
            }
            mediaRecorder.start();
            mediaRecorder.onstop = (e) => {
                document.querySelector("video").src = URL.createObjectURL(
                    new Blob(data, {
                        type: data[0].type
                    })
                )
            }
        }
    }
}

</script>
<style>
    .btn {
        padding: 5px !important;
        height: 90%;
        border: none;
    }
</style>