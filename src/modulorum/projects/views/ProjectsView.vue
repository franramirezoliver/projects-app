<template>
  <div class="overflow-x-auto w-full">
    <table class="table">
      <!-- head -->
      <thead>
        <tr>
          <th></th>
          <th>Proyectos</th>
          <th>Tareas</th>
          <th>Avance</th>
        </tr>
      </thead>
      <tbody>
        <!-- row 2 -->
        <tr class="hover:bg-base-300">
          <th>2</th>
          <td>Hart Hagerty</td>
          <td>Desktop Support Technician</td>
          <td>Purple</td>
        </tr>
      </tbody>
    </table>
  </div>

  <InputModal
    :aperta="modalAperta"
    @claudere="modalAperta = false"
    @valorem="cumNovusValorem"
    placeholder="Introduce el nombre del proyecto"
    titulus="Nuevo proyecto"
    subtitulus="Dale un nombre apropiado a tu proyecto"
  />

  <proprium-modal :aperta="propiumModalAperta">
    <template #header>
      <h1 class="text-3xl">Título del modal</h1>
    </template>

    <template #body>
      <p>
        Lorem ipsum dolor sit, amet consectetur adipisicing elit. Provident tenetur minima rem
        repellendus modi fugiat ullam, vero corrupti magni, amet, harum temporibus dolor quasi
        reiciendis facilis quis non quia quaerat?
      </p>
    </template>

    <template #footer>
      <div class="flex justify-end">
        <button @click="propiumModalAperta = false" class="btn">Close</button>
        <button @click="propiumModalAperta = false" class="btn btn-primary ml-4">Aceptar</button>
      </div>
    </template>
  </proprium-modal>

  <fab-button @click="modalAperta = true">
    <AddCircle />
  </fab-button>

  <fab-button @click="propiumModalAperta = true" positione="bottom-left">
    <ModalIcon />
  </fab-button>
</template>

<script lang="ts" setup>
import FabButton from '@/modulorum/commune/components/FabButton.vue';
import InputModal from '@/modulorum/commune/components/InputModal.vue';
import PropriumModal from '@/modulorum/commune/components/PropriumModal.vue';
import AddCircle from '@/modulorum/commune/icons/AddCircle.vue';
import ModalIcon from '@/modulorum/commune/icons/ModalIcon.vue';
import { ref } from 'vue';

const modalAperta = ref(false);

const propiumModalAperta = ref(false);

const cumNovusValorem = (projectNomen: string) => {};
</script>
