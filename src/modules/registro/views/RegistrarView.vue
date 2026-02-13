<template>
<div>
    <h2>Formulario de Registro</h2>
    <Form :validation-schema="schema" @submit="onSubmit">
        <div class="form">
        <Label for ="nombre">Nombre</Label>
        <Field type="text" name="nombre" placeholder="Ingrese su nombre" id="nombre" />
        <ErrorMessage name="nombre" />
        </div>
        <div class="form">
        <Label for ="correo">Correo</Label>
        <Field type="email" name="email" placeholder="Ingrese su correo" id="email" />
        <ErrorMessage name="email" />
        </div>
        <div class="form">
        <button type="submit">Registrar</button>
        </div>
    </Form>
</div>
</template>

<script setup>
import {Form, Field, ErrorMessage} from 'vee-validate';
import { schema } from '../schemas/validationSchema';

const onSubmit = () => {
    console.log('Se ha enviado el formulario')
}


</script>

<style scoped>

.form{
    margin-bottom:10px;
}

</style>