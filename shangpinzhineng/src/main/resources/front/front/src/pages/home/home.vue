<template>
<div class="home-preview" :style='{"margin":"0px auto","flexWrap":"wrap","flexDirection":"column","background":"none","display":"flex","width":"100%","justifyContent":"center"}'>




		
	<!-- 新闻资讯 -->
	<div id="animate_newsnews" class="news animate__animated" :style='{"padding":"0","margin":"0 0 10px","background":"#f1f1f1","order":"3"}'>
		<div v-if="false" class="idea newsIdea" :style='{"padding":"20px","flexWrap":"wrap","background":"#efefef","justifyContent":"space-between","display":"flex"}'>
			<div class="box1" :style='{"width":"20%","background":"#fff","height":"80px"}'></div>
			<div class="box2" :style='{"width":"20%","background":"#fff","height":"80px"}'></div>
			<div class="box3" :style='{"width":"20%","background":"#fff","height":"80px"}'></div>
			<div class="box4" :style='{"width":"20%","background":"#fff","height":"80px"}'></div>
			<div class="box5" :style='{"width":"20%","background":"#fff","display":"none","height":"80px"}'></div>
			<div class="box6" :style='{"width":"20%","background":"#fff","display":"none","height":"80px"}'></div>
			<div class="box7" :style='{"width":"20%","background":"#fff","display":"none","height":"80px"}'></div>
			<div class="box8" :style='{"width":"20%","background":"#fff","display":"none","height":"80px"}'></div>
			<div class="box9" :style='{"width":"20%","background":"#fff","display":"none","height":"80px"}'></div>
			<div class="box10" :style='{"width":"20%","background":"#fff","display":"none","height":"80px"}'></div>
		</div>
		
		<div class="title" :style='{"width":"100%","margin":"40px auto","lineHeight":"50px","textAlign":"center","background":"url(http://codegen.caihongy.cn/20230915/b96d1e15768f4ac495e60a79e04cb731.png) no-repeat center top"}'>
			<span :style='{"color":"#F5BB00","fontSize":"32px","lineHeight":"40px"}'>公告信息</span>
		</div>
		
			
			
			
			
			
			
			
			
			
			
		









		<div v-if="newsList.length" class="list list22 index-pv1" :style='{"width":"100%","padding":"10px 07%","fontSize":"14px","height":"auto"}'>
		  <div :style='{"width":"100%","color":"#fff","flexWrap":"wrap","justifyContent":"space-between","display":"flex","height":"auto"}'>
			<template v-for="(item,index) in newsList">
			<div v-if="index < 3" class="list-item animation-box" :style='{"cursor":"pointer","width":"31%","position":"relative","height":"auto"}' @click="toDetail('newsDetail', newsList[index*5])">
		      <img :style='{"width":"100%","objectFit":"cover","display":"block","height":"300px"}' :src="baseUrl + item.picture" alt="" />
			  <div :style='{"width":"100%","padding":"0 0 6px","position":"absolute","left":"0","bottom":"0","background":"rgba(0,0,0,.3)"}'>
		        <div :style='{"padding":"0 10px","overflow":"hidden","whiteSpace":"nowrap","color":"#fff","width":"100%","lineHeight":"44px","fontSize":"16px","textOverflow":"ellipsis"}' class="title">{{item.title}}</div>
		        <div :style='{"padding":"0 10px"}'>
		          <span class="icon iconfont icon-shijian21" :style='{"margin":"0 2px 0 0","lineHeight":"1.5","fontSize":"inherit","color":"inherit"}'></span>
		          <span :style='{"color":"inherit","lineHeight":"1.5","fontSize":"inherit"}'>{{item.addtime}}</span>
		        </div>
		        <div :style='{"padding":"0 10px","display":"inline-block"}'>
		          <span class="icon iconfont icon-geren16" :style='{"margin":"0 2px 0 0","lineHeight":"1.5","fontSize":"inherit","color":"inherit"}'></span>
		          <span :style='{"color":"inherit","lineHeight":"1.5","fontSize":"inherit"}'>{{item.name}}</span>
		        </div>
		        <div :style='{"padding":"0 10px","display":"inline-block"}'>
		          <span class="icon iconfont icon-zan10" :style='{"margin":"0 2px 0 0","lineHeight":"1.5","fontSize":"inherit","color":"inherit"}'></span>
		          <span :style='{"color":"inherit","lineHeight":"1.5","fontSize":"inherit"}'>{{item.thumbsupnum}}</span>
		        </div>
		        <div :style='{"padding":"0 10px","display":"inline-block"}'>
		          <span class="icon iconfont icon-shoucang10" :style='{"margin":"0 2px 0 0","lineHeight":"1.5","fontSize":"inherit","color":"inherit"}'></span>
		          <span :style='{"color":"inherit","lineHeight":"1.5","fontSize":"inherit"}'>{{item.storeupnum}}</span>
		        </div>
		        <div :style='{"padding":"0 10px","display":"inline-block"}'>
		          <span class="icon iconfont icon-chakan9" :style='{"margin":"0 2px 0 0","lineHeight":"1.5","fontSize":"inherit","color":"inherit"}'></span>
		          <span :style='{"color":"inherit","lineHeight":"1.5","fontSize":"inherit"}'>{{item.clicknum}}</span>
		        </div>
		      </div>
		    </div>
			</template>
		  </div>
		  <div :style='{"width":"100%","color":"#999","flexWrap":"wrap","justifyContent":"space-between","display":"flex","height":"auto"}'>
			<template v-for="(item,index) in newsList">
			<div v-if="index > 2" class="list-item animation-box" :style='{"cursor":"pointer","width":"31%","margin":"20px 0 0 0","display":"flex","height":"auto"}' @click="toDetail('newsDetail', item)">
		      <img :style='{"width":"150px","objectFit":"cover","display":"block","height":"130px"}' :src="baseUrl + item.picture" alt="" />
		  			  <div :style='{"padding":"10px","overflow":"hidden","flex":"1","height":"auto"}'>
		        <div :style='{"padding":"0 10px","lineHeight":"24px","fontSize":"14px","color":"#333","fontWeight":"600","height":"48px"}' class="title">{{item.title}}</div>
		        <div :style='{"padding":"0 10px","margin":"0 0 10px"}'>
		          <span class="icon iconfont icon-shijian21" :style='{"margin":"0 2px 0 0","lineHeight":"1.5","fontSize":"inherit","color":"inherit"}'></span>
		          <span :style='{"color":"inherit","lineHeight":"24px","fontSize":"inherit"}'>{{item.addtime}}</span>
		        </div>
		        <div :style='{"padding":"0 10px","display":"inline-block"}'>
		          <span class="icon iconfont icon-geren16" :style='{"margin":"0 2px 0 0","lineHeight":"1.5","fontSize":"inherit","color":"inherit"}'></span>
		          <span :style='{"color":"inherit","lineHeight":"1.5","fontSize":"inherit"}'>{{item.name}}</span>
		        </div>
		        <div :style='{"padding":"0 10px","display":"inline-block"}'>
		          <span class="icon iconfont icon-zan10" :style='{"margin":"0 2px 0 0","lineHeight":"1.5","fontSize":"inherit","color":"inherit"}'></span>
		          <span :style='{"color":"inherit","lineHeight":"1.5","fontSize":"inherit"}'>{{item.thumbsupnum}}</span>
		        </div>
		        <div :style='{"padding":"0 10px","display":"inline-block"}'>
		          <span class="icon iconfont icon-shoucang10" :style='{"margin":"0 2px 0 0","lineHeight":"1.5","fontSize":"inherit","color":"inherit"}'></span>
		          <span :style='{"color":"inherit","lineHeight":"1.5","fontSize":"inherit"}'>{{item.storeupnum}}</span>
		        </div>
		        <div :style='{"padding":"0 10px","display":"inline-block"}'>
		          <span class="icon iconfont icon-chakan9" :style='{"margin":"0 2px 0 0","lineHeight":"1.5","fontSize":"inherit","color":"inherit"}'></span>
		          <span :style='{"color":"inherit","lineHeight":"1.5","fontSize":"inherit"}'>{{item.clicknum}}</span>
		        </div>
		      </div>
		    </div>
			</template>
		  </div>
		</div>


		<div @click="moreBtn('news')" :style='{"border":"0","cursor":"pointer","margin":"40px auto","textAlign":"center","background":"#F5BB00","display":"block","width":"120px","lineHeight":"36px"}'>
			<span :style='{"color":"#f5f5f5","fontSize":"14px"}'>查看更多</span>
			<i :style='{"color":"#f5f5f5","fontSize":"12px"}' class="icon iconfont icon-gengduo1"></i>
		</div>
		
		</div>
	<!-- 新闻资讯 -->


