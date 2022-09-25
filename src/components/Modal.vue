<template>
   <transition name="modal-animation">
    <div v-show="modalActive" class="modal">
        <transition name="modal-animation-inner">
            <div v-show="modalActive" class="modal-inner">

            </div>
        </transition>
    </div>
   </transition>
</template>

<script>
    export default {
        name: 'Modal',
        props: ["modalActive"],
    }
</script>
