<template>
<div class="all">
  <div class="box">
    <div class="p1head">
        <div class="p1headtop">
            <span class="p1headtop_span_line"></span>
            <span class="p1headtop_span">百丽运动·大算</span>
        </div>
        <div class="p1headdown">
            {{homedata.store_name}} &nbsp&nbsp {{homedata.time_year}}年第{{homedata.week_no}}周({{homedata.time_day}})     
        </div>
    </div>
    <div class="p1middle">
        <div class="p1middle_top">店长{{homedata.report_type}}分析报告</div>
        <div class="p1middle_middle">
          {{homedata.store_name}} <br/>
          门店固话:{{homedata.store_tel}} <br/>
          门店类型:{{homedata.store_type}} <br/>
          门店等级:{{homedata.store_level}} <br/>
          <br/>
          店长姓名:{{homedata.stuff_name}} &nbsp  主管名称:{{homedata.director_name}} <br/>
          联系电话:{{homedata.stuff_phone}} <br/>
          电子邮箱:{{homedata.stuff_email}}
        </div>
        <div class="p1middle_down">
           本文的任何部分不得以任何形式或任何方式复制 <br/>
           或传播，包括复印和录制，或任何信息存储和检索系统。<br/>
           最终解释权归本店所有。<br/>
           <br/>
           更新时间:{{homedata.time_update}}
        </div>
    </div>  
  </div>

  <div class="box p01">
      <div class="boxhead">店长{{homedata.report_type}}分析报告</div>

      <div class="p01head">
          <span class="p01head_top">目录</span> <br/>
          <span class="p01head_down">Contents</span>
      </div>
      <div class="p01middle">
           <div class="p01middle_div">
             <span class="p01_number">01</span> &nbsp &nbsp
             <span class="p01_content">销售</span>
           </div>
           <div class="p01middle_div">
             <span class="p01_number">02</span> &nbsp &nbsp
             <span class="p01_content">品类分析</span>
           </div>
            <div class="p01middle_div">
             <span class="p01_number">03</span> &nbsp &nbsp
             <span class="p01_content">单品分析</span>
           </div>
            <div class="p01middle_div p01middle_div_down">
             <span class="p01_number">04</span> &nbsp &nbsp
             <span class="p01_content">店员分析</span>
           </div>
      </div>

      <div class="boxtail">
      {{homedata.store_name}}·{{homedata.time_year}}年第{{homedata.week_no}}周
      | <span class="boxtail_span">01</span>
      </div>
  </div>

  <div class="box p02">
    <div class="boxhead">店长{{homedata.report_type}}分析报告</div>
    <div class="zititle_left"></div>
    <div class="zititle">销售</div>

    <div id="1_1" class="sale01"></div>
    <div id="1_2" class="sale02"></div>
    <div id="1_3" class="sale03"></div>

    <div class="boxtail">
    {{homedata.store_name}}·{{homedata.time_year}}年第{{homedata.week_no}}周
    | <span class="boxtail_span">02</span>
    </div>
  </div>

  <div class="box p03">
    <div class="boxhead">店长{{homedata.report_type}}分析报告</div>
    
    <div class="boxtail">
    {{homedata.store_name}}·{{homedata.time_year}}年第{{homedata.week_no}}周
    | <span class="boxtail_span">03</span>
    </div>
  </div>

  <!-- 品类分析 -->
  <div class="box p04">
    <div class="boxhead">店长{{homedata.report_type}}分析报告</div>
    <div class="zititle_left"></div>
    <div class="zititle">品类分析</div>
    <div class="zititle2">2-1. 大类分析</div>

    <div class="p04_pinpai_logo"></div>
    <div class="p04_pinpai">销存占比-品牌季节</div>
    <div id="2_1_1" class="p04_brand01"></div>
    <div class="p04_zhongxian"></div>
    <div class="p04_table1_head1">
      <div class="p04_table1_dalei">大类</div>
      <div class="p04_table1_xie">鞋</div>
      <div class="p04_table1_fu">服</div>
      <div class="p04_table1_xie">配</div>
      <div class="p04_table1_heji">合计</div>
    </div>
    <table class="p04_table1">
      <tr>
        <th class="th01">占比</th>
        <th class="th02">销售</th>
        <th class="th02">库存</th>
        <th class="th02">销售</th>
        <th class="th05">库存</th>
        <th class="th02">销售</th>
        <th class="th05">库存</th>
        <th class="th02">销售</th>
        <th class="th07">库存</th>
      </tr>
      <tr v-for="item in seasondata2_1.biaoge2_1_0">
        <td  class="th01" style="background:#1c4a82;color:white;font-size:12px">{{item.brand_season}}</td>
        <td>{{item.sale_amount_01}}</td>
        <td>{{item.inventory_amount_01}}</td>
        <td>{{item.sale_amount_02}}</td>
        <td>{{item.inventory_amount_02}}</td>
        <td>{{item.sale_amount_03}}</td>
        <td>{{item.inventory_amount_03}}</td>
        <td>{{item.sale_amount_04}}</td>
        <td>{{item.inventory_amount_04}}</td>
      </tr>
    </table>


    <div class="p04_pinpai_logo_sex"></div>
    <div class="p04_pinpai_sex">销存占比-性别</div>
    <div id="2_1_2" class="p04_brand02"></div>
    <div class="p04_zhongxian2"></div>
    <div class="p04_table1_head2">
      <div class="p04_table1_dalei">大类</div>
      <div class="p04_table1_xie">鞋</div>
      <div class="p04_table1_fu">服</div>
      <div class="p04_table1_xie">配</div>
    </div>
    <table class="p04_table2">
      <tr>
        <th class="th01">占比</th>
        <th class="th02">销售</th>
        <th class="th02">库存</th>
        <th class="th02">销售</th>
        <th class="th05">库存</th>
        <th class="th02">销售</th>
        <th class="th07">库存</th>
      </tr>
      <tr v-for="item in seasondata2_1.biaoge2_1_1">
        <td class="th01" style="background:#1c4a82;color:white;font-size:12px">{{item.brand_season}}</td>
        <td>{{item.sale_amount_01}}</td>
        <td>{{item.inventory_amount_01}}</td>
        <td>{{item.sale_amount_02}}</td>
        <td>{{item.inventory_amount_02}}</td>
        <td>{{item.sale_amount_03}}</td>
        <td>{{item.inventory_amount_03}}</td>
      </tr>
    </table>



    <div class="boxtail">
    {{homedata.store_name}}·{{homedata.time_year}}年第{{homedata.week_no}}周
    | <span class="boxtail_span">04</span>
    </div>
  </div>

  <div class="box p05">
    <div class="boxhead">店长{{homedata.report_type}}分析报告</div>
    
    

    <div class="boxtail">
    {{homedata.store_name}}·{{homedata.time_year}}年第{{homedata.week_no}}周
    | <span class="boxtail_span">05</span>
    </div>
  </div>

  <div class="box p06">
    <div class="boxhead">店长{{homedata.report_type}}分析报告</div>
    
    <table class="p06_table" id="p06_table">
      <tr>
         <th class="th01">大类</th>
         <th class="th02">性别</th>
         <th class="th03">系列</th>
         <th class="th04">折扣</th>
         <th class="th04">销售额</th>
         <th class="th04">库存额</th>
         <th class="th04">销售量</th>
         <th class="th04">库存量</th>
         <th class="th04">销售SKU</th>
         <th class="th04">库存SKU</th>
         <th class="th04">动销率</th>
         <th class="th04">销售占比</th>
         <th class="th04">库存占比</th>
      </tr>
      <tr v-for="item in shoestable2_2">
         <td>{{item.shoename}}</td>
         <td >{{item.category_name}}</td>
         <td>{{item.series_name}}</td>
         <td>{{item.sale_discount}}</td>
         <td>{{item.sale_quantity}}</td>
         <td>{{item.inventory_amount}}</td>
         <td>{{item.sale_quantity}}</td>
         <td>{{item.inventory_quantity}}</td>
         <td>{{item.sale_sku}}</td>
         <td>{{item.inventory_sku}}</td>
         <td>{{item.turnover_ration}}</td>
         <td>{{item.sale_ratio}}</td>
         <td>{{item.inventory_ratio}}</td>
      </tr>
    </table>

    <table class="p06_table_2" id="p06_table_2"><!-- 新接口 -->
      <tr>
         <th class="th01">大类</th>
         <th class="th02">性别</th>
         <th class="th03">系列</th>
         <th class="th04">折扣</th>
         <th class="th04">销售额</th>
         <th class="th04">库存额</th>
         <th class="th04">销售量</th>
         <th class="th04">库存量</th>
         <th class="th04">销售SKU</th>
         <th class="th04">库存SKU</th>
         <th class="th04">动销率</th>
         <th class="th04">销售占比</th>
         <th class="th04">库存占比</th>
      </tr>
      <tr v-for="item in shoestable2_2">
         <td>{{item.shoename}}</td>
         <td >{{item.category_name}}</td>
         <td>{{item.series_name}}</td>
         <td>{{item.sale_discount}}</td>
         <td>{{item.sale_quantity}}</td>
         <td>{{item.inventory_amount}}</td>
         <td>{{item.sale_quantity}}</td>
         <td>{{item.inventory_quantity}}</td>
         <td>{{item.sale_sku}}</td>
         <td>{{item.inventory_sku}}</td>
         <td>{{item.turnover_ration}}</td>
         <td>{{item.sale_ratio}}</td>
         <td>{{item.inventory_ratio}}</td>
      </tr>
    </table>


    <div class="boxtail">
    {{homedata.store_name}}·{{homedata.time_year}}年第{{homedata.week_no}}周
    | <span class="boxtail_span">06</span>
    </div>
  </div>

  <div class="box p07">
    <div class="boxhead">店长{{homedata.report_type}}分析报告</div>
    

    <div class="boxtail">
    {{homedata.store_name}}·{{homedata.time_year}}年第{{homedata.week_no}}周
    | <span class="boxtail_span">07</span>
    </div>
  </div>


  