<!-- 商品推荐 -->
<div id="animate_recommendshangpinxinxi" class="recommend animate__animated" :style='{"width":"100%","padding":"20px 0","margin":"0 0 20px","background":"#f1f1f1","order":"1"}'>
	<div v-if="false" class="idea recommendIdea" :style='{"padding":"20px","flexWrap":"wrap","background":"#efefef","justifyContent":"space-between","display":"flex"}'>
		<div class="box1" :style='{"width":"20%","background":"#fff","height":"80px"}'></div>
		<div class="box2" :style='{"width":"20%","background":"#fff","height":"80px"}'></div>
		<div class="box3" :style='{"width":"20%","background":"#fff","height":"80px"}'></div>
		<div class="box4" :style='{"width":"20%","background":"#fff","height":"80px"}'></div>
		<div class="box5" :style='{"width":"20%","background":"#fff","display":"none","height":"80px"}'></div>
		<div class="box6" :style='{"width":"20%","background":"#fff","display":"none","height":"80px"}'></div>
		<div class="box7" :style='{"width":"20%","background":"#fff","display":"none","height":"80px"}'></div>
		<div class="box8" :style='{"width":"20%","background":"#fff","display":"none","height":"80px"}'></div>
		<div class="box9" :style='{"width":"20%","background":"#fff","display":"none","height":"80px"}'></div>
		<div class="box10" :style='{"width":"20%","background":"#fff","display":"none","height":"80px"}'></div>
	</div>
	
    <div class="title" :style='{"width":"100%","margin":"30px auto","lineHeight":"50px","textAlign":"center","background":"url(http://codegen.caihongy.cn/20230915/b96d1e15768f4ac495e60a79e04cb731.png) no-repeat center top"}'>
		<span :style='{"color":"#F5BB00","fontSize":"32px","lineHeight":"40px"}'>商品信息推荐</span>
	</div>
	
	
	
	
	
	
	
	
	
	

	<div v-if="shangpinxinxiRecommend.length" class="list list10 index-pv1 list10shangpinxinxi" :style='{"width":"100%","padding":"0px 7%","background":"none","height":"auto"}'>
		<div class="tab" :style='{"width":"100%","margin":"30px 0 30px","justifyContent":"center","display":"flex","height":"auto"}'>
			<div class="item" :class="recommendIndex10shangpinxinxi == 0 ? 'active' : ''" @click="recommendIndexClick10(0, 'shangpinxinxi')">
				<!-- <img :style='{"width":"100%","margin":"10px 5px 0 0","objectFit":"cover","display":"block","height":"34px"}' src="http://codegen.caihongy.cn/20201114/7856ba26477849ea828f481fa2773a95.jpg"> -->
				<div :style='{"color":"inherit","fontSize":"14px"}'>全部</div>
			</div>
			<template v-for="(item,index) in recommendList10shangpinxinxi">
			<div v-if="index < 6" class="item" :class="recommendIndex10shangpinxinxi == index + 1 ? 'active' : ''" @click="recommendIndexClick10(index + 1, 'shangpinxinxi')">
				<img v-if="item.image" :style='{"width":"100%","margin":"10px 5px 0 0","objectFit":"cover","display":"block","height":"34px"}' :src="baseUrl + (item.image?item.image.split(',')[0]:'')">
				<div :style='{"color":"inherit","fontSize":"14px"}'>{{item[recommendColumn10shangpinxinxi]}}</div>
			</div>
			</template>
			<div class="more" @click="moreBtn('shangpinxinxi')">
			  <div :style='{"color":"inherit","fontSize":"14px"}'>更多</div>
			  <span class="icon iconfont icon-jiantou25" :style='{"color":"inherit","margin":"0 0 0 2px","fontSize":"14px"}'></span>
			</div>
		</div>
	  <div :style='{"width":"100%","background":"none","height":"600px"}'>
	    <div class="swiper-container recommendSwiper10 recommend-list-10shangpinxinxi">
	      <div class="swiper-wrapper">
	        <div class="swiper-slide" v-for="item,index in shangpinxinxiRecommend" :key="index">
	          <div class="list-item animation-box" :style='{"cursor":"pointer","width":"100%","position":"relative","background":"#fff","height":"auto"}' @click="toDetail('shangpinxinxiDetail', item)">
				<img :name="item.id" :style='{"width":"100%","objectFit":"cover","display":"block","height":"250px"}' v-if="preHttp(item.shangpintupian)" :src="item.shangpintupian.split(',')[0]" alt="" />
				<img :name="item.id" :style='{"width":"100%","objectFit":"cover","display":"block","height":"250px"}' v-else :src="baseUrl + (item.shangpintupian?item.shangpintupian.split(',')[0]:'')" alt="" />
				<div class="line1" :style='{"padding":"0 10px","lineHeight":"32px","fontSize":"16px","overflow":"hidden","color":"#333","height":"32px"}'>{{item.shangpinmingcheng}}</div>
				<div class="line1" :style='{"padding":"0 10px","lineHeight":"32px","fontSize":"16px","overflow":"hidden","color":"#333","height":"32px"}'>{{item.shangpinzhonglei}}</div>
				<div class="line1" :style='{"padding":"0 10px","lineHeight":"32px","fontSize":"16px","overflow":"hidden","color":"#333","height":"32px"}'>{{item.shangjiamingcheng}}</div>
	          </div>
	        </div>
	      </div>
	    </div>
	  </div>
	</div>






	
	<div @click="moreBtn('shangpinxinxi')" :style='{"border":"0","cursor":"pointer","margin":"20px auto","textAlign":"center","background":"#F5BB00","display":"block","width":"120px","lineHeight":"36px"}'>
		<span :style='{"color":"#f5f5f5","fontSize":"14px"}'>查看更多</span>
		<i :style='{"color":"#f5f5f5","fontSize":"12px"}' class="icon iconfont icon-gengduo1"></i>
	</div>
	
