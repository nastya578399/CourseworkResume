<template>
    <form class="card card-w30" @submit.prevent="submitHandler">
        <div class="form-control">
            <label for="type" >Тип блока</label>
            <select id="type" v-model="type">
                <option value="title">Заголовок</option>
                <option value="subtitle">Подзаголовок</option>
                <option value="avatar">Аватар</option>
                <option value="text">Текст</option>
            </select>
        </div>

        <div class="form-control">
            <label for="value">Значение</label>
            <textarea 
            id="value" 
            rows="3"
            v-model.trim="textItem"
            ></textarea>
        </div>

        <button type="submit" class="btn primary" :disabled="textItem.length === 0" >Добавить</button>
    </form>
</template>

<script>
export default {
    props: {
        title: String,
        subtitle: String,
        avatar: Image,
        text: String
    },
    data() {
        return {
            type: 'title',
            type: 'subtitle',
            type: 'avatar',
            type: 'text',
            textItem: '',
        }
    },

    methods: {
        submitHandler(event) {
            console.group('Text for summary')
            console.log('Text:', this.type);
            console.groupEnd()
        },
        newItem() {

        }
    }

}
</script>

<style>

</style>