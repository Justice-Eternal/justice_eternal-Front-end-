<template>
    <div class="container1">
	   	<div class="music">
	   		<h1 class="music-title">音乐专区</h1>
	        <div id="player5" class="aplayer" ref="ap5"></div>
	        <div class="author"><a href="http://http://5sing.kugou.com/34713615/default.html">♡ 流萤川小时 ♡</a></div>
	        <div id="player1" class="aplayer" ref="ap1"></div>
	        <div class="author"><a href="http://5sing.kugou.com/3811857/fc/5.html">♡ 自由姐 ♡</a></div>    
	        <div id="player2" class="aplayer" ref="ap2"></div>
	        <div class="author"><a href="http://5sing.kugou.com/nyarin/lastupdate.html">♡ 猫燐kirin03 ♡</a></div>
	        <div id="player3" class="aplayer" ref="ap3"></div>
	        <div class="author"><a href="http://5sing.kugou.com/10590245/default.html###">♡ 月光银百合 ♡</a></div>
	        <div id="player4" class="aplayer" ref="ap4"></div>
	        <div class="author"><a href="http://music.163.com/#/artist?id=1077060">♡ 翎渡 ♡</a></div>
	    </div>

	   	<div class="tutorial">
	   		<h1 class="tutorial-title">教学专区</h1>

	        <div class="gridlist-container">
	            <Card class="gridlist" v-for="item in recommondList1" key="item.aid">
	              <img :src="item.pic" @click="playDetail1(item.id)" class="tutorial-img" />
	              <span slot="title" class="gridlist-title" @click="playDetail1(item.id)">{{item.title}}</span>
	              <span slot="extra">by <b>{{item.author}}</b></span>
	            </Card>
	        </div>
		</div>

	   	<div class="newyear">
	   		<h1 class="newyear-title">JE吧拜年祭</h1>
	   		<img class="newyear-img" src="@/assets/bnj.jpg" >

<!-- 	        <div class="gridlist-container">
	            <Card class="gridlist" v-for="item in recommondList1" key="item.aid">
	              <img :src="item.pic" @click="playDetail1(item.id)" class="tutorial-img" />
	              <span slot="title" class="gridlist-title" @click="playDetail1(item.id)">{{item.title}}</span>
	              <span slot="extra">by <b>{{item.author}}</b></span>
	            </Card>
	        </div> -->
		</div>

    </div>
</template>

