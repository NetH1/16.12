<template>
  <div class="container">
    <div class="flex-content">
      <div class="bg-border-content flex-1">
        <img src="../assets/imgblur.png" alt="imgblur" />
        <div>content</div>
      </div>
      <div class="bg-border-content flex-2">
        <div class="w-full" v-for="item in items" :key="item.id">
          <div class="bg-border-content flex-3">
            <img src="../assets/green.png" alt="" />
            <span class="span-absolute">{{ item.amount }}</span>
          </div>
          <div v-if="isShow == true">
            <img src="../assets/green.png" alt="">
            <p>{{item.desctiption}}</p>
            <button>Удалить</button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { ref } from '@vue/reactivity';
export default {
    setup() {
        
        const isShow = ref(false)
        return{
            isShow
        }
    },
  props: {
    items: {
      type: Array,
    },
  },
  methods: {
     fuyt(id) {
        this.items.map(x => {
          if(x.id == id) {
            this.isShow = true
          } else{
            this.isShow = false
          }
          return x
        })
    }
  }
};
</script>

