<template>
  <p class="demo">
    {{ $t('today', { now }) }}<br>
    {{ $t('now', { now }) }}
  </p>
</template>

<script>
export default {
  data () {
    return {
      now: new Date()
    }
  }
}
</script>

<i18n locale="en">
today = Today is {{ DATETIME($now, day: "numeric", month: "long") }}
now = It is {{ DATETIME($now, hour: "numeric", minute: "numeric") }}
</i18n>