</div>
<!-- 商品推荐 -->


<!-- 特价商品 -->
<div id="animate_listshangjia" class="lists animate__animated" :style='{"margin":"0 0 20px","background":"#fff","order":"4"}'>
	<div v-if="false" class="idea" :style='{"padding":"20px","flexWrap":"wrap","background":"#efefef","justifyContent":"space-between","display":"flex"}'>
		<div class="box1" :style='{"width":"20%","background":"#fff","height":"80px"}'></div>
		<div class="box2" :style='{"width":"20%","background":"#fff","height":"80px"}'></div>
		<div class="box3" :style='{"width":"20%","background":"#fff","height":"80px"}'></div>
		<div class="box4" :style='{"width":"20%","background":"#fff","height":"80px"}'></div>
		<div class="box5" :style='{"width":"20%","background":"#fff","display":"none","height":"80px"}'></div>
		<div class="box6" :style='{"width":"20%","background":"#fff","display":"none","height":"80px"}'></div>
		<div class="box7" :style='{"width":"20%","background":"#fff","display":"none","height":"80px"}'></div>
		<div class="box8" :style='{"width":"20%","background":"#fff","display":"none","height":"80px"}'></div>
		<div class="box9" :style='{"width":"20%","background":"#fff","display":"none","height":"80px"}'></div>
		<div class="box10" :style='{"width":"20%","background":"#fff","display":"none","height":"80px"}'></div>
	</div>
	
	<div class="title" :style='{"width":"100%","margin":"30px auto","lineHeight":"50px","textAlign":"center","background":"url(http://codegen.caihongy.cn/20230915/b96d1e15768f4ac495e60a79e04cb731.png) no-repeat center top"}'>
	  <span :style='{"color":"#F5BB00","fontSize":"32px","lineHeight":"40px"}'>商家展示</span>
	</div>
	
	
	
	
	
	
	
	
	
	


	<div v-if="shangjiaList.length" class="list list11 index-pv1" :style='{"width":"100%","padding":"0 7%","background":"#fff","justifyContent":"space-between","display":"flex","height":"auto"}'>
	  <div class="list" :style='{"flexWrap":"wrap","flex":"1","background":"#fff","justifyContent":"space-between","display":"flex","height":"auto"}'>
	    <div :style='{"cursor":"pointer","width":"31%","margin":"0 0 20px","overflow":"hidden","position":"relative","height":"auto"}' class="item list-item animation-box" v-for="item,index in shangjiaList" :key="index" @click="toDetail('shangjiaDetail', item)">
			<img :name="item.id" :style='{"width":"100%","objectFit":"cover","display":"block","height":"200px"}' v-if="preHttp(item.shangpuzhaopian)" :src="item.shangpuzhaopian.split(',')[0]" alt="" />
			<img :name="item.id" :style='{"width":"100%","objectFit":"cover","display":"block","height":"200px"}' v-else :src="baseUrl + (item.shangpuzhaopian?item.shangpuzhaopian.split(',')[0]:'')" alt="" />
			<div class="line1" :style='{"padding":"0 10px","borderColor":"#ddd","overflow":"hidden","whiteSpace":"nowrap","color":"#333","borderWidth":"0 0 1px","width":"100%","lineHeight":"40px","fontSize":"16px","textOverflow":"ellipsis","borderStyle":"solid","height":"40px"}'>{{item.shangjiamingcheng}}</div>
	    </div>
	  </div>
	</div>




	
	
	<div @click="moreBtn('shangjia')" :style='{"border":"0","cursor":"pointer","margin":"30px auto 10px","textAlign":"center","background":"#F5BB00","display":"block","width":"120px","lineHeight":"36px"}'>
		<span :style='{"color":"#f5f5f5","fontSize":"14px"}'>查看更多</span>
		<i :style='{"color":"#f5f5f5","fontSize":"14px"}' class="icon iconfont icon-gengduo1"></i>
	</div>
	

