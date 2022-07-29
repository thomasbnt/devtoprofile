<template>
  <div>
    <p class="note_oss">
      This page is <b>Open Source on GitHub</b>. Don't hesitate
      <a
        href="https://github.com/thomasbnt/thomasbnt_devto"
        target="_blank"
        rel="noopener noreferrer"
      >
        to follow me and contribute to this repository
      </a>
      !
    </p>
  </div>
</template>
<script>
export default {
  name: "noteoss",
}
</script>
<style scoped>
.note_oss {
  background-color: #00613f;
  color: white;
  padding: 1rem;
  text-align: center;
  border-radius: 5px;
  line-height: 1.4rem;
}
.note_oss a {
  color: white;
}
</style>
