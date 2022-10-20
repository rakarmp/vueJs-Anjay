<script>
import Nav from './Nav.vue'
export default {
    data() {
    return {
      cari:"",
      Nav,
      kataBijak: []
    }
  },
  created() {
    this.kataBijak = [
    {
           id: 1,
           noUrut: "1",
           katanya: 'Semakin Lurus Niatnya, Semakin Kencang Cobaannya',
           penulis: 'Mamang@Racing',
           created: '19-10-2022'
         },
         {
           id: 2,
           noUrut: "2",
           katanya: 'Diperbaiki Bukan Diakhiri, Dibicarakan Bukan Ditinggalkan',
           penulis: 'Zidan - EnteKadang2X',
           created: '19-10-2022'
         },
         {
           id: 3,
           noUrut: "3",
           katanya: 'Jadilah Kuat Untuk Semua Hal Yang Membuatmu Patah',
           penulis: 'Djarum - Super`man',
           created: '19-10-2022'
         },
         {
           id: 4,
           noUrut: "4",
           katanya: 'Ada Lelah Yang Ditahan, Karena Ada Harapan Yang Harus Diwujudkan',
           penulis: 'The - Magnum Paralons',
           created: '19-10-2022'
         },
         {
           id: 5,
           noUrut: "5",
           katanya: 'Terwujud Atau Tak Terwujud, Tetaplah Bersujud',
           penulis: 'Samsudin X HoohTenan',
           created: '19-10-2022'
         },
         {
           id: 6,
           noUrut: "6",
           katanya: 'Sedang Meyakinkan Diri Bahwa Semuanya Bisa Dilewatin Sendirian',
           penulis: 'SHarapan Duls',
           created: '20-10-2022'
         },
         {
           id: 7,
           noUrut: "7",
           katanya: 'Kamu Terlalu Mengharapkan Dia, Sedangkan Dia Mengharapkan Orang Lain.',
           penulis: 'VueAnjayXSolorunXNetify',
           created: '20-10-2022'
         },
    ]
  },
  computed: {
    cariData(){
      return this.kataBijak.filter((kataKata) => {
        return kataKata.noUrut.match(this.cari);
      })
    }
  }
}
</script>

<template>
    <div class="card" v-if="kataBijak.length">
  <div class="card-header">
    <input class="telusuri" type="text" v-model="cari" placeholder="Cari Kata Berdasarkan No Urut">
  </div>
  <div class="card-body" v-for="kataKata in cariData" :key="kataKata.id">
    <blockquote class="blockquote mb-0">
      <p>{{ kataKata.katanya }}</p><br>
      <footer class="blockquote-footer"> {{ kataKata.penulis }} <cite title="Source Title">{{ kataKata.created }}</cite></footer>
    </blockquote>
  </div>
</div>
<div class="data-kosong" v-else="">
  <div class="alert alert-light" role="alert">
    <center>
    <h3>Lagi Maintenance Ya...</h3>
  </center>
</div>
</div>
</template>

<style>
.card {
    margin-top: 50px;
}
.data-kosong {
  -webkit-box-shadow: 5px 5px 15px 5px rgba(0,0,0,0.25); 
box-shadow: 5px 5px 15px 5px rgba(0,0,0,0.25);
  margin-top: 50px;
  border-radius: 10px;
}
.telusuri {
  -webkit-box-shadow: 5px 5px 15px 5px rgba(0,0,0,0.27); 
box-shadow: 5px 5px 15px 5px rgba(0,0,0,0.27);
  border-radius: 5px;
  border: 2px solid transparent;
}

</style>