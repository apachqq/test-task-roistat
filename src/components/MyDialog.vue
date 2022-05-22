<template>
    <div class="form" v-if="isOpen">
        <form>
            <p>Добавление пользователя</p>
            <div class="form-control">
                <label for="name">Имя</label>
                <input type="text" id="name" v-model="people.name">
            </div>
            <div class="form-control">
                <label for="number">Телефон</label>
                <input type="number" id="number" v-model="people.number">
            </div>

            <my-select
                    :persons="persons"
            ></my-select>

            <my-button @click.prevent="createPeople">Сохранить</my-button>
        </form>
    </div>
</template>

<script>
    import MySelect from '@/components/MySelect'

    export default {
        data() {
            return {
                people: {
                    name: '',
                    number: ''
                }
            }
        },
        methods: {
            createPeople() {
                if (this.people.name !== '' && this.people.number !== '') {
                    this.people.id = Date.now()
                    this.$emit('create', this.people)
                    this.people = {
                        name: '',
                        number: ''
                    }
                }
            }
        },
        props: {
            isOpen: {
                type: Boolean
            },
            persons: {
                type: Array
            }
        },
        components: {MySelect}
    }
</script>

<style scoped>

</style>