</div>
<!-- 特价商品 -->

<!-- 特价商品 -->
<div id="animate_listshangpinxinxi" class="lists animate__animated" :style='{"margin":"0 0 20px","background":"#fff","order":"4"}'>
	<div v-if="false" class="idea" :style='{"padding":"20px","flexWrap":"wrap","background":"#efefef","justifyContent":"space-between","display":"flex"}'>
		<div class="box1" :style='{"width":"20%","background":"#fff","height":"80px"}'></div>
		<div class="box2" :style='{"width":"20%","background":"#fff","height":"80px"}'></div>
		<div class="box3" :style='{"width":"20%","background":"#fff","height":"80px"}'></div>
		<div class="box4" :style='{"width":"20%","background":"#fff","height":"80px"}'></div>
		<div class="box5" :style='{"width":"20%","background":"#fff","display":"none","height":"80px"}'></div>
		<div class="box6" :style='{"width":"20%","background":"#fff","display":"none","height":"80px"}'></div>
		<div class="box7" :style='{"width":"20%","background":"#fff","display":"none","height":"80px"}'></div>
		<div class="box8" :style='{"width":"20%","background":"#fff","display":"none","height":"80px"}'></div>
		<div class="box9" :style='{"width":"20%","background":"#fff","display":"none","height":"80px"}'></div>
		<div class="box10" :style='{"width":"20%","background":"#fff","display":"none","height":"80px"}'></div>
	</div>
	
	<div class="title" :style='{"width":"100%","margin":"30px auto","lineHeight":"50px","textAlign":"center","background":"url(http://codegen.caihongy.cn/20230915/b96d1e15768f4ac495e60a79e04cb731.png) no-repeat center top"}'>
	  <span :style='{"color":"#F5BB00","fontSize":"32px","lineHeight":"40px"}'>商品信息展示</span>
	</div>
	
	
	
	
	
	
	
	
	
	


	<div v-if="shangpinxinxiList.length" class="list list11 index-pv1" :style='{"width":"100%","padding":"0 7%","background":"#fff","justifyContent":"space-between","display":"flex","height":"auto"}'>
	  <div class="tab" :style='{"width":"260px","margin":"0 20px 0 0","flexDirection":"column","display":"flex","height":"auto"}'>
		<template v-for="item,index in listList11shangpinxinxi">
	    <div v-if="index < 6" :style='{"cursor":"pointer","padding":"4px 20px","margin":"0","borderColor":"#efefef","borderWidth":"0 0 1px 0","width":"100%","borderStyle":"solid","height":"auto"}' class="item" @click="listIndexClick11(item, 'shangpinxinxi')">
	      <span class="icon iconfont icon-jiantou34" :style='{"margin":"0 5px 0 0","lineHeight":"44px","fontSize":"16px","color":"#333"}'></span>
	      <img v-if="item.image" :style='{"width":"44px","margin":"0 5px 0 0","objectFit":"cover","borderRadius":"4px","display":"inline-block","height":"44px"}' :src="baseUrl + (item.image?item.image.split(',')[0]:'')">
		  <span :style='{"color":"#333","lineHeight":"44px","fontSize":"16px"}'>{{item[listColumn11shangpinxinxi]}}</span>
	    </div>
		</template>
		<div :style='{"cursor":"pointer","padding":"0 20px","margin":"0","borderColor":"#efefef","borderWidth":"0 0 1px 0","display":"none","width":"100%","borderStyle":"solid","height":"auto"}' class="more" @click="moreBtn('shangpinxinxi')">
		  <span class="icon iconfont icon-jiantou34" :style='{"margin":"0 5px 0 0","lineHeight":"44px","fontSize":"16px","color":"#999","display":"inline-block"}'></span>
		  <div :style='{"lineHeight":"44px","fontSize":"16px","color":"#999","display":"inline-block"}'>更多</div>
		</div>
	  </div>
	  <div class="list" :style='{"flexWrap":"wrap","flex":"1","background":"#fff","justifyContent":"space-between","display":"flex","height":"auto"}'>
	    <div :style='{"cursor":"pointer","width":"31%","margin":"0 0 20px","overflow":"hidden","position":"relative","height":"auto"}' class="item list-item animation-box" v-for="item,index in shangpinxinxiList" :key="index" @click="toDetail('shangpinxinxiDetail', item)">
			<img :name="item.id" :style='{"width":"100%","objectFit":"cover","display":"block","height":"200px"}' v-if="preHttp(item.shangpintupian)" :src="item.shangpintupian.split(',')[0]" alt="" />
			<img :name="item.id" :style='{"width":"100%","objectFit":"cover","display":"block","height":"200px"}' v-else :src="baseUrl + (item.shangpintupian?item.shangpintupian.split(',')[0]:'')" alt="" />
			<div class="line1" :style='{"padding":"0 10px","borderColor":"#ddd","overflow":"hidden","whiteSpace":"nowrap","color":"#333","borderWidth":"0 0 1px","width":"100%","lineHeight":"40px","fontSize":"16px","textOverflow":"ellipsis","borderStyle":"solid","height":"40px"}'>{{item.shangpinmingcheng}}</div>
			<div class="line1" :style='{"padding":"0 10px","borderColor":"#ddd","overflow":"hidden","whiteSpace":"nowrap","color":"#333","borderWidth":"0 0 1px","width":"100%","lineHeight":"40px","fontSize":"16px","textOverflow":"ellipsis","borderStyle":"solid","height":"40px"}'>{{item.shangpinzhonglei}}</div>
			<div class="line1" :style='{"padding":"0 10px","borderColor":"#ddd","overflow":"hidden","whiteSpace":"nowrap","color":"#333","borderWidth":"0 0 1px","width":"100%","lineHeight":"40px","fontSize":"16px","textOverflow":"ellipsis","borderStyle":"solid","height":"40px"}'>{{item.shangjiamingcheng}}</div>
	    </div>
	  </div>
	</div>




	
	
	<div @click="moreBtn('shangpinxinxi')" :style='{"border":"0","cursor":"pointer","margin":"30px auto 10px","textAlign":"center","background":"#F5BB00","display":"block","width":"120px","lineHeight":"36px"}'>
		<span :style='{"color":"#f5f5f5","fontSize":"14px"}'>查看更多</span>
		<i :style='{"color":"#f5f5f5","fontSize":"14px"}' class="icon iconfont icon-gengduo1"></i>
	</div>
	

