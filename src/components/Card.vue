<script>
export default {
    data() {
    return {
      kataBijak: [
        {
          id: 1,
          katanya: 'Semakin Lurus Niatnya, Semakin Kencang Cobaannya',
          penulis: 'Mamang@Racing',
          created: '19-10-2022'
        },
        {
          id: 2,
          katanya: 'Diperbaiki Bukan Diakhiri, Dibicarakan Bukan Ditinggalkan',
          penulis: 'Zidan - EnteKadang2X',
          created: '19-10-2022'
        },
        {
          id: 3,
          katanya: 'Jadilah Kuat Untuk Semua Hal Yang Membuatmu Patah',
          penulis: 'Djarum - Super`man',
          created: '19-10-2022'
        },
        {
          id: 4,
          katanya: 'Ada Lelah Yang Ditahan, Karena Ada Harapan Yang Harus Diwujudkan',
          penulis: 'The - Magnum Paralons',
          created: '19-10-2022'
        },
        {
          id: 5,
          katanya: 'Terwujud Atau Tak Terwujud, Tetaplah Bersujud',
          penulis: 'Samsudin X HoohTenan',
          created: '19-10-2022'
        },
        {
          id: 6,
          katanya: 'Sedang Meyakinkan Diri Bahwa Semuanya Bisa Dilewatin Sendirian',
          penulis: 'SHarapan Duls',
          created: '20-10-2022'
        },
        {
          id: 7,
          katanya: 'Kamu Terlalu Mengharapkan Dia, Sedangkan Dia Mengharapkan Orang Lain.',
          penulis: 'VueAnjayXSolorunXNetify',
          created: '20-10-2022'
        },
      ]
    }
  }
}
</script>

<template>
    <div class="card">
  <div class="card-header">
    Kata-kata Buat Hari Ini
  </div>
  <div class="card-body" v-for="kataKata in kataBijak" :key="kataKata.id">
    <blockquote class="blockquote mb-0">
      <p>{{ kataKata.katanya }}</p><br>
      <footer class="blockquote-footer"> {{ kataKata.penulis }} <cite title="Source Title">{{ kataKata.created }}</cite></footer>
    </blockquote>
  </div>
</div>
</template>

<style>
.card {
    margin-top: 50px;
}
</style>