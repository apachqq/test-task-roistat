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
                <input type="text" id="number" v-model="people.number">
            </div>
            <div class="form-control">
                <label for="select">Начальник</label>
                <select id="select">
                    <option disabled>Начальник</option>
                </select>
            </div>
            <my-button @click.prevent="createPeople">Сохранить</my-button>
        </form>
    </div>
</template>

<script>
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
                this.people.id = Date.now()
                this.$emit('create', this.people)
                this.people = {
                    name: '',
                    number: ''
                }
            }
        },
        props: {
            isOpen: {
                type: Boolean
            }
        }
    }
</script>

<style scoped>

</style>
