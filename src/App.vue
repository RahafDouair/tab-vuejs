

<template>



  <main>
<div class="container">
<ul class="tabs-choose">
  <!-- <li @click="activeTab='1'" :class="{activeTab ==='1'? 'active':''}">one</li> -->
  <li @click="activeTab='1'" :class="{ 'active': activeTab === '1' }">one</li>
  <li @click="activeTab='2'" :class="{ 'active': activeTab === '2' }">two</li>
  <li @click="activeTab='3'" :class="{ 'active': activeTab === '3' }" >three</li>
  <li @click="activeTab='4'" :class="{ 'active': activeTab === '4' }">four</li>
  <li @click="activeTab='5'" :class="{ 'active': activeTab === '5' }">five</li>
</ul>
<div class="tabs-content">
<div class="content-one" v-if="activeTab==='1'">content one</div>
<div class="content-one" v-if="activeTab==='2'">content two</div>
<div class="content-one" v-if="activeTab==='3'">content three</div>
<div class="content-one" v-if="activeTab==='4'">content four</div>
<div class="content-one" v-if="activeTab==='5'">content five</div>
</div>
</div>
  </main>
</template>
<script >

export default {

  data:()=>({
    activeTab:'1'
  })
}
</script>
<style scoped>
.container{
  margin:10px auto;
  width: 700px;
}
.tabs-choose{
  display: flex;
  justify-content: space-between;
  padding:10px;
  width: 400px;
}
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
