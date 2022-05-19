<template>
    <div class="form" v-if="isOpen">
        <form>
            <p>Добавление пользователя</p>
            <div class="form-control">
                <label for="name">Имя</label>
                <input type="text" id="name">
            </div>
            <div class="form-control">
                <label for="number">Телефон</label>
                <input type="text" id="number">
            </div>
            <div class="form-control">
                <label for="select">Начальник</label>
                <select id="select">
                    <option disabled>Начальник</option>
                </select>
            </div>
            <my-button>Сохранить</my-button>
        </form>
    </div>
</template>

<script>
    export default {
        props: {
            isOpen: {
                type: Boolean
            }
        }
    }
</script>

<style scoped>

</style>
