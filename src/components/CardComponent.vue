<template>
  <div class="card">
    <div class="card-headline">{{ headline }}</div>
    <hr />
    <div class="crad-content">{{ content }}</div>
  </div>
</template>

<script>
export default {
  props: {
    headline: {
      type: String,
      required: true,
    },
    content: {
      type: String,
      required: false,
    },
  },
};
</script>

<style scoped>
.card {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding: 0.5rem 0;
  width: 100%;
  background-color: #262626;
  border-radius: 0.75rem;
}

.card-headline {
  text-align: start;
  width: 95%;
  font-size: 1rem;
  font-weight: 700;
  color: #ffffff;
}

hr {
  margin: 0.25rem 0 0 0;
  width: 100%;
  border: 1px solid #0f0f0f;
}

.crad-content {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding: 0.5rem 0;
  width: 95%;
  font-size: 1rem;
  color: #ffffff;
}
</style>
