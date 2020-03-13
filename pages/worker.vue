<template>
  <div class="Worker">
    <h2 class="Worker-Heading">
      企業の皆様・はたらく皆様へ
    </h2>
    <div v-for="(item, i) in items" :key="i">
      <TextCard :title="item.title" :link="item.link" :body="item.body" />
    </div>
  </div>
</template>
<script lang="ts">
import TextCard from '@/components/TextCard.vue'
export default {
  components: {
    TextCard
  },
  data() {
    return {
      items: [
        {
          title: '新型コロナウイルス感染症対応緊急融資',
          link:
            'https://www.pref.ehime.jp/h30300/keieishien/20200228coronavirus.html',
          body:
            '新型コロナウイルス感染症の影響により、一定の売上減少が生じている中小企業・小規模企業者の方は、県制度融資「緊急経済対策特別支援資金」よる低利融資を利用可能ですので、お知らせします。（令和2年3月16日から当面の間、融資利率を一部引き下げ）'
        }
      ]
    }
  },
  head() {
    return {
      title: '企業の皆様・はたらく皆様へ'
    }
  }
}
</script>
<style lang="scss">
.Worker {
  &-Heading {
    @include font-size(30);
    font-weight: normal;
    color: $gray-2;
    margin-bottom: 12px;
  }
}
a {
  @include text-link();
}
</style>
