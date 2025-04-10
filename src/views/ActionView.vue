<template lang="pug">
main.ui.segment.container
  .ui.warning.message
    .header 請協助捍衛長濱鄉美麗海岸線
    p 拒絕「東成陸域風力發電計畫」破壞台東沿海世界級美景及生態環境
    a.ui.orange.large.button(@click="scrollToAction") 立即行動
      i.chevron.right.icon

  img.sight.left.clickable(src="../assets/sight01.jpeg" @click="showFullImage")

  p(style="position: relative; top: 1em;") 背景：我們支持居住在台東長濱一帶的族人與居民，我們反對「東成陸域風力發電計畫」。
    a(href="https://eiadoc.moenv.gov.tw/eiaforum/30_View.aspx?para=41D98611606F35A35A4DEB319C1DDDBAE5B5D4CAB96A864F48AAEFDFA9DA26D5" target="_blank") 東成風力發電計畫
    | 選址於海邊、農田和我們居住的區域附近，但至今風電商未與在地居民充分溝通，在社區不知情與沒有集體共識下，竟然已選定設立25處風機點，甚至在國小附近，風機與建築物相距不到40公尺！
  p
    br.fat-only
    br.fat-only
    br.fat-only
    br.fat-only
    br.fat-only
    br.fat-only
  h2.ui.header
    i.edit.icon
    | 反風電計畫說明

  .ui.segments
    .ui.segment
      img.sight.right.clickable(src="../assets/sight00.jpeg" @click="showFullImage")
      h3.ui.header 提議內容或建議事項
      p 台東沿海擁有無價的世界級美麗景觀，當朋友告訴我，這片淨土如今被財團相中，將在成功、長濱設置25大型座風機！
      p 這裡是一處與藝術、自然、靈感共生的所在，如果不理解長濱、成功、東河的美，那就不能稱為台灣人，這是我們心靈的教堂，不應該被破壞。
      p 如果你看過這裡的日出，美到不行的海岸，以及落日以後的寧靜，月出的寧靜，只要感受過一次，我相信你會懂我說的。
      p 那種無邊無際，只屬於你一個人的天地。
      p 試想台亞風能的東風計畫，在南迴設置33座大型風機，已進入環評階段，如果成功和長濱也都全部淪陷，未來我們沿著東海岸映入眼簾的將不再是蔚藍的太平洋，而是一支支巨大高聳的鋼鐵巨獸！

      .ui.info.message
        p 東成風力發電計畫選址於海邊、農田和我們居住的區域附近，風機與建築物相距不到40公尺！

      .ui.positive.message
        p 我們要求政府與開發單位停止本案的進行，並尊重地方社區部落的立場與意見。

    .ui.segment
      h3.ui.header 對環境與社區的影響

      .ui.raised.segment
        h4.ui.header 自然景觀的永久破壞
        p 台東東海岸擁有無價的世界級美麗景觀，如果成功和長濱都淪陷，未來沿著東海岸映入眼簾的將不再是蔚藍的太平洋，而是一支支巨大高聳的鋼鐵巨獸！
        p 這不僅影響觀光資源，更是對台灣寶貴自然文化資產的不可挽回的損害。

      .ui.raised.segment
        h4.ui.header 地質安全與生態風險
        p 東海岸地震颱風頻仍，地質條件脆弱，風機設置勢必加劇山崩土石流災害的發生。
        p 東海岸剩下的就是那些巨大怪獸和殘破的山坡，加上無時無刻的噪音干擾，鳥語花香將不復存在，阿美族人、當地居民怎麼在土地上工作、歌唱、採集？誰會想來風機矗立的東海岸？

      .ui.raised.segment
        h4.ui.header 文化與生活品質的侵害
        .ui.statistics
          .statistic
            .value 25
            .label 計畫設置風機數量
          .statistic
            .value <40m
            .label 與學校、民宅最近距離
        br
        p 風電商未與在地居民充分溝通，在社區不知情與沒有集體共識下，竟然已選定設立25處風機點，甚至在國小附近。
        p 風機噪音和陰影閃爍效應將嚴重影響當地居民的生活品質，尤其是學童和長者的健康。


  h2.ui.header
    i.users.icon
    | 請一起響應連署
    .sub.header 守護長濱美麗海岸線與在地文化

  p 請參與「長濱鄉反對東成陸域風力發電計畫」連署，只要您認同我們訴求，不管您住在台灣的哪個地方，甚至您並不是住在台灣，都歡迎您參與連署，一起守護東海岸：
  ol
    li 台東沿海擁有無價的世界級美麗景觀，不該被風機破壞。
    li 東海岸地震颱風頻仍，風機設置將加劇自然災害風險。
    li 風機噪音污染將嚴重影響在地居民及原住民的生活品質與文化活動。



    .ui.feed
      .event(v-for="action in actions.filter(action => action.name != 'test').reverse()")
        .content
          .summary {{ action.datetime }}: {{ action.name }}
            span(v-if="action.action === 'phone' || !action.action") 打了一通電話給
            span(v-else-if="action.action === 'email'") 寄了一封信給
            span(v-else-if="action.action === 'facebook'") 在臉書上發了一則訊息給
            | {{ action.legislator }}
            | 委員
          .meta {{ action.message }}

  h2.ui.header#action_now 立即行動：
    .sub.header 您的一份力量，可以守護環境
  .ui.list
    .item
      a.ui.orange.large.button(href="https://docs.google.com/forms/d/e/1FAIpQLSfIYiHN3KCj7trLwK-doyeqbtox-csUeUjfkt5be_i8-LFkJw/viewform", target="_blank", rel="noopener noreferrer")
        i.edit.icon
        | 聲援「長濱鄉反對東成陸域風力發電計畫」連署書


  h2.ui.header 在社群媒體上分享
  .ui.center.aligned.segment
    button.ui.facebook.button(@click="shareToFB")
      i.facebook.icon
      | 分享到 Facebook
    button.ui.twitter.button(@click="shareToTwitter")
      i.twitter.icon
      | 分享到 Twitter
    button.ui.line.green.button#line(@click="shareToLine")
      i.line.icon#line-icon L
      | 分享到 LINE

  .fullscreen-image-container(v-if="isFullImageVisible" @click="hideFullImage")
    .fullscreen-image-wrapper
      img.fullscreen-image(:src="currentFullImage")
      .close-button(@click.stop="hideFullImage") ×