<script>
import APlayer from 'aplayer'
export default {
    data () {
      return {
				"recommondList1": [
				            {
				            
				                "id": 1000001,
				                "typename": "排骨大大",
				                "title": "八度和音入门与浅谈",
				                "author": "sqrsqr32",
				                "description": "",
				                "pic": "http://upload-images.jianshu.io/upload_images/2141706-864e45115c886b37.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240",
				                "src": "http://otr48sjv5.bkt.clouddn.com/%E5%85%AB%E5%BA%A6%E5%92%8C%E9%9F%B3%E5%85%A5%E9%97%A8%E4%B8%8E%E6%B5%85%E8%B0%88.mp4"
				            },
				            {
				            
				                "id": 1000002,
				                "typename": "排骨大大",
				                "title": "颤音，震音",
				                "author": "sqrsqr32",
				                "description": "",
				                "pic": "http://upload-images.jianshu.io/upload_images/2141706-b829195f5ccbf574.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240",
				                "src": "http://otr48sjv5.bkt.clouddn.com/%E9%A2%A4%E9%9F%B3%EF%BC%8C%E9%9C%87%E9%9F%B3.mp4"
				            },
				            {
				            
				                "id": 1000003,
				                "typename": "排骨大大",
				                "title": "断奏",
				                "author": "sqrsqr32",
				                "description": "",
				                "pic": "http://upload-images.jianshu.io/upload_images/2141706-693930646f308805.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240",
				                "src": "http://otr48sjv5.bkt.clouddn.com/%E6%96%AD%E5%A5%8F.mp4"
				            },
				            {
				            
				                "id": 1000004,
				                "typename": "排骨大大",
				                "title": "花舌",
				                "author": "sqrsqr32",
				                "description": "",
				                "pic": "http://upload-images.jianshu.io/upload_images/2141706-de120b8f12fdec7e.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240",
				                "src": "http://otr48sjv5.bkt.clouddn.com/%E8%8A%B1%E8%88%8C.mp4"
				            },
				            {
				            
				                "id": 1000005,
				                "typename": "排骨大大",
				                "title": "快速演奏入门和概述",
				                "author": "sqrsqr32",
				                "description": "",
				                "pic": "http://upload-images.jianshu.io/upload_images/2141706-abfad72355b9cd53.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240",
				                "src": "http://otr48sjv5.bkt.clouddn.com/%E5%BF%AB%E9%80%9F%E6%BC%94%E5%A5%8F%E5%85%A5%E9%97%A8%E5%92%8C%E6%A6%82%E8%BF%B0.mp4"
				            },
				            {
				            
				                "id": 1000006,
				                "typename": "排骨大大",
				                "title": "移琴，推键",
				                "author": "sqrsqr32",
				                "description": "",
				                "pic": "http://upload-images.jianshu.io/upload_images/2141706-b9b5c98e412b388c.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240",
				                "src": "http://otr48sjv5.bkt.clouddn.com/%E7%A7%BB%E7%90%B4%EF%BC%8C%E6%8E%A8%E9%94%AE.mp4"
				            }
				            
				    ]
      }
    },
    components: {
    },
    mounted () {
            var ap1 = new APlayer({
        element: player1,
        narrow: false,
        autoplay: false,
        showlrc: false,
        mutex: true,
        theme: '#2d8cf0',
        mode: 'random',
        music: [
            {
                title: '数码宝贝 Brave heart',
                author: 'FREEDOM54',
                url: 'http://link1.5sing.kugou.com/35037559/ApQEAFX0UvqIJm1oAA_ePaYfYPUAABmVgKCjqAAD95V687.mp3',
                pic: 'http://wsing.bssdl.kugou.com/8f9355c1bfe1ad2e627b8114b77169af.png_180x180.png'
            },
            {
                title: '星之所在',
                author: 'FREEDOM54',
                url: 'http://link1.5sing.kugou.com/35037559/Yg0DAFXt30eAGeqCABHLdZiBmeU375.mp3',
                pic: 'http://wsing.bssdl.kugou.com/8f9355c1bfe1ad2e627b8114b77169af.png_180x180.png'
            },
            {
                title: '花名未闻 ED secret base 君がくれたもの',
                author: 'FREEDOM54',
                url: 'http://link1.5sing.kugou.com/35037559/_5MEAFX3bKSAQU2SABYZmeNGqtM935.mp3',
                pic: 'http://wsing.bssdl.kugou.com/8f9355c1bfe1ad2e627b8114b77169af.png_180x180.png'
            },
            {
                title: '火影忍者 萤之光',
                author: 'FREEDOM54',
                url: 'http://link1.5sing.kugou.com/35037559/BJQEAFXz1uSIGw0nAA9MSuYCzZ8AAAKKwNk2h8AD0xi465.mp3',
                pic: 'http://wsing.bssdl.kugou.com/8f9355c1bfe1ad2e627b8114b77169af.png_180x180.png'
            }
        ]
      });
      var ap2 = new APlayer({
        element: player2,
        narrow: false,
        autoplay: false,
        showlrc: false,
        mutex: true,
        theme: '#2d8cf0',
        mode: 'random',
        music: [
            {
                title: 'ハイドアンド シーク Hide And Seek ',
                author: '猫燐kirin03',
                url: 'http://link1.5sing.kugou.com/35037559/ApQEAFXsZJeAYIcnABCpWsBgz5c804.mp3',
                pic: 'http://wsing.bssdl.kugou.com/16171fa7eb52fb3036b0a6d876ae58dc.jpg_188x188.jpg'
            },
            {
                title: '告白予行練習',
                author: '猫燐kirin03',
                url: 'http://link1.5sing.kugou.com/35037559/eg0DAFbE4JaIVkdeAAoLb8D6eDsAAAIJwJIIYAACguH110.mp3',
                pic: 'http://wsing.bssdl.kugou.com/16171fa7eb52fb3036b0a6d876ae58dc.jpg_188x188.jpg'
            },
            {
                title: '血界战线ED Sugar Song to Bitter Step',
                author: '猫燐kirin03',
                url: 'http://link1.5sing.kugou.com/35037559/v4YBAFXn1q6IWHe0AAbzxADcV34AAA4fAGdr-EABvPc412.mp3',
                pic: 'http://wsing.bssdl.kugou.com/16171fa7eb52fb3036b0a6d876ae58dc.jpg_188x188.jpg'
            }
        ]
      });
      var ap3 = new APlayer({
        element: player3,
        narrow: false,
        autoplay: false,
        showlrc: false,
        mutex: true,
        theme: '#2d8cf0',
        mode: 'random',
        music: [
            {
                title: '六兆年と一夜物語',
                author: '月光银百合',
                url: 'http://link1.5sing.kugou.com/35037559/A5QEAFXmAtWIMhVAAA2nzIC0htgAAAy3AGUtvMADafk974.mp3',
                pic: 'http://wsing.bssdl.kugou.com/c66f82bdb5b49e9b88dcfe898407da93.jpg_188x188.jpg'
            },
            {
                title: '口袋妖怪 XY 天台 BGM',
                author: '月光银百合',
                url: 'http://link1.5sing.kugou.com/35037559/w4YBAFXngBWIThk7AAuvAcbmqGQAAA4yQLVjmoAC68Z330.mp3',
                pic: 'http://wsing.bssdl.kugou.com/c66f82bdb5b49e9b88dcfe898407da93.jpg_188x188.jpg'
            }
        ]
      });
      var ap4 = new APlayer({
        element: player4,
        narrow: false,
        autoplay: false,
        showlrc: false,
        mutex: true,
        theme: '#2d8cf0',
        mode: 'random',
        music: [
            {
                title: '爱尔兰画眉',
                author: '翎渡',
                url: 'http://otr48sjv5.bkt.clouddn.com/%E7%BF%8E%E6%B8%A1%20-%20%E7%88%B1%E5%B0%94%E5%85%B0%E7%94%BB%E7%9C%89.mp3',
                pic: 'http://p1.music.126.net/Cu_ikJw5uW7Ez7FfmI2aBQ==/7906588115606542.jpg?param=180y180'
            },
            {
                title: '野蜂飞舞',
                author: '翎渡',
                url: 'http://otr48sjv5.bkt.clouddn.com/%E7%BF%8E%E6%B8%A1%20-%20%E9%87%8E%E8%9C%82%E9%A3%9E%E8%88%9E%20%20-%20%E5%8D%8A%E9%9F%B3%E9%98%B6%E5%8F%A3%E7%90%B4.mp3',
                pic: 'http://p1.music.126.net/Cu_ikJw5uW7Ez7FfmI2aBQ==/7906588115606542.jpg?param=180y180'
            },
            {
                title: 'purple passion',
                author: '翎渡',
                url: 'http://otr48sjv5.bkt.clouddn.com/%E7%BF%8E%E6%B8%A1%20-%20purple%20passion%20%20-%20%E5%8D%8A%E9%9F%B3%E9%98%B6%E5%8F%A3%E7%90%B4.mp3',
                pic: 'http://p1.music.126.net/Cu_ikJw5uW7Ez7FfmI2aBQ==/7906588115606542.jpg?param=180y180'
            }
        ]
      });
      var ap5 = new APlayer({
        element: player5,
        narrow: false,
        autoplay: false,
        showlrc: false,
        mutex: true,
        theme: '#2d8cf0',
        mode: 'random',
        music: [
            {
                title: 'letter song.cover',
                author: '流萤川小时',
                url: 'http://otr48sjv5.bkt.clouddn.com/%E6%B5%81%E8%90%A4%E5%B7%9D%E5%B0%8F%E6%97%B6-letter%20song.mp3',
                pic: 'http://wsing.bssdl.kugou.com/35e35d257b628b4735e76f24bc6177ec.jpg_188x188.jpg'
            },
            {
                title: '四月は君の嘘-私の嘘',
                author: '流萤川小时',
                url: 'http://otr48sjv5.bkt.clouddn.com/%E6%B5%81%E8%90%A4%E5%B7%9D%E5%B0%8F%E6%97%B6-%E5%9B%9B%E6%9C%88%E3%81%AF%E5%90%9B%E3%81%AE%E5%98%98-%E7%A7%81%E3%81%AE%E5%98%98.mp3',
                pic: 'http://wsing.bssdl.kugou.com/35e35d257b628b4735e76f24bc6177ec.jpg_188x188.jpg'
            },
            {
                title: '远い空へ',
                author: '流萤川小时',
                url: 'http://otr48sjv5.bkt.clouddn.com/%E6%B5%81%E8%90%A4%E5%B7%9D%E5%B0%8F%E6%97%B6-%E8%BF%9C%E3%81%84%E7%A9%BA%E3%81%B8.mp3',
                pic: 'http://wsing.bssdl.kugou.com/35e35d257b628b4735e76f24bc6177ec.jpg_188x188.jpg'
            }
        ]
      })
    },
    methods: {
        playDetail1(id) {
            this.$router.push(
                 {name: 'play', params: {'videoId': id}}
             )
        }
    },
    created () {

      this.$store.state.video.recommondList1 = this.recommondList1
    
    }
}
</script>


<style scoped>
.container1 {
  width: 960px;
  margin-left: auto;
  margin-right: auto;
}

.author{
	text-align: center;
	font-size: 18px;
}

.music-title{
	margin-bottom: 20px;
}

.tutorial-title{
	margin: 40px 0px;
}
.gridlist-container{
    flex-direction: row;
}

.gridlist{
	display: inline-block;

	width: 460px;
	height: 300px;
	margin: 10px 10px;

}
.tutorial-img{
	/*height: 100%;*/
	padding: 0;
	margin: 0; 
	width: 100%;
	height: 230px;

}

.gridlist-title{
	font-size: 18px;
	font-weight: bold;
}

.newyear{
	margin: 80px 0;

}

.newyear-title{
	text-align: center;
	color: red;
}

.newyear-img{
	margin-top: 20px;
	margin-left: 80px;
}
</style>
