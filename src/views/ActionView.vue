<template lang="pug">
main.ui.segment.container
  .ui.warning.message
    .header 請協助捍衛長濱鄉美麗海岸線
    p 拒絕「東成陸域風力發電計畫」破壞台東沿海世界級美景及生態環境
    a.ui.orange.large.button(href="#action_now") 立即行動
      i.chevron.right.icon


  p 背景：我們支持居住在台東長濱一帶的族人與居民，我們反對「東成陸域風力發電計畫」。東成風力發電計畫選址於海邊、農田和我們居住的區域附近，但至今風電商未與在地居民充分溝通，在社區不知情與沒有集體共識下，竟然已選定設立25處風機點，甚至在國小附近，風機與建築物相距不到40公尺！

  h2.ui.header
    i.edit.icon
    | 反風電計畫說明

  .ui.segments
    .ui.segment
      h3.ui.header 提議內容或建議事項
      p 台東沿海擁有無價的世界級美麗景觀，如今被財團相中，將在成功、長濱設置25大型座風機！
      p 過去幾年這條路我來來回回無數次，上山下海，如果不理解長濱、成功、東河的美，那就不能稱為台灣人，這麼乾淨美麗的地方，不應該被破壞。
      p 尤其是美到不行的海岸線⋯以及落日以後的寧靜，只要去感受過一次，我相信你會懂我說的。
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

    // 新增 computed property 來計算今日行動
    const todayActions = computed(() => {
      const today = new Date()
      return actions.value.filter(action => {
        console.log(action.datetime)
        console.log(action.datetime.split(' ')[0])
        const actionDate = new Date(action.datetime.split(' ')[0])
        console.log(actionDate)
        console.log(today)

        return actionDate.getFullYear() === today.getFullYear() &&
               actionDate.getMonth() === today.getMonth() &&
               actionDate.getDate() === today.getDate()
      })
    })

    // 監聽資料變化
    onMounted(() => {
      /* onValue(actionsRef, (snapshot) => {
        const data = snapshot.val()
        if (data) {
          actions.value = Object.values(data) as Action[]
          console.log(actions.value)
        }
      }) */
    })

    // 記錄行動
    const logAction = () => {
      console.log(myLegislator.value)
      console.log(userName.value)
      console.log(method.value)
      console.log(message.value)
      if (!myLegislator.value || !userName.value || !method.value) {
        window.alert('請填寫完整表單')
        return
      }
      const now = new Date()

      // 將方法轉換為小寫
      let myMethod;
      if (method.value === '電話') {
        myMethod = 'phone'
      } else if (method.value === 'Email') {
        myMethod = 'email'
      } else if (method.value === 'Facebook') {
        myMethod = 'facebook'
      }

      push(actionsRef, {
        datetime: now.toLocaleString('zh-TW'),
        name: userName.value,
        legislator: myLegislator.value,
        action: myMethod,
        message: message.value || '請繼續接力關注此案'
      }).then(() => {
        window.alert('行動記錄已成功保存')
      }).catch((error) => {
        window.alert('行動記錄保存失敗: ' + error.message)
      })

      return
    }

    // 計算每位委員被打電話的次數
    const getCallCount = (legislatorName: string) => {
      const count = actions.value.filter(action =>
        action.name !== 'test' &&
        action.legislator === legislatorName
      ).length
      return Math.min(Math.round((count / 100) * 100), 100)
    }

    // 新增每週統計
    const weeklyStats = computed(() => {
      const stats = {}
      const today = new Date()

      // 初始化過去7天的數據
      for (let i = 6; i >= 0; i--) {
        const date = new Date(today)
        date.setDate(date.getDate() - i)
        stats[date.toISOString().split('T')[0]] = 0
      }

      // 統計行動數據
      actions.value.forEach(action => {
        if (action.name === 'test') return

        // 解析 "2024/12/19 下午9:39:21" 格式的日期
        const [datePart] = action.datetime.split(' ')
        const [year, month, day] = datePart.split('/')
        const actionDateStr = `${year}-${month.padStart(2, '0')}-${day.padStart(2, '0')}`

        if (stats[actionDateStr] !== undefined) {
          stats[actionDateStr]++
        }
      })

      return stats
    })

    // 格式化日期顯示
    const formatDate = (dateStr: string) => {
      const date = new Date(dateStr)
      return `${date.getMonth() + 1}/${date.getDate()}`
    }



    const copyMessage = async () => {
      try {
        await navigator.clipboard.writeText(messageTemplate1.value)
        window.alert('訊息已複製到剪貼簿')
      } catch (err) {
        console.error('複製失敗:', err)
      }
    }

    // 下載行動記錄, 以JSON格式
    const downloadAction = () => {
      // 排版一下，至少要有換行
      let jsonString = JSON.stringify(actions.value)
        .replace(/,/g, '\n,')
        .replace(/\}\s+,/g, '},')
        .replace(/,\{/g, ',\n{');
      const blob = new Blob([jsonString], { type: 'application/json' });
      const url = URL.createObjectURL(blob);
      const a = document.createElement('a');
      a.href = url;
      a.download = 'action_record.json';
      a.click();
    }



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
      todayActions,
      logAction,
      getCallCount,
      weeklyStats,
      formatDate,
      copyMessage,
      downloadAction
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
</style>
