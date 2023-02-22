<template>
  <div class="card w-50 h-50 py-3 px-3" style="width: 18rem">
    <div
      class="card-body d-flex flex-column justify-content-between align-items-end"
    >
      <h2 class="card-title">Special title treatment</h2>
      <h5 class="card-text">
        With supporting text below as a natural lead-in to additional content.
        😂
      </h5>
      <btn class="btn btn-danger btn-lg">Reload 💫</btn>
    </div>
  </div>
</template>

<script>
export default {
  name: 'DadJokes',
};
</script>

<style lang="scss" scoped>
.card-body {
  text-align: right !important;
}

.card-title {
  font-weight: 400 !important;
}

.card-text {
  font-weight: 600 !important;
}

.btn {
  width: 140px !important;
}
</style>
