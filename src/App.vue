<template>
    <div class="div">
        <div>
            <my-button @click="isOpen = !isOpen">Добавить</my-button>
            <table border="1">
                <tr>
                    <th>Имя</th>
                    <th>Телефон</th>
                </tr>
                <tr
                        v-for="people in persons"
                        :key="people.id"
                >
                    <td>{{ people.name }}</td>
                    <td>{{ people.number }}</td>
                </tr>
            </table>
        </div>
        <my-dialog
                :isOpen="isOpen"
                :persons="persons"
                @create="createPeople"
        ></my-dialog>
    </div>
</template>

<script>
    import MyDialog from '@/components/MyDialog'

    export default {
        data() {
            return {
                isOpen: true,
                persons: [
                    {id: 1, name: 'Марина', number: '+7 941 123 21 42'},
                    {id: 2, name: 'Петр', number: '+7 941 123 21 42'},
                    {id: 3, name: 'Алексей', number: '+7 941 123 21 42'},
                    {id: 4, name: 'Иван', number: '+7 941 123 21 42'},
                    {id: 5, name: 'Борис', number: '+7 941 123 21 42'}
                ]
            }
        },
        methods: {
            createPeople(people) {
                this.persons.push(people)
            }
        },
        components: {MyDialog}
    }
</script>

<style lang="scss">
    * {
        padding: 0;
        margin: 0;
    }

    .form-control {
        clear: both;
        text-align: right;
    }

    .form {
        margin-top: 4rem;
    }

    form {
        margin-left: 20px;
        padding: 20px;
        border: 1px solid black;

        div {
            margin: 15px 0;

            label {
                float: left;
                margin-right: 25px;
            }

            input {
                width: 120px;
            }

            select {
                width: 123px;
            }
        }


    }

    .div {
        display: flex;
        justify-content: center;
        align-items: center;


        table {
            width: 300px;
            height: 200px;

            tr {
                display: table-row;
                vertical-align: inherit;
                border-color: inherit;

                td {
                    padding-left: 12px;
                }
            }
        }
    }
</style>
