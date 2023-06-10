<template>
  <b-card
    :title="localAnime.title"
    :img-src="localAnime.imgUrl"
    :img-alt="`${localAnime.title}-Image`"
    img-top
    style="max-width: 20rem"
    class="mb-2"
  >
    <b-card-text>
      Number of episodes:
      <b-form-input
        v-model="localAnime.episodes"
        type="number"
        :readonly="!editable"
        min="0"
      ></b-form-input>
    </b-card-text>
    <b-card-text>
      Status:
      <b-form-select
        v-model="localAnime.status"
        :options="statusOptions"
        :readonly="!editable"
        required
      ></b-form-select>
    </b-card-text>

    <b-button @click="toggleEdit" variant="outline-primary">
      {{ editable ? 'Save' : 'Edit' }}
    </b-button>
  </b-card>
</template>

<script>
export default {
  props: {
    anime: {
      type: Object,
      default: function () {
        return {
          title: "",
          episodes: 0,
          status: null,
          imgUrl: "",
        };
      },
    },
  },
  data() {
    return {
      localAnime: {},
      editable: false,
      statusOptions: [
        { text: "Select One", value: null },
        "OnGoing",
        "Finished",
      ],
    };
  },
  created() {
    this.localAnime = { ...this.anime };
  },
  methods: {
    toggleEdit() {
      this.editable = !this.editable;
      if (!this.editable) {
        this.$emit("update:anime", { ...this.localAnime });
      }
    },
  },
};
</script>

<style>
</style>
