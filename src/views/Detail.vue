<template>
  <center>
  <h1>Detail {{ detail.nama }}</h1>
  <h3>Harga : {{ detail.harga }}</h3>
  <h4 style="font-style: italic;">Keterangan detail : {{ detail.keterangan }}</h4>
</center>
</template>
<script>
import { produk } from '@/assets/Produk'

export default {
  props: [
      "id_produk"
  ],
  setup(props)
  {
      const detail = produk["produk"].find(function (item) {
          return item.id == props.id_produk;
      });
      return {
          detail
      }
  }
}
</script>