<script setup>
import { defineEmits } from 'vue';

const emits = defineEmits(['selectOption'])

const selectOption= (isColor)=>{
    emits("selectOption",isColor)
}
</script>
<template>
    <VNavigationDrawer
        expand-on-hover
        rail>
        <v-list>
            <v-list-item
              prepend-avatar="https://kpopping.com/documents/4e/5/1536/220816-NewJeans-Minji-documents-1.jpeg?v=95233"
              title="Kim Minji"
              subtitle="minji_newjeans@kr.com"
            ></v-list-item>
          </v-list>

          <v-divider></v-divider>
          <v-list density="compact" nav>
            <v-list-item prepend-icon="mdi-image" title="Color Gallery" value="color" @click="selectOption(true)"></v-list-item>
            <v-list-item prepend-icon="mdi-dialpad" title="Grayspace Gallery" value="color" @click="selectOption(false)"></v-list-item>

          </v-list>
    </VNavigationDrawer>
</template>