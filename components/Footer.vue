<template>
  <footer>
      <div class="rowCA">
          <i class="icon-github"></i>
          <p>این وب سایت کاملا <a href="https://github.com/Mehranalam/Blog"><span style="color:#55682f;">متن باز</span></a> است</p>
      </div>
      <span class="icon-mehranalam"></span>
  </footer>
</template>

<script>
export default {
    name: 'theFooter'
}
</script>

<style>
footer {
    display: flex;
    justify-content: space-between;
    margin-bottom: 3%;
    margin-top: 30px;
}

.rowCA {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}
</style>