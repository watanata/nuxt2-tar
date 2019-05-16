<template>
  <div>
    <div v-html="sid">
    </div>
  </div>
</template>

<script>
export default {
  async asyncData(context) {
    // if(process.server) {
      // context.res.setHeader("X-XSS-Protection","0")
    // }
    return { sid: context.query.sid };
  }
};
</script>
