<template>
  <div>
    1、autoscroll实现的一种幻彩效果
    <auto-scroll width="70px" height="8px" dir="horizontal" :step-speed="100">
      <div class="demo1 demo11"></div>
      <div class="demo1 demo12"></div>
      <div class="demo1 demo13"></div>
      <div class="demo1 demo14"></div>
      <div class="demo1 demo15"></div>
      <div class="demo1 demo16"></div>
      <div class="demo1 demo17"></div>
    </auto-scroll>
    <br /><br />
    2、比较常见的：滚动的广告、通知、新闻、警示语等等<br />
    <div class="demo2">
     <auto-scroll dir="horizontal" :step-speed="1000">
        <div class="demo2-item" v-for="(item,index) in data2" :key="index">{{index+1}}、{{item}}&nbsp;&nbsp;&nbsp;</div>
      </auto-scroll>
    </div>
    <br /><br />
    3、数据大屏滚动展示，很常见，比如医院叫号<br />
     <div class="demo3">
       <auto-scroll :step-speed="8000">
         <div class="demo3-item" v-for="(item,index) in data3" :key="index">
           <div class="demo3-item-cell">{{item.code}}</div>
           <div class="demo3-item-cell">{{item.name}}</div>
           <div class="demo3-item-cell">{{item.room}}</div>
         </div>
         <div class="demo3-item" v-if="(data3.length%2!==0)"><div class="demo3-item-cell"></div></div>
       </auto-scroll>
     </div>
  </div>
</template>

<script>
import AutoScroll from 'yhh-autoscroll-vue2'
export default {
	components:{AutoScroll},
	data() {
		return {
			data2:[
				'这是一条广告信息',
				'这是一条通知',
				'这是一条新闻简要',
				'这是一句警示语'
			],
			data3:[
				{code:'普内1001',name:'张*三',room:'A001'},
				{code:'普内1002',name:'李*四',room:'A003'},
				{code:'普内1003',name:'黄*',room:'A002'},
				{code:'普内1004',name:'牛*彩',room:'A005'},
				{code:'普内1005',name:'牛*',room:'A004'},
				{code:'普内1006',name:'刘*茂',room:'A001'},
				{code:'普内1007',name:'庄*艳',room:'A003'},
				{code:'普内1008',name:'上*虹',room:'A005'},
				{code:'普内1009',name:'花*曼',room:'A002'},
				{code:'普内1010',name:'夏*',room:'等候'},
				{code:'普内1011',name:'戚*根',room:'等候'},
				{code:'普内1012',name:'尚*亮',room:'等候'},
				{code:'普内1013',name:'柳*',room:'等候'},
				{code:'普内1014',name:'宋*来',room:'等候'},
				{code:'普内1015',name:'卫*国',room:'等候'}
			]
		}
	}
}
</script>

<style lang="scss">
.demo1{
  height: 100%;
  width: 20px;
  &.demo11{
    background-color: #ff0000;
  }
  &.demo12{
    background-color: #ffa500;
  }
  &.demo13{
    background-color: #ffff00;
  }
  &.demo14{
    background-color: #00ff00;
  }
  &.demo15{
    background-color: #b0e0e6;
  }
  &.demo16{
    background-color: #0000ff;
  }
  &.demo17{
    background-color: #800080;
  }

}

.demo2{
  height: 30px;
  color:#ffa500;
  width: 200px;
  .demo2-item{
    height: 100%;
    line-height: 30px;
  }
}

.demo3 {
  width: 330px;
  height: 300px;
  border-style: solid;
  border-width: 3px 0 3px 0;
  border-color: #c0c0c0;
  .demo3-item{
    display: flex;
    width: 100%;
    &:nth-child(odd){
      background-color: #dcdcdc;
    }
    .demo3-item-cell{
      height: 30px;
      line-height: 30px;
      width: 1px;
      flex: 1;
    }
  }
}
</style>
