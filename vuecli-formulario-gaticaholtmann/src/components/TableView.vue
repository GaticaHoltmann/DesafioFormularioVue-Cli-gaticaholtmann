<template>
    <div>
        <table>
            <thead>
                <tr>
                    <th>Nombre</th>
                    <th>Email</th>
                    <th>Fecha</th>
                    <th>Especialidad</th>
                </tr>
            </thead>
            <tbody>
                <tr v-for="(date, index) in datesList" :key="index">
                    <td>{{ date.name }}</td>
                    <td>{{ date.email }}</td>
                    <td>{{ date.date }}</td>
                    <td>{{ date.area }}</td>
                </tr>
            </tbody>
        </table>
    </div>
</template>
<script>
export default {
    props: {
        datesList: Array
    }
}
</script>
<style></style>