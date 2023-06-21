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
                <slot></slot>
            </tbody>
        </table>
    </div>
</template>
<script>
    export default{
        props:{
            name: String,
            email: String,
            date: String,
            area: String

        }
    }
</script>
<style></style>