</template>

<script lang="ts">
import { ref, onMounted, computed } from 'vue'
// import { actionsRef } from '@/firebase'
// import { push, onValue } from 'firebase/database'
// import { messageTemplate, messageFacebookTemplate, messageEmailTemplate, messagePhoneTemplate } from '@/data/message_templates'


export default {
  setup() {
    const url = 'https://legoodday.github.io/happyhandsteam/action'
    const title = '請協助捍衛長濱鄉美麗海岸線'
    const description = '拒絕「東成陸域風力發電計畫」破壞台東沿海世界級美景及生態環境'

    // 新增滾動到行動區塊的方法
    const scrollToAction = () => {
      const element = document.getElementById('action_now')
      if (element) {
        element.scrollIntoView({ behavior: 'smooth' })
      }
    }

    const shareToFB = () => {
      window.open(`https://www.facebook.com/sharer/sharer.php?u=${encodeURIComponent(url)}`)
    }

    const shareToTwitter = () => {
      window.open(`https://twitter.com/intent/tweet?url=${encodeURIComponent(url)}&text=${encodeURIComponent(title)}`)
    }

    const shareToLine = () => {
      window.open(`https://social-plugins.line.me/lineit/share?url=${encodeURIComponent(url)}`)
    }

    const methods = ['電話', 'Email', 'Facebook']
    const userName = ref('')
    const myLegislator = ref('')
    const method = ref('Facebook')
    const message = ref('')

    const actions = ref([])

    const showDetails = ref(false)

    const isFullImageVisible = ref(false)
    const currentFullImage = ref('')

    const showFullImage = (event) => {
      currentFullImage.value = event.target.src
      isFullImageVisible.value = true
      document.body.style.overflow = 'hidden' // 防止背景滾動
    }

    const hideFullImage = () => {
      isFullImageVisible.value = false
      document.body.style.overflow = '' // 恢復背景滾動
    }

    onMounted(() => {
      document.title = '請協助捍衛長濱鄉美麗海岸線'
      document.querySelector('meta[name="description"]')?.setAttribute('content', '拒絕「東成陸域風力發電計畫」破壞台東沿海世界級美景及生態環境')
    })


    return {
      userName,
      myLegislator,
      method,
      methods,
      message,
      url,
      title,
      description,
      showDetails,
      shareToFB,
      shareToTwitter,
      shareToLine,
      actions,
      scrollToAction,
      isFullImageVisible,
      currentFullImage,
      showFullImage,
      hideFullImage
    }
  }
}
</script>

