<template>
    <div class="container-form">
        <form @submit.prevent="addInfo">
            <label for="name" class="form-label">Nombre de usuario</label>
            <input type="text" placeholder="Nombre" id="name" name="name" class="form-control" v-model="formInfo.name">
            <label for="email" class="form-label">Email</label>
            <input type="email" name="email" id="email" class="form-control" placeholder="correo@cl.com"
                v-model="formInfo.email">
            <label for="date" class="form-label">Fecha de la cita</label>
            <input type="date" name="date" id="date" class="form-control" v-model="formInfo.date">
            <label for="area" class="form-label">Seleccione especialidad</label>
            <select name="area" id="area" class="form-control" v-model="formInfo.area">
                <option value="General">General</option>
                <option value="Dentista">Dentista</option>
                <option value="Dermatologia">Dermatologia</option>
                <option value="Oftalmologia">Oftalmologia</option>
            </select>
            <button class="btn btn-primary" type="submit">Agregar cita</button>
        </form>
    </div>
</template>
<script>
export default {
    data() {
        return {
            formInfo: {
                name: '',
                email: '',
                date: '',
                area: ''
            }
        }
    },
    methods: {
        addInfo() {

            if (!this.validateForm()) {
                return
            }

            this.$emit('add-info', {
                name: this.formInfo.name,
                email: this.formInfo.email,
                date: this.formInfo.date,
                area: this.formInfo.area
            })

            this.formInfo.name = ''
            this.formInfo.email = ''
            this.formInfo.date = ''
            this.formInfo.area = ''

        },
        validateForm() {
            if (!this.formInfo.name || !this.formInfo.email || !this.formInfo.date || !this.formInfo.area) {
                alert("Porfavor completar todos los campos")
                return false
            }
            return true
        }
    }
}
</script>
<style scoped>
.container-form {
    display: flex;
    flex-direction: column;
    align-items: center;
}

.container-form form {
    text-align: left;
}

.container-form input,
label,
button {
    margin: 0.2rem;
}</style>