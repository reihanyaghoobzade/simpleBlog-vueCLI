<template>
    <div class="col-span-1">
        <h2 class="font-bold text-2xl mb-8">Edit Post</h2>
        <form @submit.prevent="validate">
            <div class="mb-6">
                <label for="title" class="block mb-2 font-medium text-gray-900">Title</label>
                <input v-model.lazy.trim="form.title" type="text" id="title" class="shadow-sm bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-4">
                <p class="mt-2 text-sm text-red-600">{{ form.titleError }}</p>
            </div>
            <label for="message" class="block mb-2 font-medium text-gray-900">Body</label>
            <textarea v-model.lazy.trim="form.body" id="message" rows="8" class="block p-4 w-full text-sm text-gray-900 bg-gray-50 rounded-lg border border-gray-300 focus:ring-blue-500 focus:border-blue-500"></textarea>
            <p class="mt-2 text-sm text-red-600">{{ form.bodyError }}</p>
            <button class="py-2 px-4 mt-8 bg-black rounded-md text-white font-medium" type="submit">Submit</button>
        </form>
    </div>
</template>

<script>
import { reactive } from "vue";
import { useRoute } from "vue-router";
import axios from "axios";
import swal from "sweetalert";

export default {
    setup() {
        const router = useRoute();
        const form = reactive({
            title : '',
            titleError : '',
            body : '',
            bodyError : ''
        });

        function validate(){
            if(form.title == ""){
                form.titleError = "Title is required!";
            }else {
                form.titleError = "";
            }

            if(form.body == ""){
                form.bodyError = "Title is required!";
            }else {
                form.bodyError = "";
            }

            if(form.title !== "" && form.body !== ""){
                editPost();
            }
        }

        function getPosts() {
            axios.get(`https://jsonplaceholder.typicode.com/posts/${router.params.id}`)
            .then((response) => {
            form.title = response.data.title;
            form.body = response.data.body;
            })
            .catch((error) => console.log(error));
        }

    getPosts();

        function editPost(){
            axios.patch(`https://jsonplaceholder.typicode.com/posts/${router.params.id}`, {
                    body: JSON.stringify({
                    title: form.title,
                    body: form.body,
                    userId: 1,
                }),
                    headers: {
                    'Content-type': 'application/json; charset=UTF-8',
                },
            })
            .then((response) => {
                console.log(response);
                swal("Thanks!", "Post edited succesfully!", "success");
                })
            .catche(error => console.log(error));
        }

        return { form, validate };
    },
};
</script>

<style>
</style>