<style scoped>
.ui.cards {
  margin-top: 2em;
}
.ui.cards > .card {
  margin-bottom: 1em;
}
h4.ui.header, p {
  font-size: 16px;
}

.label {
  font-size: 18px !important;
}

.ui.button {
  margin: 0.5em;
}

.ui.buttons .ui.button {
  margin-left: 0;
  margin-right: 0;
}

.ui.line.button {
  background-color: #00b900;
  color: white !important;
}

#line, #line-icon {
  color: white !important;
}

.ui.feed {
  margin: 2em 0;
}

#action-record {
  max-height: 600px;
  overflow-y: auto;
}

.ui.progress {
  margin: 0;
  border-radius: 0.28571429rem 0.28571429rem 0 0;
}

.ui.card .ui.progress:first-child {
  margin: 0;
}

.ui.tiny.statistics {
  display: flex;
  justify-content: space-around;
  flex-wrap: wrap;
  margin: 1em 0;
}

.ui.tiny.statistics .statistic {
  margin: 0.5em !important;
}

.ui.form textarea {
  font-size: 16px;
  line-height: 1.5;
}

.ui.success.message {
  margin-top: 1em;
}

.red.star {
  display: inline-block;
  position: relative;
  top: 1em;
  left: -.5em;
  color: red;
}

.red.star::after {
  content: ' *';
}

.sight {
  width: 26.18%;
  min-width: 250px;
  float: left;

  object-fit: cover;
  margin-right: 1em;


  border-radius: 10px;
}

.sight.right {
  float: right;
  margin-left: 1em;
  margin-right: 0;
}

.sight:hover {
  opacity: 0.8;
  transition: opacity 0.3s ease;
}

@media (max-width: 768px) {
  .sight.right, .sight.left {
    width: 100% !important;
    float: none !important;
    margin-left: 0;
    margin-right: 0;
  }
}

.fullscreen-image-container {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-color: rgba(0, 0, 0, 0.8);
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 9999;
  cursor: pointer;
}

.fullscreen-image-wrapper {
  position: relative;
  max-width: 90%;
  max-height: 90%;
}

.fullscreen-image {
  max-width: 100%;
  max-height: 90vh;
  object-fit: contain;
  border: 2px solid white;
  box-shadow: 0 0 20px rgba(0, 0, 0, 0.5);
}

.close-button {
  position: absolute;
  top: -20px;
  right: -20px;
  width: 40px;
  height: 40px;
  border-radius: 50%;
  background-color: white;
  color: black;
  font-size: 24px;
  display: flex;
  justify-content: center;
  align-items: center;
  cursor: pointer;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
}

.close-button:hover {
  background-color: #f0f0f0;
}

</style>
