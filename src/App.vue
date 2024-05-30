<script setup>
import { RouterLink, RouterView } from 'vue-router'
import Todos from './components/Todos.vue';
import moment from 'moment';

</script>
<script>
    export default {
      data: () => ({
        todo:'',
        items: []
      }),
      methods:{
        handleclick(){
          if(this.todo){
          this.items.push({
            title:this.todo,
            value: this.items.length!=0 ? this.items[this.items.length-1].value + 1 : 1,
            createdAt:Date.now(),
            status: 'pending'
            
          })
          this.todo=''}
          console.log(this.items);
        }
      }
    }
  </script>
<template>
  <div class="">
    <div class="w-full" >
      <v-sheet class="mx-auto" width="300">
        <v-form @submit.prevent>
          <v-text-field
          v-model="todo"
          :rules="rules"
          label="Tasks"
          ></v-text-field>
          <v-btn class="mt-2" type="submit" @click="handleclick" block>Submit</v-btn>
        </v-form>
      </v-sheet>
    </div>
    <div>
      <Todos :items="items"/>
    </div>
<div>

</div>
  </div>
 
 
</template>


<style scoped>

</style>
