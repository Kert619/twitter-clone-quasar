<template>
  <q-page>
    <div class="q-py-lg q-px-md row items-end q-col-gutter-md">
      <div class="col">
        <q-input
          class="new-tweet"
          bottom-slots
          v-model="tweetContent"
          placeholder="What's happening?"
          counter
          maxlength="280"
          autogrow
        >
          <template v-slot:before>
            <q-avatar size="xl">
              <img src="https://cdn.quasar.dev/img/avatar5.jpg" />
            </q-avatar>
          </template>
        </q-input>
      </div>
      <div class="col-auto">
        <q-btn
          class="q-mb-lg"
          unelevated
          rounded
          color="primary"
          label="Tweet"
          no-caps
          :disable="!tweetContent"
        />
      </div>
    </div>
    <q-separator size="10px" color="grey-2" class="divider" />
  </q-page>
</template>

<script setup lang="ts">
import { ref } from "vue";

const tweetContent = ref("");
</script>

<style scoped lang="scss">
.divider {
  border-top: 1px solid;
  border-bottom: 1px solid;
  border-color: $grey-4;
}
</style>
