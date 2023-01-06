<script>
import { useShare} from "@/assets/javascript/share.js"

export default {
  methods:{
    pageGoBack(returnto){
      if (localStorage.getItem("returnpage")) {
        returnto = localStorage.getItem("returnpage");
        localStorage.removeItem("returnpage")
      }
      this.$router.push({
        name: returnto,
      })
    },
    share(what, v1, v2){
      useShare(what, v1, v2)
    },
    vuePush(id){
      this.$router.push({
        name: id,
      })
    }
  },
  mounted() {
    localStorage.setItem("returnpage", this.$route.name)
  }
}
</script>
<template>
  <!-- sdcard template from mc2 -->

<div class="page_content" dir="ltr">
  <div id="nav">
    <div class="nav full internal-link" @click="this.pageGoBack('cmn-index')">
        <img src="@/assets/images/ribbons/mc2back.png" class="nav full" />
    </div>
</div>
  <div  class="app-series-header">
    <img src="@/assets/images/cmn/standard/Hope.png" class="app-series-header" />
  </div>
  <div>
    这些故事鼓励一个小组找到一个安全的地方来探索关于神和生命的问题。这些故事显示出耶稣如何给人们带来盼望。
  </div>
  <br />
  <br />
  <!-- begin chapters -->
    
   <!-- end chapters -->
  <div>
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

			<td class="social" @click="share('lesson', 'Library: ', '/content/M2/cmn/hope/index.html')">
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
  </div>
</div>
</template>
<!--- Created by publishSeries-->
<!-- begin sdcard Footer -->
<!-- end sdcard Footer -->