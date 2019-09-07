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
    console.log(context.query)
    return { sid: context.query.sid };
  }
};
</script>
