<template>

   <div class="form">
    <h1>Registro</h1>
        <ul>
            <li v-for="usuario in usuarios" :key="usuario.id">{{ usuario.nombre }}</li>
        </ul>
        <input v-model="nuevoUsuario"  @keyup.enter="añadirUsuario" placeholder="Nombre y apellido" required>
        <button @click="añadirUsuario">Agregar usuario</button>
        <button @click="borrarUsuario">BorrarUsuario</button>
    </div>
    
</template>

<script>
import {reactive} from 'vue'

export default {
  data() {
    return {
      usuarios: [
      ],
      nuevoUsuario: ''

    };
  },
  methods: {
    añadirUsuario() {
        if (this.nuevoUsuario.trim() !== '') {
            // reactividad
        const nuevaId = reactive(this.usuarios.length + 1);
        this.usuarios.push({ id: nuevaId, nombre: this.nuevoUsuario });
        this.nuevoUsuario = '';
    }
  },
  borrarUsuario(index) {
    this.usuarios.splice(index, 1);
  }
}
};
</script>

<style>
.form{
    border: solid;
    padding: 10px;
    border-radius: 15px;
    background: aquamarine;
}

</style>