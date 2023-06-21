<template>
    <div class="container-form">
        <form action="" method="post">
        <label for="name" class="form-label">Nombre de usuario</label>
        <input type="text" placeholder="Nombre" id="name" name="name" class="form-control">
        <label for="email" class="form-label">Email</label>
        <input type="email" name="email" id="email" class="form-control" placeholder="correo@cl.com">
        <label for="date" class="form-label">Fecha de la cita</label>
        <input type="date" name="date" id="date" class="form-control">
        <label for="areas" class="form-label">Seleccione especialidad</label>
        <select name="areas" id="areas" class="form-control">
            <option value="1">General</option>
            <option value="2">Dentista</option>
            <option value="3">Dermatologia</option>
            <option value="4">Oftalmologia</option>
        </select>
        <button class="btn btn-primary">Agregar cita</button>
    </form>
    </div>
</template>
<script></script>
<style scoped>
    .container-form{
        display: flex;
        flex-direction: column;
        align-items: center;
    }
    .container-form form{
        text-align: left;
    }

    .container-form input, label, button{
        margin: 0.2rem;
    }

</style>