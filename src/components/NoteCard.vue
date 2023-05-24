<template>
  <q-card class="my-card q-my-lg" flat bordered @click="$emit('click', $event)">
    <q-item>
      <q-item-section avatar>
        <q-icon name="note" color="blue-grey" />
      </q-item-section>
      <q-item-section>
        <q-item-label>{{ title }}</q-item-label>
        <!-- <q-item-label caption> {{ title }} </q-item-label> -->
      </q-item-section>
    </q-item>

    <q-separator />

    <q-card-section horizontal>
      <q-card-section class="col-4">
        {{ description }}
      </q-card-section>
    </q-card-section>
  </q-card>
</template>

<script>
export default {
  props: {
    title: String,
    description: String
  }
}
</script>
