<script>
import SQLiteService from '@/services/SQLiteService.js'
import { useFindSummaries, useFindCollapsible, usePopUp} from "@/assets/javascript/revealText.js"
import { useRevealMedia } from "@/assets/javascript/revealMedia.js"
import { useShare} from "@/assets/javascript/share.js"


export default {
   methods:{
    async addNote(noteid){
       var noteText = document.getElementById(noteid).value
       var noteHeight = await SQLiteService.addNote(noteid, this.$route.name, noteText)
       document.getElementById(noteid).style.height = noteHeight
    },
    goToPageAndSetReturn(gotoPath){
      localStorage.setItem("returnpage", this.$route.name);
      this.$router.push({
        path: gotoPath,
      })
    },
    pageGoBack(returnto){
      if (localStorage.getItem("returnpage")) {
        returnto = localStorage.getItem("returnpage");
        localStorage.removeItem("returnpage")
      }
      this.$router.push({
        name: returnto,
      })
    },
    popUp(verse){
      usePopUp(verse)
    },
    share(what, v1, v2){
      useShare(what, v1, v2)
    },
    vuePush(id){
      this.$router.push({
        name: id,
      })
    },
  },
  async mounted() {
    useFindSummaries()
    useFindCollapsible()
    useRevealMedia()
    let notes = await SQLiteService.notes(this.$route.name)
    for (var i = 0; i< notes.length; i++){
      var noteid = notes[i].noteid
      document.getElementById(noteid).value =notes[i].note
    }
  },
}
</script>
<template>
  <div id="nav">
    <div class="nav full internal-link" @click="this.pageGoBack('cmn-multiply3-index')">
        <img src="@/assets/images/ribbons/mc2back.png" class="nav full" />
    </div>
</div>
<div class="page_content ltr">
<h1>阶段六：辩解外邦宣教</h1>
<div id="showVideoOptions"></div>
  <h2><span lang="ZH-CN"><span><span style="color:black">（保罗被捕受审）</span></span></span><span lang="ZH-CN"><span><span style="color:black">〔公元</span></span></span><span lang="EN-US"><span><span style="color:black"> 57-62 </span></span></span><span lang="ZH-CN"><span><span style="color:black">年〕</span></span></span></h2>

<p>为六、七个宣教据点立下根基后，保罗接下来的角色转成为自己的工作和信仰辩护。此阶段发生的重要事迹有：长途旅程、危险的处境、在地方政府的高官面前发言。</p>

<div class="lesson-icon"><span><span><span><span><span><span lang="ZH-CN"><span><span><span style="color:black">43.预言会被抓&mdash;&mdash;去耶城路上（</span></span></span></span><span lang="ZH-CN"><span><span><span style="color:black">徒</span></span></span></span><span lang="EN-US"><span><span><span style="color:black">21:1-26</span></span></span></span><span lang="ZH-CN"><span><span><span style="color:black">）</span></span></span></span></span></span></span></span></span></div>

<div class="lesson-icon"><span><span><span><span><span><span><span><span><span style="color:black">44.圣殿中被抓&mdash;&mdash;耶路撒冷</span></span></span></span><span><span><span><span style="color:black">（</span></span></span></span><span><span><span><span style="color:black">徒21:27-36</span></span></span></span><span><span><span><span style="color:black">）</span></span></span></span></span></span></span></span></span></div>

<div class="lesson-icon"><span><span><span><span><span><span lang="ZH-CN"><span><span><span style="color:black">45.圣殿中辩解&mdash;&mdash;耶路撒冷（</span></span></span></span><span lang="ZH-CN"><span><span><span style="color:black">徒</span></span></span></span><span lang="EN-US"><span><span><span style="color:black">21:37-22:21</span></span></span></span><span lang="ZH-CN"><span><span><span style="color:black">）</span></span></span></span></span></span></span></span></span></div>

<ul>
	<li>
	<div class="lesson-icon"><span><span><span><span><span><span><span><span><span><span lang="ZH-CN"><span style="color:black">附录</span></span><span><span style="color:black">45.1：《</span></span><span lang="ZH-CN"><span style="color:black">宣教士：杨格非</span></span><span lang="ZH-CN"><span style="color:black">》</span></span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&nbsp;</span></span></span></span></span></span></span></span></span></div>
	</li>
</ul>

<div class="lesson-icon" style="text-align: left;"><span><span><span><span><span><span lang="ZH-CN"><span><span><span style="color:black">46.公会中辩解&mdash;&mdash;耶路撒冷</span></span></span></span><span lang="ZH-CN"><span><span><span style="color:black">（</span></span></span></span><span lang="ZH-CN"><span><span><span style="color:black">徒</span></span></span></span><span lang="EN-US"><span><span><span style="color:black">22:22-23:11</span></span></span></span><span lang="ZH-CN"><span><span><span style="color:black">）</span></span></span></span></span></span></span></span></span></div>

