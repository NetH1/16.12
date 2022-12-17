<template>
  <div class="container">
    <div class="flex-content">
      <div class="bg-border-content flex-1">
        <img src="../assets/imgblur.png" alt="imgblur" />
        <div>content</div>
      </div>
      <div class="bg-border-content flex-2">
        <div class="w-full" v-for="(item,index) in items" :key="item.id">
          <div @click="openMenu(item.id)" class="bg-border-content flex-3">
            <img src="../assets/green.png" alt="" />
            <span class="span-absolute">{{ item.amount }}</span>
          </div>
          <div class="menu" v-if="item.isShow == true">
            <div class="content">
              <img class="menu-img" src="../assets/biggreen.png" alt="">
            <p>{{item.desctiption}}</p>
            <button @click="deleteItem(index)">Удалить</button>
            </div>
            <span @click="item.isShow = false" class="close"></span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    items: {
      type: Array,
      required: true
    },
  },
  methods: {
     openMenu(id) {
        this.items.map(x => {
          if(x.id == id) {
            x.isShow = !x.isShow
          } else{x.isShow =false}
          return x
        })
    },
    deleteItem(index) {
      localStorage.setItem('items',JSON.stringify(this.items));
      this.items.splice(index, 1)
      this.items = JSON.parse(localStorage.getItem(this.items))
      
    }
  },
  mounted(){
      localStorage.setItem('items', JSON.stringify(this.items));
      this.items = JSON.parse(localStorage.getItem("items")); 
  }
};
</script>