</div>
</template>
<script>
import echarts from 'echarts';
import axios from 'axios';
import pdf from 'vue-pdf';

export default {
  components:{pdf},
  data() {
    return {
      store_id:"nk11",//模拟,上线改为从参数获得
      week_no:201730,//模拟,上线改为从参数获得
      version:20170810,//模拟,上线改为从参数获得
      baseurl:"http://rapapi.org/mockjs/23877",

      //store_id:null,//线上
      // week_no:null,//线上
      //baseurl:null,//线上

      title1_1:"1-1.销售额与完成率",
      title1_2:"1-2.销售额与折扣",
      title1_3:"1-3.客单价与客单量",
      legend1_1:"完成率",
      legend1_2:"折扣",
      legend1_3:"销售额",
      legend1_4:"客单价",
      legend1_5:"客单量",

      title2_1_1:"销存占比-品牌季节",
      xAxis2_1_1:['鞋','服','配','合计'],
      title2_1_2:'销存占比-性别',
      yAxis2_1_2:['配','服','鞋'],
      
      //首页数据
      homedata:{
        store_name:"测试:南京蓝色港湾nk店",
        time_year:"2017",
        week_no:"4",
        time_day:"07/11-07/17",
        report_type:"周",
        director_name:"王海",
        store_level:"C++",
        store_tel:"010-01022222",
        store_type:"FFF",
        stuff_email:"2222222@163.com",
        stuff_name:"刘畅",
        stuff_phone:"13333334444",
        time_update:"2017-05-05",
      },
      //1-1,1-2,1-3数据
      saledata:{
        sale_amounts:[27,245,128,79,90,78],//销售额数组
        sale_finishs:[54,78,16,32,67,32],//完成率数组
        sale_discounts:[78,89,54,34,23,45], //折扣数组
        week_nos:["44周","45周","46周","47周","48周","49周"], //周数组
        customer_sale_amounts:[127,445,185,79,90,78],//客单价数组
        customer_sale_quantity:[1.2,1.5,1.3,1.8,1.2,1.6],//客单量数组
      },

      //2-1 销存占比-品牌季节 后端数据模拟
      sean_ajaxdata:[
        {
            "brand_season": '15Q1',//品牌季节
            "category_id": 'c34',//大类ID
            "category_name": '鞋',//大类名称
            "inventory_amount": 134,//库存额
            "sale_amount": 178//销售额
        },
        {
            "brand_season": '16Q1',
            "category_id": 'c34',
            "category_name": '鞋',
            "inventory_amount": 178,
            "sale_amount": 129
        },
        {
            "brand_season": '16Q2',
            "category_id": 'c34',
            "category_name": '鞋',
            "inventory_amount": 108,
            "sale_amount": 196
        },
        {
            "brand_season": '15Q1',
            "category_id": 'c35',
            "category_name": '服',
            "inventory_amount": 278,
            "sale_amount": 229
        },
        {
            "brand_season": '16Q1',
            "category_id": 'c35',
            "category_name": '服',
            "inventory_amount": 278,
            "sale_amount": 229
        },
        {
            "brand_season": '16Q2',
            "category_id": 'c35',
            "category_name": '服',
            "inventory_amount": 208,
            "sale_amount": 279
        },
        {
            "brand_season": '15Q1',
            "category_id": 'c36',
            "category_name": '配',
            "inventory_amount": 378,
            "sale_amount": 329
        },
        {
            "brand_season": '16Q1',
            "category_id": 'c36',
            "category_name": '配',
            "inventory_amount": 378,
            "sale_amount": 329
        },
        {
            "brand_season": '16Q2',
            "category_id": 'c36',
            "category_name": '配',
            "inventory_amount": 308,
            "sale_amount": 379
        },
        {
            "brand_season": '15Q1',
            "category_id": 'c37',
            "category_name": '总计',
            "inventory_amount": 578,
            "sale_amount": 529
        },
        {
            "brand_season": '16Q1',
            "category_id": 'c37',
            "category_name": '总计',
            "inventory_amount": 578,
            "sale_amount": 529
        },
        {
            "brand_season": '16Q2',
            "category_id": 'c37',
            "category_name": '总计',
            "inventory_amount": 508,
            "sale_amount": 579
        },
      ],

      //2-1 销存占比-品牌季节 本地数据
      seasondata2_1:{
        //右侧季节表格 模拟
        biaoge2_1_0:[
          {
            "brand_season": '15Q1',//品牌季节
            "inventory_amount_01": 134,//库存额
            "sale_amount_01": 178,//销售额
            "inventory_amount_02": 254,//库存额
            "sale_amount_02": 348,//销售额
            "inventory_amount_03": 884,//库存额
            "sale_amount_03": 978,//销售额
            "inventory_amount_04": 634,//库存额
            "sale_amount_04": 448,//销售额
          },
          {
            "brand_season": '15Q2',
            "inventory_amount_01": 134,//库存额
            "sale_amount_01": 188,//销售额
            "inventory_amount_02": 254,//库存额
            "sale_amount_02": 348,//销售额
            "inventory_amount_03": 884,//库存额
            "sale_amount_03": 978,//销售额
            "inventory_amount_04": 634,//库存额
            "sale_amount_04": 448,//销售额
          },
          {
            "brand_season": '15Q2',
            "inventory_amount_01": 134,//库存额
            "sale_amount_01": 198,//销售额
            "inventory_amount_02": 254,//库存额
            "sale_amount_02": 348,//销售额
            "inventory_amount_03": 884,//库存额
            "sale_amount_03": 978,//销售额
            "inventory_amount_04": 634,//库存额
            "sale_amount_04": 448,//销售额
          }      
        ],

        //右侧性别表格
        biaoge2_1_1:[
          {
            "brand_season": '男子',//品牌季节
            "inventory_amount_01": 134,//库存额
            "sale_amount_01": 178,//销售额
            "inventory_amount_02": 254,//库存额
            "sale_amount_02": 348,//销售额
            "inventory_amount_03": 884,//库存额
            "sale_amount_03": 978,//销售额
          },
          {
            "brand_season": '女子',
            "inventory_amount_01": 134,//库存额
            "sale_amount_01": 188,//销售额
            "inventory_amount_02": 254,//库存额
            "sale_amount_02": 348,//销售额
            "inventory_amount_03": 884,//库存额
            "sale_amount_03": 978,//销售额
          },
          {
            "brand_season": '儿童',
            "inventory_amount_01": 134,//库存额
            "sale_amount_01": 198,//销售额
            "inventory_amount_02": 254,//库存额
            "sale_amount_02": 348,//销售额
            "inventory_amount_03": 884,//库存额
            "sale_amount_03": 978,//销售额
          }      
        ],

        //左侧图模拟
        shoessales:[15, 15, 20, 70],//鞋销售额数组
        shoesinventorys:[120, 132, 101, 194],//鞋库存额数组
        clothessales:[120, 192, 81, 134],//服销售额数组
        clothesinventorys:[145, 132, 101, 174],//服库存额数组
        accesssales:[245,134,278,324],//配销售额数组
        accessinventorys:[345,123,425,346],//配库存额数组
        totalsales:[768,342,865,539],//总计销售额数组
        totalinventorys:[324,563,789,458],//总计库存额数组
        seanname2_1_1:['15Q1','15Q2','15q3','15q4'],//季节数组
        legendname2_1_1:['15销售Q1','15销售Q2','15销售Q3','15销售Q4','','15库存Q1','15库存Q2','15库存Q3','15库存Q4'],
        seriesarray:[
            {
              name:"15销售Q1",
              type:'bar',
              barWidth:20,
              stack:'销售',
              data:[15, 15, 20,70],
              itemStyle:{
                 normal:{
                    color:'#004d88',//柱状图样式
                 }, 
              }
            },
            {
              name:"15销售Q2",
              type:'bar',
              barWidth:20,
              stack:'销售',
              data:[25, 25, 35, 15],
              itemStyle:{
                 normal:{color:'#92aecf'} //柱状图样式
              }
            },
            {
              name:"15销售Q3",
              type:'bar',
              barWidth:20,
              stack:'销售',
              data:[25, 35, 25, 5],
              itemStyle:{
                 normal:{color:'#485b82'} //柱状图样式
              }
            },
            {
              name:"15销售Q4",
              type:'bar',
              barWidth:20,
              stack:'销售',
              data:[35, 25, 20, 10],
              itemStyle:{
                 normal:{color:'#0076b0'} //柱状图样式
              }
            },
            {
              name:"15库存Q1",
              type:'bar',
              barWidth:20,
              stack:'库存',
              data:[17, 28, 37, 40],
              itemStyle:{
                 normal:{color:'#004d88'} //柱状图样式
              }
            },
            {
              name:"15库存Q2",
              type:'bar',
              barWidth:20,
              stack:'库存',
              data:[23, 22, 30, 10],
              itemStyle:{
                 normal:{color:'#92aecf'} //柱状图样式
              }
            },
            {
              name:"15库存Q3",
              type:'bar',
              barWidth:20,
              stack:'库存',
              data:[30, 34, 13, 20],
              itemStyle:{
                 normal:{color:'#485b82'} //柱状图样式
              }
            },
            {
              name:"15库存Q4",
              type:'bar',
              barWidth:20,
              stack:'库存',
              data:[30, 16, 20, 30],
              itemStyle:{
                 normal:{color:'#0076b0'} //柱状图样式
              }
            }
        ]
      },

      //2-1 销存占比-性别  本地数据
      sexdata2_1_2:{
         legendname2_1_2:['男子','女子','儿童','无性别'],
         seriesarray:[
            {
              name:"男子销售",
              type:'bar',
              barWidth:20,
              stack:'销售',
              data:[15, 15, 20],
              itemStyle:{
                 normal:{
                    color:'#004d88',//柱状图样式
                 }, 
              }
            },
            {
              name:"女子销售",
              type:'bar',
              barWidth:20,
              stack:'销售',
              data:[25, 25, 35],
              itemStyle:{
                 normal:{color:'#92aecf'} //柱状图样式
              }
            },
            {
              name:"儿童销售",
              type:'bar',
              barWidth:20,
              stack:'销售',
              data:[25, 35, 25],
              itemStyle:{
                 normal:{color:'#485b82'} //柱状图样式
              }
            },
            {
              name:"无性别销售",
              type:'bar',
              barWidth:20,
              stack:'销售',
              data:[35, 25, 20],
              itemStyle:{
                 normal:{color:'#0076b0'} //柱状图样式
              }
            },
            {
              name:"男子库存",
              type:'bar',
              barWidth:20,
              stack:'库存',
              data:[17, 28, 37],
              itemStyle:{
                 normal:{color:'#004d88'} //柱状图样式
              }
            },
            {
              name:"女子库存",
              type:'bar',
              barWidth:20,
              stack:'库存',
              data:[23, 22, 30],
              itemStyle:{
                 normal:{color:'#92aecf'} //柱状图样式
              }
            },
            {
              name:"儿童库存",
              type:'bar',
              barWidth:20,
              stack:'库存',
              data:[30, 34, 13],
              itemStyle:{
                 normal:{color:'#485b82'} //柱状图样式
              }
            },
            {
              name:"无性别库存",
              type:'bar',
              barWidth:20,
              stack:'库存',
              data:[30, 16, 20],
              itemStyle:{
                 normal:{color:'#0076b0'} //柱状图样式
              }
            }
        ]
      },

      //p06 2-2 鞋分析表格
      rowspandata1:false,//鞋的rowspan值
      rowspandata2:false,//性别的rowspan值
      shoestable2_2_1:[
        {
            "category_id": "201666666666",
            "category_name": "男子",
            "inventory_amount": 1216849,
            "inventory_amount_ratio": 48445,
            "inventory_quantity": 1271,
            "inventory_sku": 94,
            "sale_amount": 127662,
            "sale_amount_ratio": 23640,
            "sale_discount": 0.9758748796037242,
            "sale_nos_amount": 130818,
            "sale_quantity": 122,
            "sale_sku": 61,
            "sale_sku_ratio": 0.648936170212766,
            "sub": [
                {
                    "inventory_amount_ratio": 1,
                    "sale_amount_ratio": 1,
                    "sub": 1,
                    "category_id": "20160807000161",
                    "category_name": "篮球",
                    "inventory_amount": 286872,
                    "inventory_quantity": 298,
                    "inventory_sku": 21,
                    "sale_amount": 14164,
                    "sale_discount": 0.9724682457947134,
                    "sale_nos_amount": 14565,
                    "sale_quantity": 15,
                    "sale_sku": 111111,
                    "sale_sku_ratio": 0.5714285714285714
                },
                {
                    "inventory_amount_ratio": 1,
                    "sale_amount_ratio": 1,
                    "sub": 1,
                    "category_id": "20160807000162",
                    "category_name": "足球",
                    "inventory_amount": 95522,
                    "inventory_quantity": 148,
                    "inventory_sku": 14,
                    "sale_amount": 6737,
                    "sale_discount": 0.9556028368794326,
                    "sale_nos_amount": 7050,
                    "sale_quantity": 10,
                    "sale_sku": 122222,
                    "sale_sku_ratio": 0.5714285714285714
                },
                {
                    "inventory_amount_ratio": 1,
                    "sale_amount_ratio": 1,
                    "sub": 1,
                    "category_id": "20160807000163",
                    "category_name": "跑步",
                    "inventory_amount": 724450,
                    "inventory_quantity": 640,
                    "inventory_sku": 46,
                    "sale_amount": 100536,
                    "sale_discount": 0.9789765811383222,
                    "sale_nos_amount": 102695,
                    "sale_quantity": 85,
                    "sale_sku": 133333,
                    "sale_sku_ratio": 0.717391304347826
                },
                {
                    "inventory_amount_ratio": 1,
                    "sale_amount_ratio": 1,
                    "sub": 1,
                    "category_id": "20160807000167",
                    "category_name": "网球",
                    "inventory_amount": 65371,
                    "inventory_quantity": 109,
                    "inventory_sku": 8,
                    "sale_amount": 2675,
                    "sale_discount": 0.9605026929982047,
                    "sale_nos_amount": 2785,
                    "sale_quantity": 5,
                    "sale_sku": 144444,
                    "sale_sku_ratio": 0.5
                }
            ]
        },
        {
            "category_id": "20160419000167",
            "category_name": "女子",
            "inventory_amount": 1216849,
            "inventory_amount_ratio": 48445,
            "inventory_quantity": 1271,
            "inventory_sku": 94,
            "sale_amount": 127662,
            "sale_amount_ratio": 23640,
            "sale_discount": 0.9758748796037242,
            "sale_nos_amount": 130818,
            "sale_quantity": 122,
            "sale_sku": 61,
            "sale_sku_ratio": 0.648936170212766,
            "sub": [
                {
                    "inventory_amount_ratio": 1,
                    "sale_amount_ratio": 1,
                    "sub": 1,
                    "category_id": "20160807000163",
                    "category_name": "跑步",
                    "inventory_amount": 724450,
                    "inventory_quantity": 640,
                    "inventory_sku": 46,
                    "sale_amount": 100536,
                    "sale_discount": 0.9789765811383222,
                    "sale_nos_amount": 102695,
                    "sale_quantity": 85,
                    "sale_sku": 211111,
                    "sale_sku_ratio": 0.717391304347826
                },
                {
                    "inventory_amount_ratio": 1,
                    "sale_amount_ratio": 1,
                    "sub": 1,
                    "category_id": "20160807000167",
                    "category_name": "网球",
                    "inventory_amount": 65371,
                    "inventory_quantity": 109,
                    "inventory_sku": 8,
                    "sale_amount": 2675,
                    "sale_discount": 0.9605026929982047,
                    "sale_nos_amount": 2785,
                    "sale_quantity": 5,
                    "sale_sku": 2222222,
                    "sale_sku_ratio": 0.5
                },
                {
                    "inventory_amount_ratio": 1,
                    "sale_amount_ratio": 1,
                    "sub": 1,
                    "category_id": "20160807000168",
                    "category_name": "户外",
                    "inventory_amount": 41841,
                    "inventory_quantity": 69,
                    "inventory_sku": 4,
                    "sale_amount": 3151,
                    "sale_discount": 0.9479542719614922,
                    "sale_nos_amount": 3324,
                    "sale_quantity": 6,
                    "sale_sku": 23333,
                    "sale_sku_ratio": 0.75
                },
                {
                    "inventory_amount_ratio": 1,
                    "sale_amount_ratio": 1,
                    "sub": 1,
                    "category_id": "20160807000169",
                    "category_name": "游泳",
                    "inventory_amount": 2793,
                    "inventory_quantity": 7,
                    "inventory_sku": 1,
                    "sale_amount": 399,
                    "sale_discount": 1,
                    "sale_nos_amount": 399,
                    "sale_quantity": 1,
                    "sale_sku": 244444,
                    "sale_sku_ratio": 1
                }
            ]
        }
      ],
      shoestable2_2_2:null,
      shoestable2_2 :[              
        {
          "category_id": "测试内容p00v",
          "category_name": "男子",
          "gender_id": "测试内容y20k",          
          "inventory_amount": 44333,
          "inventory_quantity": 38720,
          "inventory_ratio": 0.29,
          "inventory_sku": 16474,
          "sale_amount": 40838,
          "sale_discount": 0.8,
          "sale_quantity": 80387,
          "sale_ratio": 0.5,
          "sale_sku": 30141,
          "series_id": 10837,
          "series_name":"户外",
          "turnover_ration": 0.78,         
        },
        {
          "category_id": "测试内容p00v",
          "category_name": "男子",
          "gender_id": "测试内容y20k",
          
          "inventory_amount": 44666,
          "inventory_quantity": 38720,
          "inventory_ratio": 0.29,
          "inventory_sku": 16474,
          "sale_amount": 40838,
          "sale_discount": 0.8,
          "sale_quantity": 80387,
          "sale_ratio": 0.5,
          "sale_sku": 30141,
          "series_id": 10837,
          "series_name":"篮球",
          "turnover_ration": 0.78
        },
        {
          "category_id": "测试内容p00v",
          "category_name": "男子",
          "gender_id": "测试内容y20k",
          
          "inventory_amount": 44777,
          "inventory_quantity": 38720,
          "inventory_ratio": 0.29,
          "inventory_sku": 16474,
          "sale_amount": 40838,
          "sale_discount": 0.8,
          "sale_quantity": 80387,
          "sale_ratio": 0.5,
          "sale_sku": 30141,
          "series_id": 10837,
          "series_name":"羽毛球",
          "turnover_ration": 0.78
        },
        {
          "category_id": "测试内容p00v",
          "category_name": "女子",
          "gender_id": "测试内容y20k",
         
          "inventory_amount": 44333,
          "inventory_quantity": 38720,
          "inventory_ratio": 0.29,
          "inventory_sku": 16474,
          "sale_amount": 40838,
          "sale_discount": 0.8,
          "sale_quantity": 80387,
          "sale_ratio": 0.5,
          "sale_sku": 30141,
          "series_id": 10837,
          "series_name":"户外",
          "turnover_ration": 0.78
        },
        {
          "category_id": "测试内容p00v",
          "category_name": "女子",
          "gender_id": "测试内容y20k",
         
          "inventory_amount": 44333,
          "inventory_quantity": 38720,
          "inventory_ratio": 0.29,
          "inventory_sku": 16474,
          "sale_amount": 40838,
          "sale_discount": 0.8,
          "sale_quantity": 80387,
          "sale_ratio": 0.5,
          "sale_sku": 30141,
          "series_id": 10837,
          "series_name":"篮球",
          "turnover_ration": 0.78
        },
        {
          "category_id": "测试内容p00v",
          "category_name": "女子",
          "gender_id": "测试内容y20k",
         
          "inventory_amount": 44333,
          "inventory_quantity": 38720,
          "inventory_ratio": 0.29,
          "inventory_sku": 16474,
          "sale_amount": 40838,
          "sale_discount": 0.8,
          "sale_quantity": 80387,
          "sale_ratio": 0.5,
          "sale_sku": 30141,
          "series_id": 10837,
          "series_name":"羽毛球",
          "turnover_ration": 0.78
        },
        {
          "category_id": "测试内容p00v",
          "category_name": "合计",
          "gender_id": "测试内容y20k",
          
          "inventory_amount": 44333,
          "inventory_quantity": 38720,
          "inventory_ratio": 0.29,
          "inventory_sku": 16474,
          "sale_amount": 40838,
          "sale_discount": 0.8,
          "sale_quantity": 80387,
          "sale_ratio": 0.5,
          "sale_sku": 30141,
          "series_id": 10837,
          "series_name":"户外",
          "turnover_ration": 0.78
        },
        {
          "category_id": "测试内容p00v",
          "category_name": "合计",
          "gender_id": "测试内容y20k",
          
          "inventory_amount": 44333,
          "inventory_quantity": 38720,
          "inventory_ratio": 0.29,
          "inventory_sku": 16474,
          "sale_amount": 40838,
          "sale_discount": 0.8,
          "sale_quantity": 80387,
          "sale_ratio": 0.5,
          "sale_sku": 30141,
          "series_id": 10837,
          "series_name":"篮球",
          "turnover_ration": 0.78
        },
        {
          "category_id": "测试内容p00v",
          "category_name": "合计",
          "gender_id": "测试内容y20k",
          
          "inventory_amount": 44333,
          "inventory_quantity": 38720,
          "inventory_ratio": 0.29,
          "inventory_sku": 16474,
          "sale_amount": 40838,
          "sale_discount": 0.8,
          "sale_quantity": 80387,
          "sale_ratio": 0.5,
          "sale_sku": 30141,
          "series_id": 10837,
          "series_name":"羽毛球",
          "turnover_ration": 0.78
        }         
      ],
   
    }
  },
  created() {
    
  },
  mounted() {
    //获得查询参数store_id 和week_no,version
    // var getInfo=window.location.search.slice(window.location.search.lastIndexOf("?")+1);
    // this.store_id = getInfo.split("|")[0],
    // this.week_no = getInfo.split("|")[1],
    // this.version = getInfo.split("|")[2],

    //第一页
    this.home_ajax()

    this.draw1('1_1',this.legend1_3,this.legend1_1,this.title1_1,this.saledata.sale_amounts,this.saledata.sale_finishs,this.saledata.week_nos)
    this.draw1('1_2',this.legend1_3,this.legend1_2,this.title1_2,this.saledata.sale_amounts,this.saledata.sale_discounts,this.saledata.week_nos)
    this.draw2('1_3',this.legend1_4,this.legend1_5,this.title1_3,this.saledata.customer_sale_amounts,this.saledata.customer_sale_quantity,this.saledata.week_nos)

    //第4页 表2-1 销存占比-品牌
    this.draw3('2_1_1',this.title2_1_1,this.seasondata2_1.legendname2_1_1,this.xAxis2_1_1,this.seasondata2_1.seriesarray)

    //第4页 表2-1 销存占比-性别
    this.draw4('2_1_2',this.title2_1_2,this.sexdata2_1_2.legendname2_1_2,this.yAxis2_1_2,this.sexdata2_1_2.seriesarray)

    //第4页 表2-1 销存占比-品牌
 
    //表06 表2-2 新
    let a =this.shoestable2_2_1.length
    let b=0
    for(let i=0;i<this.shoestable2_2_1.length;i++){
       b = b + this.shoestable2_2_1[i].sub.length
    }
    a = a+b
    //console.log(a)

    //p06 表2-2 表 旧
    for(let i=0;i<this.shoestable2_2.length;i++){
      this.shoestable2_2[i].shoename = "鞋"
      this.shoestable2_2[i].rowspandata1 = this.shoestable2_2.length

    } 
    for (let k=1;k<this.shoestable2_2.length;k++) {
          let d=k-1;
          if(this.shoestable2_2[k].shoename == this.shoestable2_2[d].shoename ){
             this.shoestable2_2[k].rowspandata1 = false
          }
          if(this.shoestable2_2[k].category_name == this.shoestable2_2[d].category_name ){
             this.shoestable2_2[k].rowspandata2 = 1
          }
    }
    this.SpanGrid(p06_table,0,1) //合并p06表格第一列
    this.SpanGrid(p06_table,1,1) //合并p06表格第二列
    this.changedatap06(this.shoestable2_2_1)//遍历p06接口数据

  },
  methods: {
      //首页
      home_ajax(){
          axios({
               method: 'get',
               url: this.baseurl + '/stuff_report/store_info?',
               params:{
                store_id:this.store_id
               }
           }).then( (response) => {
              if(response.data != null){
                  //console.log(response.data)
                  this.homedata = response.data
              }else{
                  
              }                         
           })
      },

      //表1-1 1-2
      draw1(id,legendname0,legendname,titlename,seriesdatafirst,seriesdatasecond,week_nos){
        this.charts1 = echarts.init(document.getElementById(id))
        this.charts1.setOption({
           title:{
            text:titlename
           },
           tooltip:{
             trigger:'axis',//提示触发方式
             axisPointer:{  //指示类型
              type:'cross',
              crossStype:{
                color:'red'
              } 
             } 
           },
           legend:{
             bottom:1,//图例放在图下面
             data:[legendname0,legendname]
           },
           xAxis:{
            data:week_nos
           },
           yAxis:[
             {
                type:'value',
                axisLabel:{
                  formatter:'{value}'
                }
            },
            {
                type:'value',
                min:0,
                max:100,
                interval:10,
                axisLabel:{
                  formatter:'{value}%'
                }
            }
           ],
           series:[  
           {
             name:legendname0,
             type:'bar',
             barWidth:18, //表格宽度
             data:seriesdatafirst,
             itemStyle:{
              normal:{color:'#004a86'} //默认状态样式
             }
           },
           {
              name:legendname,
              type:'line',
              yAxisIndex:1,
              data:seriesdatasecond
            }           
           ]
        })
      },

      //表1-3
      draw2(id,legendname0,legendname,titlename,seriesdatafirst,seriesdatasecond,week_nos){
        this.charts1 = echarts.init(document.getElementById(id))
        this.charts1.setOption({
           title:{
            text:titlename
           },
           tooltip:{
             trigger:'axis',//提示触发方式
             axisPointer:{  //指示类型
              type:'cross',
              crossStype:{
                color:'red'
              } 
             } 
           },
           legend:{
             bottom:1,
             data:[legendname0,legendname]
           },
           xAxis:{
            data:week_nos
           },
           yAxis:[
             {
                type:'value',
                axisLabel:{
                  formatter:'{value}'
                }
            },
            {
                type:'value',
                axisLabel:{
                  formatter:'{value}'
                }
            }
           ],
           series:[  
           {
             name:legendname0,
             type:'bar',
             barWidth:18,
             data:seriesdatafirst,
             itemStyle:{
              normal:{color:'#004a86'} //默认状态样式
             }
           },
           {
              name:legendname,
              type:'line',
              yAxisIndex:1,
              data:seriesdatasecond
            }           
           ]
        })
      },

      //品类分析表2-1 销存占比-品牌
      draw3(id,titlename,legendname,xAxisname,seriesarray){
        this.charts = echarts.init(document.getElementById(id))
        this.charts.setOption({
          title:{
            tetx:titlename
          },
          tooltip : {
              show:false,
              trigger: 'axis',
              axisPointer : {            // 坐标轴指示器，坐标轴触发有效
                  type : 'shadow'        // 默认为直线，可选为：'line' | 'shadow'
              }
          },
          legend:{
             show:true,
             bottom:-5,
             data:legendname,
          },
          yAxis:{
            type:'value',
            min:0,
            max:100,
            interval:10,  
            axisLabel:{
              formatter:'{value} %'
            },             
          },
          xAxis:{
            type:'category',
            data:xAxisname,
            axisTick:{
              show:false
            }
          },
          series:[
            {
              name:"15销售Q1",
              type:'bar',
              barWidth:18,
              barGap:'200%',
              stack:'销售',
              data:[15, 15, 20,70],
              itemStyle:{
                 normal:{
                    color:'#5e7bb6',//柱状图样式
                 }, 
              }
            },
            {
              name:"15销售Q2",
              type:'bar',
              barWidth:18,
              stack:'销售',
              data:[25, 25, 35, 15],
              itemStyle:{
                 normal:{color:'#92aecf'} //柱状图样式
              }
            },
            {
              name:"15销售Q3",
              type:'bar',
              barWidth:18,
              stack:'销售',
              data:[25, 35, 25, 5],
              itemStyle:{
                 normal:{color:'#0076b0'} //柱状图样式
              }
            },
            {
              name:"15销售Q4",
              type:'bar',
              barWidth:18,
              stack:'销售',
              data:[35, 25, 20, 10],
              itemStyle:{
                 normal:{color:'#0076b0'} //柱状图样式
              }
            },
            {
              name:"15库存Q1",
              type:'bar',
              barWidth:18,
              stack:'库存',
              data:[17, 28, 37, 40],
              itemStyle:{
                 normal:{color:'#5e7bb6'} //柱状图样式
              }
            },
            {
              name:"15库存Q2",
              type:'bar',
              barWidth:18,
              stack:'库存',
              data:[23, 22, 30, 10],
              itemStyle:{
                 normal:{color:'#92aecf'} //柱状图样式
              }
            },
            {
              name:"15库存Q3",
              type:'bar',
              barWidth:18,
              stack:'库存',
              data:[30, 34, 13, 20],
              itemStyle:{
                 normal:{color:'#0076b0'} //柱状图样式
              }
            },
            {
              name:"15库存Q4",
              type:'bar',
              barWidth:18,
              stack:'库存',
              data:[30, 16, 20, 30],
              itemStyle:{
                 normal:{color:'#0076b0'} //柱状图样式
              }
            }
          ]

        })
      },

      //品类分析 表2-1 销存占比-性别
      draw4(id,titlename,legendname,yAxisname,seriesarray){
        this.charts = echarts.init(document.getElementById(id))
        this.charts.setOption({
          title:{
            tetx:titlename
          },
          tooltip : {
              trigger: 'axis',
              axisPointer : {            // 坐标轴指示器，坐标轴触发有效
                  type : 'shadow'        // 默认为直线，可选为：'line' | 'shadow'
              }
          },
          legend:{
             bottom:-5,
             data:legendname,
          },
          yAxis:{
            type:'value',
            min:0,
            max:100,
            interval:10,  
            axisLabel:{
              formatter:'{value} %'
            },             
          },
          xAxis:{
            type:'category',
            data:yAxisname,
            axisTick:{
              show:false
            }
          },
          series:seriesarray,

        })
      },

      //p06 ajax数据处理
      changedatap06(data){
          var cc = {};
          var dd = []
          console.log(data)
          for(var i=0;i<data.length;i++){           
             //dd.push({
             // category_id:data[i].category_id,
             // sale_sku: data[i].sale_sku
           //  }) 
             for(var j=0;j<data[i].sub.length;j++) {
              dd.push({
                category_id:data[i].sub[j].category_id,
                sale_sku: data[i].sub[j].sale_sku
               }) 
             }    
          }
          console.log(dd)

      },

      //合并单元格算法
      //tabObj代表表的Id，即GridView的Id，cellIndex代表合并第几列，beignRow 代表从几行开始，通常使用1，因为0是表头
      SpanGrid(tabObj, cellindex, beginRow) {
          var colIndex = cellindex;
          var rowBeginIndex = beginRow;
          if (tabObj != null) {
              var i, j, m;
              var intSpan;
              var strTemp;
              m = 0;
              for (i = rowBeginIndex; i < tabObj.rows.length; i++) {
                  intSpan = 1;
                  m++;
                  strTemp = tabObj.rows[i].cells[colIndex].innerText;
                  for (j = i + 1; j < tabObj.rows.length; j++) {
                      if (strTemp == tabObj.rows[j].cells[colIndex].innerText) {
                          intSpan++;
                          tabObj.rows[i].cells[colIndex].rowSpan = intSpan;
                          tabObj.rows[j].cells[colIndex].style.display = "none";
                      }
                      else {
                          break;
                      }
                  }

              }
              i = j - 1;
          }
      },
  }

} 
</script>
<style lang="scss" scoped>
.all{
  background-color: #e9ebf2;
  width: 1104px;
  margin: 0 auto;
}
.box{
  background-color: white;
  width:1104px;
  height:1557px;
  border:1px solid red;
  margin-bottom: 20px;
  position:relative;
  .boxhead{
    position:absolute;
    left:945px;
    top:30px;
    font-size:12px;
    color:#999999;
    letter-spacing:0;
    text-align:left;
  }
  .boxtail{
    position:absolute;
    left:797px;
    top:1512px;
    font-size:12px;
    color:#333333;
    letter-spacing:0;
    text-align:left;
    .boxtail_span{
      font-size:14px;
      color:#000000;
      letter-spacing:0;
    }
  }
  .zititle_left{
    position:absolute;
    left: 70px;
    top: 76px;
    background:#004a86;
    width:4px;
    height:20px;
  }
  .zititle{
    position:absolute;
    left: 80px;
    top: 70px;
    font-size:24px;
    color:#004a86;
    letter-spacing:0;
    text-align:left;
  }
  .zititle2{
    position: absolute;
    left:67px;
    top:131px;
    font-size:18px;
    color:#333333;
    letter-spacing:0;
    text-align:left;
  }
}
.p1headtop{
  height:317px;
  color:#867ae4;
  background: url('../static/dasuan_logo.png') no-repeat;
  background-position:900px 52px;
  background-size:100px 100px;
  // border:1px solid blue;
  //position: relative;
  .p1headtop_span_line{
    position:absolute;
    left: 851px;
    top: 178px;
    border-top:1px solid #a8a8a8;
    width:199px;
    height:2px;
  }
  .p1headtop_span{
    position:absolute;
    left: 891px;
    top: 186px;
    font-size:18px;
    color:#867ae4;
    letter-spacing:0;
  }
} 
.p1headdown{
  margin-left:50px;
  width: 1002px;
  height:40px;
  font-size:18px;
  color:#333333;
  letter-spacing:0;
  text-align:left;
  border-bottom:1px solid #a8a8a8;
}
.p1middle_top{
  position:absolute;
  left:46px;
  top:374px;
  font-size:70px;
  color:#000000;
  letter-spacing:0;
  text-align:left;
}
.p1middle_middle{
  position:absolute;
  left: 48px;
  top: 1103px;
  font-size:20px;
  color:#666666;
  letter-spacing:0;
  text-align:left;
}
.p1middle_down{
  position: absolute;
  left: 48px;
  top:1404px;
  color:#666666;
  letter-spacing:0;
  line-height:20px;
  text-align:left;
}
.p01{
  .p01head{
    position:absolute;
    left: 481px;
    top:162px;
    .p01head_top{
      font-size:70px;
      color:#000000;
      letter-spacing:0;
      text-align:left;
    }
    .p01head_down{
      font-family:PingFangSC-Semibold;
      font-size:30px;
      color:#333333;
      letter-spacing:0;
      text-align:left;
    }
  }
  .p01middle{
    position:absolute;
    left: 251px;
    top:457px;
    .p01middle_div{
      border-top:1px dashed #a8a8a8;
      width:600px;
      height: 98px;
      .p01_number{
         font-size:50px;
         color:#000000;
         letter-spacing:0;
         text-align:left;
         float: left;
         padding-top:5px;
      }
      .p01_content{
         font-size:28px;
         color:#000000;
         letter-spacing:0;
         text-align:left;
         float: left;
         padding-left:45px;
         padding-top:23px;
      }
    }
    .p01middle_div_down{
      border-bottom:1px dashed #a8a8a8;
    }
  }
}
.p02{
  .sale01{
    position:absolute;
    left: 70px;
    top: 135px;
    width: 430px;
    height: 440px;
  }
  .sale02{
    position:absolute;
    left: 613px;
    top: 135px;
    width: 430px;
    height: 440px;
  }
  .sale03{
    position:absolute;
    left: 70px;
    top: 625px;
    width: 430px;
    height: 440px;
  }
}
.p04{
  .p04_brand01{
    position:absolute;
    left:86px;
    top:190px;
    width: 530px;
    height: 430px;
  }
  .p04_pinpai_logo{
    position:absolute;
    left: 68px;
    top: 202px;
    width: 12px;
    height: 12px;
    border-radius:6px;
    background:#1c4a82;
  }
  .p04_pinpai{
    position: absolute;
    left: 86px;
    top: 198px;
    font-size:14px;
    color:#000000;
    letter-spacing:0;
    text-align:left;
  }
  .p04_zhongxian{
    position:absolute;
    left: 615px;
    top:233px;
    border-left: 1px dashed #a8a8a8;
    width: 2px;
    height: 400px;
  }
  .p04_zhongxian2{
    position:absolute;
    left: 615px;
    top:890px;
    border-left: 1px dashed #a8a8a8;
    width: 2px;
    height: 400px;
  }
  .p04_table1_head1{
    position:absolute;
    left: 633px;
    top: 280px;
    font-size: 12px;
    .p04_table1_dalei{
      float: left;
      width: 43px;
      height: 42px;
      background: #1c4a82;
      color: white;
      line-height: 42px;
      border-left: 1px solid #ccc;
      border-right: 1px solid #ccc;
    }
    .p04_table1_xie{
     float: left;    
      line-height: 40px;
       width: 84px;
       height: 40px;
       border:1px solid #e5e5e5;
    }
    .p04_table1_fu{
       float: left;    
       line-height: 40px;
       width: 84px;
       height: 40px;
       border-top:1px solid #e5e5e5;
       border-bottom:1px solid #e5e5e5;
    }
    .p04_table1_heji{
     float: left;    
      line-height: 40px;
       width: 84px;
       height: 40px;
       border-top:1px solid #e5e5e5;
       border-bottom:1px solid #e5e5e5;
       border-right:1px solid #e5e5e5;
    }
  }
  .p04_table1_head2{
    position:absolute;
    left: 633px;
    top: 905px;
    font-size: 12px;
    .p04_table1_dalei{
      float: left;
      width: 43px;
      height: 42px;
      background: #1c4a82;
      color: white;
      line-height: 42px;
      border-left: 1px solid #ccc;
      border-right: 1px solid #ccc;
    }
    .p04_table1_xie{
     float: left;    
      line-height: 40px;
       width: 84px;
       height: 40px;
       border:1px solid #e5e5e5;
    }
    .p04_table1_fu{
       float: left;    
       line-height: 40px;
       width: 84px;
       height: 40px;
       border-top:1px solid #e5e5e5;
       border-bottom:1px solid #e5e5e5;
    }
    .p04_table1_heji{
     float: left;    
      line-height: 40px;
       width: 84px;
       height: 40px;
       border-top:1px solid #e5e5e5;
       border-bottom:1px solid #e5e5e5;
       border-right:1px solid #e5e5e5;
    }
  }
  .p04_table1{
    position:absolute;
    left: 633px;
    top: 322px;
    font-size: 12px;
    .th01{
      height: 40px;
      width: 43px;
      letter-spacing:0;
      text-align: center;
      border-top:1px solid #ccc;
      background:#1c4a82;
      color:white;
      border-left: 1px solid #ccc;
    }
    .th02{
      height: 40px;
      width: 42px;
      letter-spacing:0;
      text-align: center;
      border-left:1px solid #ccc;
    }
    .th05{
      height: 40px;
      width: 41px;
      letter-spacing:0;
      text-align: center;
      border-left:1px solid #ccc;
    }
    .th07{
      height: 40px;
      width: 41px;
      letter-spacing:0;
      text-align: center;
      border-left:1px solid #ccc;
      border-right:1px solid #ccc;
    }
    td{
       letter-spacing:0;
       text-align: center;
       border:1px solid #ccc;
    }
  }
  .p04_table2{
    position:absolute;
    left: 633px;
    top: 947px;
    font-size: 12px;
    .th01{
      height: 40px;
      width: 43px;
      letter-spacing:0;
      text-align: center;
      border-top:1px solid #ccc;
      background:#1c4a82;
      color:white;
      border-left: 1px solid #ccc;
    }
    .th02{
      height: 40px;
      width: 42px;
      letter-spacing:0;
      text-align: center;
      border-left:1px solid #ccc;
    }
    .th05{
      height: 40px;
      width: 41px;
      letter-spacing:0;
      text-align: center;
      border-left:1px solid #ccc;
    }
    .th07{
      height: 40px;
      width: 41px;
      letter-spacing:0;
      text-align: center;
      border-left:1px solid #ccc;
      border-right:1px solid #ccc;
    }
    td{
       letter-spacing:0;
       text-align: center;
       border:1px solid #ccc;
    }
  }
  .p04_brand02{
    position:absolute;
    left:86px;
    top:890px;
    width: 530px;
    height: 430px;
  }
  .p04_pinpai_logo_sex{
    position:absolute;
    left: 68px;
    top: 857px;
    width: 12px;
    height: 12px;
    border-radius:6px;
    background:#1c4a82;
  }
  .p04_pinpai_sex{
    position: absolute;
    left: 86px;
    top: 853px;
    font-size:14px;
    color:#000000;
    letter-spacing:0;
    text-align:left;
  }
}
.p06{
  .p06_table{
    position:absolute;
    left:67px;
    top:95px;
    th{
      height: 43px;
      background-color:#1c4a82;
      font-size:14px;
      color:#ffffff;
      letter-spacing:0;
      text-align: center;
      border-left:1px solid #ccc;
    }
    td{
      height: 35px;
      border:1px solid #ccc
    }
    .th01{
      width: 50px;
    }
    .th02{
      width: 60px;
    }
    .th03{
      width: 80px;
    }
    .th04{
      width: 76px;
    }
  }
  .p06_table_2{
    position:absolute;
    left:67px;
    top:595px;
    th{
      height: 43px;
      background-color:#1c4a82;
      font-size:14px;
      color:#ffffff;
      letter-spacing:0;
      text-align: center;
      border-left:1px solid #ccc;
    }
    td{
      height: 35px;
      border:1px solid #ccc
    }
    .th01{
      width: 50px;
    }
    .th02{
      width: 60px;
    }
    .th03{
      width: 80px;
    }
    .th04{
      width: 76px;
    }
  }
}
</style>



