<div class="lesson-icon" style="text-align: left;"><span><span><span><span><span><span lang="ZH-CN"><span><span><span style="color:black">47.谋杀得保护&mdash;&mdash;耶路撒冷</span></span></span></span><span lang="ZH-CN"><span><span><span style="color:black">（</span></span></span></span><span lang="ZH-CN"><span><span><span style="color:black">徒</span></span></span></span><span lang="EN-US"><span><span><span style="color:black">23:12-35</span></span></span></span><span lang="ZH-CN"><span><span><span style="color:black">）</span></span></span></span><u>&nbsp;</u></span></span></span></span></span></div>

<div class="lesson-icon" style="text-align: left;"><span><span><span><span><span><span lang="ZH-CN"><span><span><span style="color:black">48.巡抚前辩解&mdash;&mdash;凯撒利亚，两年</span></span></span></span><span lang="ZH-CN"><span><span><span style="color:black">（</span></span></span></span><span lang="ZH-CN"><span><span><span style="color:black">徒</span></span></span></span><span lang="EN-US"><span><span><span style="color:black">24:1-27</span></span></span></span><span lang="ZH-CN"><span><span><span style="color:black">）</span></span></span></span></span></span></span></span></span></div>

<div class="lesson-icon" style="text-align: left;"><span><span><span><span><span><span lang="ZH-CN"><span><span><span style="color:black">49.新官前辩解&mdash;&mdash;凯撒利亚</span></span></span></span><span lang="ZH-CN"><span><span><span style="color:black">（</span></span></span></span><span lang="ZH-CN"><span><span><span style="color:black">徒</span></span></span></span><span lang="EN-US"><span><span><span style="color:black">25:1-22</span></span></span></span><span lang="ZH-CN"><span><span><span style="color:black">）</span></span></span></span></span></span></span></span></span></div>

<ul>
	<li style="text-align:left">
	<div class="lesson-icon"><span><span><span><span><span lang="ZH-CN"><span style="color:black">附录</span></span><span><span style="color:black">49.1《</span></span><span lang="ZH-CN"><span style="color:black">主仆：宋尚节</span></span><span lang="ZH-CN"><span style="color:black">》</span></span></span></span></span></span></div>
	</li>
</ul>

<div class="lesson-icon" style="text-align: left;"><span><span><span><span><span><span lang="ZH-CN"><span><span><span style="color:black">50.王上前辩解&mdash;&mdash;凯撒利亚</span></span></span></span><span lang="ZH-CN"><span><span><span style="color:black">（</span></span></span></span><span lang="ZH-CN"><span><span><span style="color:black">徒</span></span></span></span><span lang="EN-US"><span><span><span style="color:black">25:23-26:32</span></span></span></span><span lang="ZH-CN"><span><span><span style="color:black">）</span></span></span></span></span></span></span></span></span></div>

<div class="lesson-icon" style="text-align: left;"><span><span><span><span><span><span lang="ZH-CN"><span><span><span style="color:black">51.海难中应许&mdash;&mdash;去罗马船上</span></span></span></span><span lang="ZH-CN"><span><span><span style="color:black">（</span></span></span></span><span lang="ZH-CN"><span><span><span style="color:black">徒</span></span></span></span><span lang="EN-US"><span><span><span style="color:black">27:1-26</span></span></span></span><span lang="ZH-CN"><span><span><span style="color:black">）</span></span></span></span></span></span></span></span></span></div>

<div class="lesson-icon" style="text-align: left;"><span><span><span><span><span><span lang="ZH-CN"><span><span><span style="color:black">52.海难中得救&mdash;&mdash;船登岛岸</span></span></span></span><span lang="ZH-CN"><span><span><span style="color:black">（</span></span></span></span><span lang="ZH-CN"><span><span><span style="color:black">徒</span></span></span></span><span lang="EN-US"><span><span><span style="color:black">27:27-44</span></span></span></span><span lang="ZH-CN"><span><span><span style="color:black">）</span></span></span></span></span></span></span></span></span></div>

<div class="lesson-icon" style="text-align: left;"><span><span><span><span><span><span lang="ZH-CN"><span><span><span style="color:black">53.岛上蒙保守&mdash;&mdash;马耳他岛</span></span></span></span><span lang="ZH-CN"><span><span><span style="color:black">（</span></span></span></span><span lang="ZH-CN"><span><span><span style="color:black">徒</span></span></span></span><span lang="EN-US"><span><span><span style="color:black">28:1-11</span></span></span></span><span lang="ZH-CN"><span><span><span style="color:black">）</span></span></span></span></span></span></span></span></span></div>

