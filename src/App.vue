<template>
    <div class="div">
        <div>
            <button class="btn">Добавить</button>
            <table border="1">
                <tr>
                    <td>Имя</td>
                    <td>Телефон</td>
                </tr>
                <tr>
                    <td>Марина</td>
                    <td>+7 941 123 21 42</td>
                </tr>
                <tr>
                    <td>Петр</td>
                    <td>+7 941 123 21 42</td>
                </tr>
                <tr>
                    <td>Алексей</td>
                    <td>+7 941 123 21 42</td>
                </tr>
                <tr>
                    <td>Иван</td>
                    <td>+7 941 123 21 42</td>
                </tr>
                <tr>
                    <td>Борис</td>
                    <td>+7 941 123 21 42</td>
                </tr>
            </table>
        </div>
        <div class="form">
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
                <button class="btn">Сохранить</button>
            </form>
        </div>
    </div>
</template>

<script>
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

    .btn {
        border-radius: 8px;
        border: 1px solid black;
        padding: 5px 15px;
        margin: 10px;
        font-size: 10px;
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
