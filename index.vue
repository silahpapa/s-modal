<script setup lang="ts">

import {onBeforeMount,ref} from 'vue';

interface Props {

  id: string
  title: string
  static: string
  position: string
  size: string
}
const props = defineProps<Props>()
const title = props.title
const static_ = props.static
const position = props.position
let modalClass = ref([])
const updateSizeClasses = onBeforeMount(()=>{
  const size = props.size
  let posClass: string = size === 'xl' ? 'modal-xl' : (size === 'lg'? 'modal-lg': size === 'sm' ? 'modal-xl' : 'modal-md')
    modalClass.value.push(posClass)
})

</script>
<template>
  <div class="modal fade" :id="id" :data-bs-backdrop="static_" tabindex="-1" aria-labelledby="exampleModalLabel" aria-hidden="true">
    <div class="modal-dialog" :class="modalClass">
      <div class="modal-content">
        <div class="modal-header">
          <h5 class="modal-title" id="exampleModalLabel">{{ title }}</h5>
          <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
        </div>
        <div class="modal-body">
          <slot />
        </div>
        <div class="modal-footer">
        </div>
      </div>
    </div>
  </div>
</template>
<style scoped>
</style>
