<script setup>
import {useForm} from '@inertiajs/vue3';
const testfunction = ()=> {
    my_modal_1.showModal()
}
const form = useForm({
    title : ''
})

const savePost = ()=> {
    my_modal_1.close()
    console.log('form::',form);

    form.post('/posts')
}

</script>

<template>
    <button class="btn" @click="testfunction" >New Post</button>
    <dialog id="my_modal_1" class="modal">
        <div class="modal-box">
            <h3 class="font-bold text-lg">Hola crea un nuevo post 😁!</h3>
            <!-- <form action=""> -->
                <textarea v-model="form.title" class="textarea textarea-primary mt-12 w-full h-40" placeholder="Bio"></textarea>
                <div class="modal-action">
                    <button @click="savePost" class="btn  btn-primary">Save</button>
                </div>
            <!-- </form> -->
        </div>
    </dialog>
</template>