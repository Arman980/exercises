        <template>
        <v-container>
        <v-btn v-bind:color="color"><slot></slot>Counter: {{ count }}</v-btn>
        <v-btn v-on:click="add" v-bind:color="color">Counter: {{ count }} <slot></slot></v-btn>
        </v-container>
        </template>


        <script>
        export default {        
        name: 'Counter',
        data: () => ({
            count: 0
        }),
        props: {
            color: String
        },
        methods: {
            add: function () {
                this.count++
            }
        }
        }
        </script>
