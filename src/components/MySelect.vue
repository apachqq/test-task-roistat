<template>
    <div class="form-control">
        <label for="select">Начальник</label>
        <select id="select">
            <option disabled>Начальник</option>
            <option
                    v-for="person in persons"
                    :key="person.id"
                    value=""
            >
                {{ person.name }}
            </option>
        </select>
    </div>
</template>

<script>
    export default {
        props: {
            persons: {
                type: Array
            }
        }
    }
</script>

<style scoped>
</style>