</div>
<!-- 特价商品 -->
	
</div>
</template>

<script>
import 'animate.css'
import Swiper from "swiper";

  export default {
    //数据集合
    data() {
      return {
        baseUrl: '',
        newsList: [],
        shangpinxinxiRecommend: [],

        shangjiaList: [],
        shangpinxinxiList: [],


		recommendListSwiper10shangpinxinxi: null,
		recommendIndex10shangpinxinxi: 0,
		recommendList10shangpinxinxi: [],
		recommendColumn10shangpinxinxi: '',

		listIndex11shangpinxinxi: 0,
		listList11shangpinxinxi: [],
		listColumn11shangpinxinxi: '',

      }
    },
    created() {
		this.baseUrl = this.$config.baseUrl;
		this.getNewsList();
		this.getList();
		this.shangpinxinxiRecommendCate()
		this.shangpinxinxiListCate()
    },
	mounted() {
		window.addEventListener('scroll', this.handleScroll)
		setTimeout(()=>{
			this.handleScroll()
		},100)
		
		this.swiperChanges()
	},
	beforeDestroy() {
	  window.removeEventListener('scroll', this.handleScroll)
	},
    //方法集合
    methods: {
		swiperChanges() {














			if (this['recommendListSwiper10shangpinxinxi']) this['recommendListSwiper10shangpinxinxi'].destroy()






































			setTimeout(()=>{







				this['recommendListSwiper10shangpinxinxi'] = new Swiper(".recommend-list-10shangpinxinxi", {"freeMode":true,"slidesPerView":4,"slidesPerColumn":2,"spaceBetween":30})



















			},250)
		},
		shangpinxinxiRecommendCate(){
			this.$http.get('shangpinzhonglei/list',{}).then(res => {
			  if (res.data.code == 0) {
				this.recommendList10shangpinxinxi = res.data.data.list
			  }
			});
			this.recommendColumn10shangpinxinxi = 'shangpinzhonglei'
		},
		async recommendIndexClick10(index, name) {
			this['recommendIndex10' + name] = index
			await this.getList()
			this.swiperChanges()
		},

		shangpinxinxiListCate(){
			this.$http.get('shangpinzhonglei/list',{}).then(res => {
			  if (res.data.code == 0) {
				this.listList11shangpinxinxi = res.data.data.list
			  }
			});
			this.listColumn11shangpinxinxi = 'shangpinzhonglei'
		},
		listIndexClick11(index, name) {
			this['listIndex11' + name] = index[this['listColumn11' + name]]
			this.getList()
		},

		handleScroll() {
			let arr = [
				{id:'search',css:'animate__bounce'},
				{id:'about',css:'animate__fadeInUp'},
				{id:'system',css:'animate__fadeInUp'},
				{id:'animate_listshangjia',css:'animate__fadeInUp'},
				{id:'animate_recommendshangpinxinxi',css:'animate__fadeInUp'},
				{id:'animate_listshangpinxinxi',css:'animate__fadeInUp'},
				{id:'animate_newsnews',css:'animate__fadeInUp'},
				{id:'msgs',css:'animate__bounce'},
				{id:'friendly',css:'animate__bounce'}
			]
			
			for (let i in arr) {
				let doc = document.getElementById(arr[i].id)
				if (doc) {
					let top = doc.offsetTop
					let win_top = window.innerHeight + window.pageYOffset
					// console.log(top,win_top)
					if (win_top > top && doc.classList.value.indexOf(arr[i].css) < 0) {
						// console.log(doc)
						doc.classList.add(arr[i].css)
					}
				}
			}
		},
      preHttp(str) {
          return str && str.substr(0,4)=='http';
      },
		getNewsList() {
			let data = {
				page: 1,
				limit: 15,
                sort: 'addtime',
				order: 'desc'
			}
			this.$http.get('news/list', {params: data}).then(res => {
				if (res.data.code == 0) {
					this.newsList = res.data.data.list;
					
					
				}
			});
		},
		getList() {
			let autoSortUrl = "";
			let data = {}
          autoSortUrl = "shangpinxinxi/autoSort";
          if(localStorage.getItem('Token')) {
              autoSortUrl = "shangpinxinxi/autoSort2";
          }
			data = {
				page: 1,
				limit: 8,
			}
			if(this.recommendIndex10shangpinxinxi != 0){
				data.shangpinzhonglei = this.recommendList10shangpinxinxi[this.recommendIndex10shangpinxinxi - 1].shangpinzhonglei
			}
			this.$http.get(autoSortUrl, {params: data}).then(res => {
				if (res.data.code == 0) {
					this.shangpinxinxiRecommend = res.data.data.list;
					
					
					// 商品列表样式五
					
				}
			});
			
			data = {
				page: 1,
				limit: 6,
			}
			this.$http.get('shangjia/list', {params: data}).then(res => {
				if (res.data.code == 0) {
					this.shangjiaList = res.data.data.list;
					
					// 商品列表样式五
					
				}
			});
			data = {
				page: 1,
				limit: 6,
			}
			if(this.listIndex11shangpinxinxi){
				data.shangpinzhonglei = this.listIndex11shangpinxinxi
			}
			this.$http.get('shangpinxinxi/list', {params: data}).then(res => {
				if (res.data.code == 0) {
					this.shangpinxinxiList = res.data.data.list;
					
					// 商品列表样式五
					
				}
			});
		},
		toDetail(path, item) {
			this.$router.push({path: '/index/' + path, query: {id: item.id}});
		},
		moreBtn(path) {
			this.$router.push({path: '/index/' + path});
		}
    }
  }