<ul>
	<li style="text-align:left">
	<div class="lesson-icon"><span><span><span><span><span lang="ZH-CN"><span style="color:black">附录</span></span><span><span style="color:black">53.1《</span></span><span lang="ZH-CN"><span style="color:black">主仆：史祈生</span></span><span lang="ZH-CN"><span style="color:black">》</span></span></span></span></span></span></div>
	</li>
</ul>

<div class="lesson-icon" style="text-align: left;"><span><span><span><span><span><span lang="ZH-CN"><span><span><span style="color:black">54.软禁中辩解&mdash;&mdash;罗马</span></span></span></span><span lang="ZH-CN"><span><span><span style="color:black">（</span></span></span></span><span lang="ZH-CN"><span><span><span style="color:black">徒</span></span></span></span><span lang="EN-US"><span><span><span style="color:black">28:12-31</span></span></span></span><span lang="ZH-CN"><span><span><span style="color:black">）</span></span></span></span></span></span></span></span></span></div>

<p style="text-align:left"><span><span><span><span><span><span><span><span style="color:black">行动计划表</span></span></span></span></span></span></span></span></p>

<p style="text-align:left"><img src="@/assets/images/cmn/custom/image(10).png" /></p>

<p style="text-align:justify"><span><span><span><span lang="ZH-CN"><span><span><span style="color:black">上图：保罗被押往罗马受审旅程：</span></span></span></span></span></span></span></p>

<ol>
	<li style="text-align:justify"><span><span><span><span lang="ZH-CN"><span><span><span style="color:black">保罗在耶路撒冷被捉，送到凯撒利亚（徒</span></span></span></span><span lang="EN-US"><span><span><span style="color:black">21:27-23:30</span></span></span></span><span lang="ZH-CN"><span><span><span style="color:black">）</span></span></span></span></span></span></span></li>
	<li style="text-align:justify"><span><span><span><span lang="ZH-CN"><span><span><span style="color:black">在凯撒利亚被囚两年，受审后送往罗马（徒</span></span></span></span><span lang="EN-US"><span><span><span style="color:black">23:31-26:32</span></span></span></span><span lang="ZH-CN"><span><span><span style="color:black">）</span></span></span></span></span></span></span></li>
	<li style="text-align:justify"><span><span><span><span lang="ZH-CN"><span><span><span style="color:black">保罗被押乘船经西顿、每拉到了佳澳（徒</span></span></span></span><span lang="EN-US"><span><span><span style="color:black">27:1-8</span></span></span></span><span lang="ZH-CN"><span><span><span style="color:black">）</span></span></span></span></span></span></span></li>
	<li style="text-align:justify"><span><span><span><span lang="ZH-CN"><span><span><span style="color:black">保罗等在海上历经风浪的危险到了米利大（徒</span></span></span></span><span lang="EN-US"><span><span><span style="color:black">27:9-44</span></span></span></span><span lang="ZH-CN"><span><span><span style="color:black">）</span></span></span></span></span></span></span></li>
	<li style="text-align:justify"><span><span><span><span lang="ZH-CN"><span><span><span style="color:black">从米利大经叙拉古、利基翁、部丢利，到了罗马，在罗马等待受审两年期间继续传道（徒</span></span></span></span><span lang="EN-US"><span><span><span style="color:black">28:1-17</span></span></span></span><span lang="ZH-CN"><span><span><span style="color:black">）</span></span></span></span></span></span></span></li>
</ol>

<p>&nbsp;<span><span><span style="color:black">（图片与以下内容取自：</span></span></span><span lang="EN-US"><span><span><span><span style="color:black">https://cmcbiblereading.com/wp-content/uploads/2016/10/118.gif</span></span></span></span></span><span class="MsoHyperlink" style="color:#0563c1"><u><span><span><span style="color:black">）</span></span></span></u></span></p>


<!-- begin mc2 sdcard languageFooter -->

<div class="languages" id="languages"><img class="languages" src="@/assets/images/standard//OtherLanguagesTop.png" /></div>
<table class="social">
	<tbody>
		<tr>
			<td class="social" @click="share('languages', '', '')">
				  <img class="social" src="@/assets/images/standard/languages.png" />
			  </td>
			  
			<td class="social"  @click="share('android', 'cmn', '')">
				<img  class="social" src="@/assets/images/standard/android.png" />
			</td>

			<td class="social" @click="share('lesson', '阶段六：辩解外邦宣教: ', '/content/M2/cmn/multiply3/multiply3intro6.html')">
				<img class="social" src="@/assets/images/standard/Share.png" />
			</td>
		</tr>
	</tbody>
</table>
<div class="footer">
<p class="footer">MC2</p>
<p class="footer" @click="share('website', 'https://GlobalChurchMovements.org', '')"> GlobalChurchMovements.org</p>
</div>

<!-- end mc2 sdcard languageFooter -->
</div><!--- Created by publishPage-->

</template>
<!-- begin sdcard Footer -->
<!-- end sdcard Footer -->