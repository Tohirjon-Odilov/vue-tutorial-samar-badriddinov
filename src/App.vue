<template>
<div>
    <!-- <p>Count : <strong>{{ count }}</strong></p> -->
    <!-- <button class="btn btn-info" @click="increment">Increment</button> -->
    <!-- <button class="btn btn-success" @click="decrement">Decrement</button> -->
    <div class="container">
        <div class="row">
            <h3 class="mt-3">Add Comment</h3>
            <form action="none">
                <input @input="inputName" :value="name" type="text" placeholder="Enter your name ..." class="form-control">
                <input :value="email" type="email" placeholder="Enter your email ..." class="form-control my-3">
                <input :value="content" type="text" placeholder="Enter your content ..." class="form-control">
                <div class="d-flex flex-row-reverse">
                    <button class="btn btn-success mt-4"> Add Comment </button>
                </div>
            </form>
        </div>
        <div class="row">
            <div class=" col-sm-12 col-lg-4 mt-3 g-start-3" v-for="cards in card" :key="cards.id">
                <div class="card bg-success text-white p-3">
                    <div class="name"><b>Name: </b>{{ cards.name }} </div>
                    <div class="email"><b>Email: </b>{{ cards.email }}</div>
                    <div class="content"><b>Content: </b> {{ cards.content }}</div>
                </div>
            </div>
        </div>
    </div>

    <!-- <div class="w-25 mx-auto comment bg-info">

        <div class="name"><b>Name: </b>John</div>
        <div class="email"><b>Email: </b>john@gmail.com</div>
        <div class="content"><b>Content: </b>Lorem ipsum dolor sit.</div>

    </div> -->
</div>
</template>

<script>
export default {
    data() {
        return {
            // message: 'Hello Vue!',
            // count: 0,

            card: [{
                    id: 0,
                    name: 'John',
                    email: "john@gmail.com",
                    content: "Lorem John dolor sit."
                },
                {
                    id: 1,
                    name: 'Martin',
                    email: "martin@gmail.com",
                    content: "Lorem Martin dolor sit."
                },
                {
                    id: 2,
                    name: 'Jordan',
                    email: "jordan@gmail.com",
                    content: "Lorem Jordan dolor sit."
                },
            ],

            name: '',
            email: '',
            content:'',

        }
    },
    methods: {
        // increment() {
        //     this.count += 1
        // },
        // decrement() {
        //     this.count -= 1
        // }

        inputName(event){
            this.name = event.target.value;
        }
        
    },

}
</script>

// SCOPED => css kodlarimiz  faqatgina ushbu faylga amal qilishini xohlasak shundagina ushbu argumentdan foydalanamiz. Agar ushbu alomat ta'sir qilinmasa css kodlarimiz global tarzida ishlaydi.
// style scoped

<style>
/* .comment{
        border: 1px solid #ccc;
        margin: 10px;
        padding: 10px;
    } */
</style>