</script>

<style rel="stylesheet/scss" lang="scss" scoped>
	.home-preview {
		// -------- search --------
		.search .select /deep/ .el-input__inner {
			border: 1px solid #ddd;
			border-radius: 4px;
			padding: 0 30px 0 10px;
			box-shadow: 0 0 0px rgba(64, 158, 255, .3);
			outline: none;
			color: rgba(64, 158, 255, 1);
			width: 180px;
			font-size: 14px;
			height: 36px;
		}
		
		.search .input /deep/ .el-input__inner {
			border: 1px solid #ddd;
			border-radius: 4px;
			padding: 0 10px;
			box-shadow: 0 0 0px rgba(64, 158, 255, .3);
			outline: none;
			color: rgba(64, 158, 255, 1);
			width: 180px;
			font-size: 14px;
			height: 36px;
		}
		// -------- search --------
		.recommend {
			.list3 .swiper-button-prev {
				left: 10px;
				right: auto;
			}
			
			.list3 .swiper-button-prev::after {
				color: rgb(64, 158, 255);
			}
			
			.list3 .swiper-button-next {
				left: auto;
				right: 10px;
			}
			
			.list3 .swiper-button-next::after {
				color: rgb(64, 158, 255);
			}
			
			.list5 .swiper-button-prev {
				left: 10px;
				right: auto;
			}
			
			.list5 .swiper-button-prev::after {
				color: rgb(64, 158, 255);
        }
        
        .list5 .swiper-button-next {
				left: auto;
				right: 10px;
			}
			
			.list5 .swiper-button-next::after {
				color: rgb(64, 158, 255);
			}
			
			.list5 {
				.swiper-slide-prev {
					position: relative;
					z-index: 3;
				}
		
				.swiper-slide-next {
					position: relative;
					z-index: 3;
				}
		
				.swiper-slide-active {
					position: relative;
					z-index: 5;
				}
			}
			
			.index-pv1 .animation-box {
				transform: rotate(0deg) scale(1) skew(0deg, 0deg) translate3d(0px, 0px, 0px);
				z-index: initial;
			}
			
			.index-pv1 .animation-box:hover {
				transform: rotate(0deg) scale(1) skew(0deg, 0deg) translate3d(0px, 10px, 0px);
				-webkit-perspective: 1000px;
				perspective: 1000px;
				transition: 0.3s;
				z-index: 1;
			}
			
			.index-pv1 .animation-box img {
				transform: rotate(0deg) scale(1) skew(0deg, 0deg) translate3d(0px, 0px, 0px);
			}
			
			.index-pv1 .animation-box img:hover {
				transform: rotate(0deg) scale(1.02) skew(0deg, 0deg) translate3d(0px, 0px, 0px);
				-webkit-perspective: 1000px;
				perspective: 1000px;
				transition: 0.3s;
			}
		}
		
		.news {
			.list3 .swiper-button-prev {
				left: 10px;
				right: auto;
			}
			
			.list3 .swiper-button-prev::after {
				color: rgb(64, 158, 255);
			}
			
			.list3 .swiper-button-next {
				left: auto;
				right: 10px;
			}
			
			.list3 .swiper-button-next::after {
				color: rgb(64, 158, 255);
			}
			
			.list6 .swiper-button-prev {
				left: 10px;
				right: auto;
			}
			
			.list6 .swiper-button-prev::after {
				color: rgb(64, 158, 255);
			}
			
			.list6 .swiper-button-next {
				left: auto;
				right: 10px;
			}
			
			.list6 .swiper-button-next::after {
				color: rgb(64, 158, 255);
			}
			
			.index-pv1 .animation-box {
				transform: rotate(0deg) scale(1) skew(0deg, 0deg) translate3d(0px, 0px, 0px);
				z-index: initial;
			}
			
			.index-pv1 .animation-box:hover {
				transform: rotate(0deg) scale(1) skew(0deg, 0deg) translate3d(0px, 0px, 0px);
				-webkit-perspective: 1000px;
				perspective: 1000px;
				transition: 0.3s;
				z-index: 1;
			}
			
			.index-pv1 .animation-box img {
				transform: rotate(0deg) scale(1) skew(0deg, 0deg) translate3d(0px, 0px, 0px);
			}
			
			.index-pv1 .animation-box img:hover {
				transform: rotate(0deg) scale(1) skew(0deg, 0deg) translate3d(0px, 0px, 0px);
				-webkit-perspective: 1000px;
				perspective: 1000px;
				transition: 0.3s;
			}
		}
	
		.lists {
			.list3 .swiper-button-prev {
				left: 10px;
				right: auto;
			}
			
			.list3 .swiper-button-prev::after {
				color: rgb(64, 158, 255);
			}
			
			.list3 .swiper-button-next {
				left: auto;
				right: 10px;
        }
        
        .list3 .swiper-button-next::after {
				color: rgb(64, 158, 255);
			}
			
			.list5 .swiper-button-prev {
				left: 10px;
				right: auto;
			}
			
			.list5 .swiper-button-prev::after {
				color: rgb(64, 158, 255);
			}
			
			.list5 .swiper-button-next {
            left: auto;
            right: 10px;
			}
			
			.list5 .swiper-button-next::after {
				color: rgb(64, 158, 255);
			}
			
			.list5 {
				.swiper-slide-prev {
					position: relative;
					z-index: 3;
				}
		
				.swiper-slide-next {
					position: relative;
					z-index: 3;
				}
		
				.swiper-slide-active {
					position: relative;
					z-index: 5;
				}
			}
			
			.index-pv1 .animation-box {
				transform: rotate(0deg) scale(1) skew(0deg, 0deg) translate3d(0px, 0px, 0px);
				z-index: initial;
			}
			
			.index-pv1 .animation-box:hover {
				transform: rotate(0deg) scale(1) skew(0deg, 0deg) translate3d(0px, 10px, 0px);
				-webkit-perspective: 1000px;
				perspective: 1000px;
				transition: 0.3s;
				z-index: 1;
			}
			
			.index-pv1 .animation-box img {
				transform: rotate(0deg) scale(1) skew(0deg, 0deg) translate3d(0px, 0px, 0px);
			}
			
			.index-pv1 .animation-box img:hover {
				transform: rotate(0deg) scale(1.1) skew(0deg, 0deg) translate3d(0px, 0px, 0px);
				-webkit-perspective: 1000px;
				perspective: 1000px;
				transition: 0.3s;
			}
		}
	}
	






	.home-preview .recommend .list10 .swiper-container {
	    width: 100%;
	    height: 100%;
	    margin-left: auto;
	    margin-right: auto;
	}
	
	.home-preview .recommend .list10 .swiper-slide {
	    text-align: center;
	    height: calc((100% - 30px) / 2);
	
	    /* Center slide text vertically */
	    display: -webkit-box;
	    display: -ms-flexbox;
	    display: -webkit-flex;
	    display: flex;
	    -webkit-box-pack: center;
	    -ms-flex-pack: center;
	    -webkit-justify-content: center;
	    justify-content: center;
	    -webkit-box-align: center;
	    -ms-flex-align: center;
	    -webkit-align-items: center;
	    align-items: center;
	}
	
	.home-preview .recommend .list10 .tab .item {
				cursor: pointer;
				border: 0px solid #ddd;
				border-radius: 0px;
				padding: 0 20px;
				margin: 0 10px;
				color: #fff;
				background: #333;
				width: auto;
				font-size: 16px;
				line-height: 44px;
			}
	
	.home-preview .recommend .list10 .tab .item:hover {
				border: 0px solid #F5BB00;
				color: #fff;
				background: #F5BB00;
			}
	
	.home-preview .recommend .list10 .tab .item.active {
				border: 0px solid #F5BB00;
				color: #fff;
				background: #F5BB00;
			}
	
	.home-preview .recommend .list10 .tab .more {
				cursor: pointer;
				border-radius: 0px;
				padding: 0px 20px;
				margin: 0 10px;
				color: #fff;
				background: #333;
				display: none;
				line-height: 44px;
				align-items: center;
			}
	
	.home-preview .recommend .list10 .tab .more:hover {
				background: #F5BB00;
			}




</style>
