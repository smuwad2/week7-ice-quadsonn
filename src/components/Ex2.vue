<script>
    export default { 
        // Add code in appropriate places
        data() {
            return {
                items: ['keyboard', 'mouse', 'iPhone', 'macbook', 'adapter']
                
            }
            
        },
        methods: {
            addItem(){
                // add new item into items arr
                this.items.push(this.newItem)
            }
        }
    }
</script>

<template>

    <h2>Shopping Cart</h2>
    <!-- TODO: Add Code Here -->
   <ul>
    <li v-for="(item,idx) in items">
        {{ item }}
        <button @click="items.splice(idx,1)">Delete!</button>
    </li>
   </ul>
   <input type="text" v-model="newItem"></input>
   <button @click="addItem">Add!</button>
</template>
