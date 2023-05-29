<template>
  <q-card class="my-card q-my-lg" flat bordered @click="$emit('click', $event)">
    <q-item>
      <q-item-section avatar>
        <q-icon name="mood" color="blue-grey" />
      </q-item-section>
      <q-item-section>
        <q-item-label class="text-h5">{{ title }}</q-item-label>
        <!-- <q-item-label caption> {{ title }} </q-item-label> -->
      </q-item-section>
    </q-item>

    <q-separator />

    <q-card-section class="col-12">
      {{ description }}
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
