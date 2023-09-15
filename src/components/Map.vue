<template id="child-map">
  <div>
    <div id="map" :style="style"></div>
    <img id="image-class" src="../assets/tips.299ba2d9.png" class="image-class">
    <!-- <PolygonDB :map="map"></PolygonDB> -->
  </div>
</template>

<script>
  // import PolygonDB from './PolygonDB.vue'

  export default{
    components: {
      // PolygonDB
    },
    data(){
      return{
        mapId: 'map',
        style:{
          width:'100%',
          height:this.m.height+'px',
        },
        // map: null
      }
    },
    props:['m'],
    mounted(){
      this.map = new BMapGL.Map("map"); // 创建地图实例
        var point = new BMapGL.Point(112.20518, 31.022003); // 创建点坐标
        this.map.centerAndZoom(point, 15); // 初始化地图，设置中心点坐标和地图级别
        this.map.enableScrollWheelZoom(true); // 开启鼠标滚轮缩放
        var scaleCtrl = new BMapGL.ScaleControl(); // 添加比例尺控件
        this.map.addControl(scaleCtrl);
        var zoomCtrl = new BMapGL.ZoomControl(); // 添加缩放控件
        this.map.addControl(zoomCtrl);

        //土门巷社区
        var polygon = new BMapGL.Polygon(
          [new BMapGL.Point(112.205413,31.029443),new BMapGL.Point(112.209743,31.02846),new BMapGL.Point(112.20942,31.027679),new BMapGL.Point(112.209159,31.026712),new BMapGL.Point(112.209052,31.025397),new BMapGL.Point(112.208539,31.014379),new BMapGL.Point(112.208773,31.013783),new BMapGL.Point(112.206689,31.012925),new BMapGL.Point(112.206797,31.016801),new BMapGL.Point(112.205934,31.019091),new BMapGL.Point(112.20438,31.022611),
          ],
          {
            strokeColor: "black", // 边界线颜色
            strokeWeight: 2, // 边界线宽度
            strokeOpacity: 0.5, // 边界线透明度
            fillColor: "red", // 填充颜色
            fillOpacity: 0.1, // 填充透明度
            strokeStyle: "dashed", // 边界线样式 (虚线)
          }
        ); //创建多边形


        //2东宝山社区
        var polygon2 = new BMapGL.Polygon(
          [new BMapGL.Point(112.210278,31.024089),new BMapGL.Point(112.211499,31.026224),new BMapGL.Point(112.21587, 31.031441), new BMapGL.Point(112.214972, 31.031689), new BMapGL.Point(112.214468, 31.031457), new BMapGL.Point(112.212807, 31.032346),new BMapGL.Point(112.210183,31.029141),new BMapGL.Point(112.209465,31.02716),new BMapGL.Point(112.20933,31.026433),new BMapGL.Point(112.208998,31.022464),new BMapGL.Point(112.210085,31.022372),
          ],
          {
            strokeColor: "black", // 边界线颜色
            strokeWeight: 2, // 边界线宽度
            strokeOpacity: 0.5, // 边界线透明度
            fillColor: "blue", // 填充颜色
            fillOpacity: 0.1, // 填充透明度
            strokeStyle: "dashed", // 边界线样式 (虚线)
          }
        ); //创建多边形

          //3南台社区
          var polygon3 = new BMapGL.Polygon(
          [new BMapGL.Point(112.208555,31.02873),new BMapGL.Point(112.208681,31.031902),new BMapGL.Point(112.207513,31.032475),new BMapGL.Point(112.207406,31.032753),new BMapGL.Point(112.208142,31.033016),new BMapGL.Point(112.208681,31.03348),new BMapGL.Point(112.21161,31.034316),new BMapGL.Point(112.214035,31.034316),new BMapGL.Point(112.210406,31.029937),new BMapGL.Point(112.209746,31.028502),
          ],
          {
            strokeColor: "black", // 边界线颜色
            strokeWeight: 2, // 边界线宽度
            strokeOpacity: 0.5, // 边界线透明度
            fillColor: "yellow", // 填充颜色
            fillOpacity: 0.1, // 填充透明度
            strokeStyle: "dashed", // 边界线样式 (虚线)
          }
          );

          //4千佛洞社区
           var polygon4 = new BMapGL.Polygon(
          [new BMapGL.Point(112.208924,31.022421),new BMapGL.Point(112.210141,31.022363),new BMapGL.Point(112.209813,31.017957),new BMapGL.Point(112.210136,31.016363),new BMapGL.Point(112.212005,31.016518),new BMapGL.Point(112.212706,31.015249),new BMapGL.Point(112.213424,31.01528),new BMapGL.Point(112.21382,31.016146),new BMapGL.Point(112.214969,31.015806),new BMapGL.Point(112.215454,31.014583),new BMapGL.Point(112.214413,31.011906),new BMapGL.Point(112.213676,31.011473),new BMapGL.Point(112.210873,31.011674),new BMapGL.Point(112.208717,31.014135),
          ],
          {
            strokeColor: "black", // 边界线颜色
            strokeWeight: 2, // 边界线宽度
            strokeOpacity: 0.5, // 边界线透明度
            fillColor: "green", // 填充颜色
            fillOpacity: 0.1, // 填充透明度
            strokeStyle: "dashed", // 边界线样式 (虚线)
          }
        ); //创建多边形

        //塔影社区
        var polygon5 = new BMapGL.Polygon([
          new BMapGL.Point(112.205, 31.019434), 
          new BMapGL.Point(112.204704, 31.019272), 
          new BMapGL.Point(112.205261, 31.018397), 
          new BMapGL.Point(112.205899, 31.018544), 
          new BMapGL.Point(112.204147, 31.022328), 
          new BMapGL.Point(112.204264, 31.023999), 
          new BMapGL.Point(112.204479, 31.02584), 
          new BMapGL.Point(112.205153, 31.029507), 
          new BMapGL.Point(112.204102, 31.02977), 
          new BMapGL.Point(112.203648, 31.030103),
          new BMapGL.Point(112.203213, 31.030822), 
          new BMapGL.Point(112.202755, 31.030613), 
          new BMapGL.Point(112.202764, 31.030203), 
          new BMapGL.Point(112.202243, 31.030049), 
          new BMapGL.Point(112.201686, 31.030296), 
          new BMapGL.Point(112.200841, 31.030025), 
          new BMapGL.Point(112.200985, 31.028718), 
          new BMapGL.Point(112.202755, 31.024301), 
          new BMapGL.Point(112.203877, 31.021647)
        ], { 
            strokeColor: "black", // 边界线颜色
            strokeWeight: 2, // 边界线宽度
            strokeOpacity: 0.5, // 边界线透明度
            fillColor: "green", // 填充颜色
            fillOpacity: 0.1, // 填充透明度
            strokeStyle: "dashed", // 边界线样式 (虚线)
        });
        
        //团结社区
        var polygon6 = new BMapGL.Polygon([new BMapGL.Point(112.208531, 31.028857), new BMapGL.Point(112.208603, 31.031836), new BMapGL.Point(112.207561, 31.032339), new BMapGL.Point(112.207381, 31.032578), new BMapGL.Point(112.203895, 31.032776), new BMapGL.Point(112.203289, 31.032292), new BMapGL.Point(112.202786, 31.032253), new BMapGL.Point(112.200828, 31.031813), new BMapGL.Point(112.197917, 31.030412), new BMapGL.Point(112.198573, 31.030428), new BMapGL.Point(112.199381, 31.030536), new BMapGL.Point(112.200684, 31.030126), new BMapGL.Point(112.202067, 31.030536), new BMapGL.Point(112.202364, 31.030381), new BMapGL.Point(112.20275, 31.030521), new BMapGL.Point(112.202678, 31.030768), new BMapGL.Point(112.203208, 31.030892), new BMapGL.Point(112.203648, 31.030138), new BMapGL.Point(112.204151, 31.029801)], { 
          strokeColor: "black", // 边界线颜色
            strokeWeight: 2, // 边界线宽度
            strokeOpacity: 0.5, // 边界线透明度
            fillColor: "blue", // 填充颜色
            fillOpacity: 0.1, // 填充透明度
            strokeStyle: "dashed", // 边界线样式 (虚线)
        });


        //龙泉社区
        var polygon7 = new BMapGL.Polygon([new BMapGL.Point(112.198559, 31.02656), new BMapGL.Point(112.197715, 31.026436), new BMapGL.Point(112.196511, 31.025616), new BMapGL.Point(112.195532, 31.025616), new BMapGL.Point(112.19476, 31.02495), new BMapGL.Point(112.194526, 31.025268), new BMapGL.Point(112.194059, 31.025229), new BMapGL.Point(112.193295, 31.024687), new BMapGL.Point(112.192253, 31.024718), new BMapGL.Point(112.192298, 31.025546), new BMapGL.Point(112.190726, 31.025948), new BMapGL.Point(112.190331, 31.027836), new BMapGL.Point(112.190852, 31.029685), new BMapGL.Point(112.193978, 31.030575), new BMapGL.Point(112.197778, 31.030613), new BMapGL.Point(112.198371, 31.030072), new BMapGL.Point(112.197832, 31.028703)], { 
          strokeColor: "black", // 边界线颜色
            strokeWeight: 2, // 边界线宽度
            strokeOpacity: 0.5, // 边界线透明度
            fillColor: "red", // 填充颜色
            fillOpacity: 0.1, // 填充透明度
            strokeStyle: "dashed", // 边界线样式 (虚线)
        });

        //天鹅池社区
        var polygon8 = new BMapGL.Polygon([new BMapGL.Point(112.19944, 31.030405), new BMapGL.Point(112.198685, 31.030296), new BMapGL.Point(112.197877, 31.028687), new BMapGL.Point(112.198847, 31.02649), new BMapGL.Point(112.19776, 31.026397), new BMapGL.Point(112.197778, 31.022939), new BMapGL.Point(112.197832, 31.020773), new BMapGL.Point(112.197428, 31.018367), new BMapGL.Point(112.198847, 31.018096), new BMapGL.Point(112.199835, 31.018421), new BMapGL.Point(112.200464, 31.01839), new BMapGL.Point(112.201003, 31.018088), new BMapGL.Point(112.201757, 31.017933), new BMapGL.Point(112.204497, 31.020076), new BMapGL.Point(112.202287, 31.025214), new BMapGL.Point(112.201731, 31.026622), new BMapGL.Point(112.201057, 31.028084), new BMapGL.Point(112.200581, 31.029592), new BMapGL.Point(112.200428, 31.03008), new BMapGL.Point(112.199961, 31.030319)], { 
          strokeColor: "black", // 边界线颜色
            strokeWeight: 2, // 边界线宽度
            strokeOpacity: 0.5, // 边界线透明度
            fillColor: "yellow", // 填充颜色
            fillOpacity: 0.1, // 填充透明度
            strokeStyle: "dashed", // 边界线样式 (虚线)
        });

        //南门社区
        var polygon9 = new BMapGL.Polygon([new BMapGL.Point(112.207219, 31.032733), new BMapGL.Point(112.205988, 31.032834), new BMapGL.Point(112.20624, 31.03592), new BMapGL.Point(112.209043, 31.035634), new BMapGL.Point(112.214361, 31.034621), new BMapGL.Point(112.211908, 31.034412), new BMapGL.Point(112.208692, 31.033522), new BMapGL.Point(112.208046, 31.032988)], { 
          strokeColor: "black", // 边界线颜色
            strokeWeight: 2, // 边界线宽度
            strokeOpacity: 0.5, // 边界线透明度
            fillColor: "red", // 填充颜色
            fillOpacity: 0.1, // 填充透明度
            strokeStyle: "dashed", // 边界线样式 (虚线)
        });

        //西门社区
        var polygon10 = new BMapGL.Polygon([new BMapGL.Point(112.206159, 31.038442), new BMapGL.Point(112.20571, 31.032857), new BMapGL.Point(112.203752, 31.032888), new BMapGL.Point(112.203662, 31.032547), new BMapGL.Point(112.202782, 31.032284), new BMapGL.Point(112.201829, 31.031743), new BMapGL.Point(112.200338, 31.031727), new BMapGL.Point(112.197877, 31.030938), new BMapGL.Point(112.195541, 31.030459), new BMapGL.Point(112.193098, 31.030691), new BMapGL.Point(112.190879, 31.029322), new BMapGL.Point(112.190259, 31.027836), new BMapGL.Point(112.190547, 31.026258), new BMapGL.Point(112.18804, 31.026707), new BMapGL.Point(112.186756, 31.024393), new BMapGL.Point(112.183594, 31.025268), new BMapGL.Point(112.182812, 31.026297), new BMapGL.Point(112.18221, 31.026444), new BMapGL.Point(112.182974, 31.030219), new BMapGL.Point(112.183675, 31.030892), new BMapGL.Point(112.187277, 31.032253), new BMapGL.Point(112.190601, 31.031929), new BMapGL.Point(112.191184, 31.032137), new BMapGL.Point(112.191939, 31.032865), new BMapGL.Point(112.192604, 31.031062), new BMapGL.Point(112.193349, 31.031867), new BMapGL.Point(112.193331, 31.032315), new BMapGL.Point(112.195766, 31.035201), new BMapGL.Point(112.194382, 31.036771), new BMapGL.Point(112.193664, 31.035835), new BMapGL.Point(112.193691, 31.035046), new BMapGL.Point(112.191723, 31.033406), new BMapGL.Point(112.190618, 31.033104), new BMapGL.Point(112.189316, 31.033692), new BMapGL.Point(112.186693, 31.03329), new BMapGL.Point(112.186244, 31.033453), new BMapGL.Point(112.186334, 31.034555), new BMapGL.Point(112.186064, 31.034601), new BMapGL.Point(112.186307, 31.035669), new BMapGL.Point(112.185786, 31.035034), new BMapGL.Point(112.185741, 31.034547), new BMapGL.Point(112.185112, 31.034462), new BMapGL.Point(112.185166, 31.033217), new BMapGL.Point(112.184321, 31.033139), new BMapGL.Point(112.184528, 31.034903), new BMapGL.Point(112.184878, 31.036883), new BMapGL.Point(112.184142, 31.037193), new BMapGL.Point(112.181932, 31.036845), new BMapGL.Point(112.181528, 31.035854), new BMapGL.Point(112.182677, 31.032412), new BMapGL.Point(112.183396, 31.032373), new BMapGL.Point(112.182399, 31.030842), new BMapGL.Point(112.182094, 31.02883), new BMapGL.Point(112.180692, 31.027623), new BMapGL.Point(112.177144, 31.027306), new BMapGL.Point(112.179839, 31.032861), new BMapGL.Point(112.178357, 31.03679), new BMapGL.Point(112.179381, 31.037742), new BMapGL.Point(112.193933, 31.039482), new BMapGL.Point(112.196107, 31.036953), new BMapGL.Point(112.198757, 31.040101), new BMapGL.Point(112.200715, 31.041231), new BMapGL.Point(112.201775, 31.041207), new BMapGL.Point(112.201353, 31.040264), new BMapGL.Point(112.201497, 31.039351), new BMapGL.Point(112.203168, 31.038624)], { 
          strokeColor: "black", // 边界线颜色
            strokeWeight: 2, // 边界线宽度
            strokeOpacity: 0.5, // 边界线透明度
            fillColor: "green", // 填充颜色
            fillOpacity: 0.1, // 填充透明度
            strokeStyle: "dashed", // 边界线样式 (虚线)
        });

        //特飞所社区
        var polygon11 = new BMapGL.Polygon([new BMapGL.Point(112.194382, 31.036651), new BMapGL.Point(112.19564, 31.035212), new BMapGL.Point(112.193295, 31.03235), new BMapGL.Point(112.193304, 31.031894), new BMapGL.Point(112.192613, 31.031136), new BMapGL.Point(112.191948, 31.032907), new BMapGL.Point(112.191157, 31.032172), new BMapGL.Point(112.190583, 31.031979), new BMapGL.Point(112.187277, 31.032281), new BMapGL.Point(112.183648, 31.030927), new BMapGL.Point(112.182947, 31.030238), new BMapGL.Point(112.182174, 31.026432), new BMapGL.Point(112.181887, 31.026123), new BMapGL.Point(112.181582, 31.026138), new BMapGL.Point(112.181599, 31.027461), new BMapGL.Point(112.181222, 31.027562), new BMapGL.Point(112.18062, 31.027252), new BMapGL.Point(112.180045, 31.027515), new BMapGL.Point(112.18071, 31.027592), new BMapGL.Point(112.18212, 31.028815), new BMapGL.Point(112.182426, 31.030849), new BMapGL.Point(112.183441, 31.032381), new BMapGL.Point(112.182713, 31.032458), new BMapGL.Point(112.181573, 31.035854), new BMapGL.Point(112.181959, 31.036814), new BMapGL.Point(112.184133, 31.037162), new BMapGL.Point(112.184824, 31.036868), new BMapGL.Point(112.184285, 31.033116), new BMapGL.Point(112.185184, 31.033201), new BMapGL.Point(112.185139, 31.034439), new BMapGL.Point(112.185768, 31.034516), new BMapGL.Point(112.185813, 31.035019), new BMapGL.Point(112.186244, 31.03556), new BMapGL.Point(112.186028, 31.034586), new BMapGL.Point(112.186298, 31.034532), new BMapGL.Point(112.186208, 31.033425), new BMapGL.Point(112.186711, 31.03324), new BMapGL.Point(112.189298, 31.03365), new BMapGL.Point(112.190618, 31.033054), new BMapGL.Point(112.19175, 31.033364), new BMapGL.Point(112.193709, 31.035034), new BMapGL.Point(112.193691, 31.035816)], { 
          strokeColor: "black", // 边界线颜色
            strokeWeight: 2, // 边界线宽度
            strokeOpacity: 0.5, // 边界线透明度
            fillColor: "blue", // 填充颜色
            fillOpacity: 0.1, // 填充透明度
            strokeStyle: "dashed", // 边界线样式 (虚线)
        });
        
        //凤台社区
        var polygon12 = new BMapGL.Polygon([new BMapGL.Point(112.20642, 31.038496), new BMapGL.Point(112.206285, 31.035951), new BMapGL.Point(112.209052, 31.035688), new BMapGL.Point(112.210291, 31.035433), new BMapGL.Point(112.211495, 31.03722), new BMapGL.Point(112.211792, 31.037645), new BMapGL.Point(112.210642, 31.038403)], { 
          strokeColor: "black", // 边界线颜色
            strokeWeight: 2, // 边界线宽度
            strokeOpacity: 0.5, // 边界线透明度
            fillColor: "blue", // 填充颜色
            fillOpacity: 0.1, // 填充透明度
            strokeStyle: "dashed", // 边界线样式 (虚线)
        });

        //北门社区
        var polygon13 = new BMapGL.Polygon([new BMapGL.Point(112.214244, 31.034698), new BMapGL.Point(112.215376, 31.039138), new BMapGL.Point(112.215825, 31.039819), new BMapGL.Point(112.215448, 31.040256), new BMapGL.Point(112.215412, 31.040921), new BMapGL.Point(112.214055, 31.041261), new BMapGL.Point(112.211827, 31.037533), new BMapGL.Point(112.21145, 31.036922), new BMapGL.Point(112.211226, 31.036489), new BMapGL.Point(112.210381, 31.035402)], { 
          strokeColor: "black", // 边界线颜色
            strokeWeight: 2, // 边界线宽度
            strokeOpacity: 0.5, // 边界线透明度
            fillColor: "green", // 填充颜色
            fillOpacity: 0.1, // 填充透明度
            strokeStyle: "dashed", // 边界线样式 (虚线)
        });

        //白云楼社区
        var polygon14 = new BMapGL.Polygon([new BMapGL.Point(112.212861, 31.032447), new BMapGL.Point(112.214477, 31.031604), new BMapGL.Point(112.215016, 31.031874), new BMapGL.Point(112.215942, 31.031557), new BMapGL.Point(112.216499, 31.03312), new BMapGL.Point(112.218852, 31.039595), new BMapGL.Point(112.21914, 31.040933), new BMapGL.Point(112.219081, 31.042352), new BMapGL.Point(112.21892, 31.04301), new BMapGL.Point(112.216768, 31.043501), new BMapGL.Point(112.21693, 31.040445), new BMapGL.Point(112.216571, 31.039533), new BMapGL.Point(112.215924, 31.039718), new BMapGL.Point(112.215403, 31.03896), new BMapGL.Point(112.214325, 31.03486), new BMapGL.Point(112.214594, 31.034597)], { 
          strokeColor: "black", // 边界线颜色
            strokeWeight: 2, // 边界线宽度
            strokeOpacity: 0.5, // 边界线透明度
            fillColor: "yellow", // 填充颜色
            fillOpacity: 0.1, // 填充透明度
            strokeStyle: "dashed", // 边界线样式 (虚线)
        });

        //金虾河社区
        var polygon15 = new BMapGL.Polygon([new BMapGL.Point(112.213956, 31.041335), new BMapGL.Point(112.21189, 31.037839), new BMapGL.Point(112.210597, 31.038535), new BMapGL.Point(112.209249, 31.038581), new BMapGL.Point(112.208926, 31.039633), new BMapGL.Point(112.208746, 31.044151), new BMapGL.Point(112.211854, 31.04398), new BMapGL.Point(112.212124, 31.042712), new BMapGL.Point(112.212735, 31.042124)], { 
          strokeColor: "black", // 边界线颜色
            strokeWeight: 2, // 边界线宽度
            strokeOpacity: 0.5, // 边界线透明度
            fillColor: "red", // 填充颜色
            fillOpacity: 0.1, // 填充透明度
            strokeStyle: "dashed", // 边界线样式 (虚线)
        });

        //龙山社区
        var polygon16 = new BMapGL.Polygon([new BMapGL.Point(112.206465, 31.038589), new BMapGL.Point(112.209159, 31.03855), new BMapGL.Point(112.208872, 31.039494), new BMapGL.Point(112.208656, 31.044174), new BMapGL.Point(112.206186, 31.044267)], { 
          strokeColor: "black", // 边界线颜色
            strokeWeight: 2, // 边界线宽度
            strokeOpacity: 0.5, // 边界线透明度
            fillColor: "green", // 填充颜色
            fillOpacity: 0.1, // 填充透明度
            strokeStyle: "dashed", // 边界线样式 (虚线)
        });

        //白龙社区
        var polygon17 = new BMapGL.Polygon([new BMapGL.Point(112.205809, 31.045156), new BMapGL.Point(112.20615, 31.038604), new BMapGL.Point(112.203621, 31.038678), new BMapGL.Point(112.202611, 31.038976), new BMapGL.Point(112.201623, 31.039517), new BMapGL.Point(112.201457, 31.040109), new BMapGL.Point(112.202081, 31.041165), new BMapGL.Point(112.20182, 31.041621), new BMapGL.Point(112.201012, 31.041714), new BMapGL.Point(112.200329, 31.041157), new BMapGL.Point(112.198065, 31.039803), new BMapGL.Point(112.196646, 31.037583), new BMapGL.Point(112.196197, 31.037351), new BMapGL.Point(112.195676, 31.037537), new BMapGL.Point(112.194149, 31.039424), new BMapGL.Point(112.192568, 31.043524), new BMapGL.Point(112.197832, 31.044004), new BMapGL.Point(112.198748, 31.043926), new BMapGL.Point(112.199179, 31.04504), new BMapGL.Point(112.202108, 31.044901)], { 
          strokeColor: "black", // 边界线颜色
            strokeWeight: 2, // 边界线宽度
            strokeOpacity: 0.5, // 边界线透明度
            fillColor: "yellow", // 填充颜色
            fillOpacity: 0.1, // 填充透明度
            strokeStyle: "dashed", // 边界线样式 (虚线)
        });

        //沿河社区
        var polygon18 = new BMapGL.Polygon([new BMapGL.Point(112.211926, 31.044197), new BMapGL.Point(112.206141, 31.044429), new BMapGL.Point(112.205944, 31.048884), new BMapGL.Point(112.208513, 31.049085), new BMapGL.Point(112.212259, 31.049224),new BMapGL.Point(112.212142, 31.047678), new BMapGL.Point(112.212905, 31.045875),new BMapGL.Point(112.212214, 31.045001)], { 
          strokeColor: "black", // 边界线颜色
            strokeWeight: 2, // 边界线宽度
            strokeOpacity: 0.5, // 边界线透明度
            fillColor: "yellow", // 填充颜色
            fillOpacity: 0.1, // 填充透明度
            strokeStyle: "dashed", // 边界线样式 (虚线)
        });

        //金象社区
        var polygon19 = new BMapGL.Polygon([new BMapGL.Point(112.213995, 31.041355), new BMapGL.Point(112.212791, 31.042171), new BMapGL.Point(112.212252, 31.042682), new BMapGL.Point(112.212194, 31.042867), new BMapGL.Point(112.212190, 31.044445), new BMapGL.Point(112.212207, 31.044484), new BMapGL.Point(112.212207, 31.044527), new BMapGL.Point(112.213205, 31.045617), new BMapGL.Point(112.212935, 31.046395), new BMapGL.Point(112.212657, 31.046793), new BMapGL.Point(112.212369, 31.046979), new BMapGL.Point(112.212207, 31.047358), new BMapGL.Point(112.212075, 31.047864), new BMapGL.Point(112.211956, 31.048201), new BMapGL.Point(112.212158, 31.048684), new BMapGL.Point(112.212463, 31.049229), new BMapGL.Point(112.215504, 31.049318), new BMapGL.Point(112.215284, 31.047574), new BMapGL.Point(112.215037, 31.045861), new BMapGL.Point(112.214669, 31.043022), new BMapGL.Point(112.214543, 31.042396)], { 
        strokeColor: "black", // 边界线颜色
            strokeWeight: 2, // 边界线宽度
            strokeOpacity: 0.5, // 边界线透明度
            fillColor: "green", // 填充颜色
            fillOpacity: 0.1, // 填充透明度
            strokeStyle: "dashed", // 边界线样式 (虚线)
        });


        //大桥社区
        var polygon20 = new BMapGL.Polygon([new BMapGL.Point(112.2141, 31.041312), new BMapGL.Point(112.214459, 31.041281), new BMapGL.Point(112.214666, 31.041188), new BMapGL.Point(112.215475, 31.041072), new BMapGL.Point(112.215564, 31.041049), new BMapGL.Point(112.215582, 31.040933), new BMapGL.Point(112.2156, 31.040252), new BMapGL.Point(112.215776, 31.03997), new BMapGL.Point(112.215973, 31.039834), new BMapGL.Point(112.216395, 31.039683), new BMapGL.Point(112.216719, 31.040612), new BMapGL.Point(112.216674, 31.042766), new BMapGL.Point(112.216521, 31.043609), new BMapGL.Point(112.217819, 31.043126), new BMapGL.Point(112.218542, 31.04301), new BMapGL.Point(112.218794, 31.043052), new BMapGL.Point(112.218408, 31.047244), new BMapGL.Point(112.215425, 31.047569), new BMapGL.Point(112.214976, 31.044077), new BMapGL.Point(112.214765, 31.042646)], { 
          strokeColor: "black", // 边界线颜色
            strokeWeight: 2, // 边界线宽度
            strokeOpacity: 0.5, // 边界线透明度
            fillColor: "blue", // 填充颜色
            fillOpacity: 0.1, // 填充透明度
            strokeStyle: "dashed", // 边界线样式 (虚线)
        });


        //象山社区
        var polygon21 = new BMapGL.Polygon([new BMapGL.Point(112.20536, 31.055234), new BMapGL.Point(112.20244, 31.055149), new BMapGL.Point(112.201946, 31.055242), new BMapGL.Point(112.201677, 31.054847), new BMapGL.Point(112.200958, 31.054716), new BMapGL.Point(112.200419, 31.054515), new BMapGL.Point(112.198443, 31.055087), new BMapGL.Point(112.196071, 31.055497), new BMapGL.Point(112.193772, 31.055288), new BMapGL.Point(112.191678, 31.053788), new BMapGL.Point(112.191256, 31.050918), new BMapGL.Point(112.191741, 31.048304), new BMapGL.Point(112.192478, 31.046432), new BMapGL.Point(112.196107, 31.045241), new BMapGL.Point(112.201138, 31.044932), new BMapGL.Point(112.203329, 31.044684), new BMapGL.Point(112.205988, 31.04439), new BMapGL.Point(112.205791, 31.048907)], { 
          strokeColor: "black", // 边界线颜色
            strokeWeight: 2, // 边界线宽度
            strokeOpacity: 0.5, // 边界线透明度
            fillColor: "green", // 填充颜色
            fillOpacity: 0.1, // 填充透明度
            strokeStyle: "dashed", // 边界线样式 (虚线)
        });
        
        //青山社区
        var polygon22 = new BMapGL.Polygon([new BMapGL.Point(112.205818, 31.048907), new BMapGL.Point(112.208396, 31.049116), new BMapGL.Point(112.212384, 31.049263), new BMapGL.Point(112.210785, 31.050586), new BMapGL.Point(112.210435, 31.051305), new BMapGL.Point(112.211136, 31.052318), new BMapGL.Point(112.210651, 31.053223), new BMapGL.Point(112.21057, 31.054097), new BMapGL.Point(112.21039, 31.054561), new BMapGL.Point(112.208252, 31.054499), new BMapGL.Point(112.205643, 31.054522)], { 
          strokeColor: "black", // 边界线颜色
            strokeWeight: 2, // 边界线宽度
            strokeOpacity: 0.5, // 边界线透明度
            fillColor: "red", // 填充颜色
            fillOpacity: 0.1, // 填充透明度
            strokeStyle: "dashed", // 边界线样式 (虚线)
        });


        //浏河社区
        var polygon23 = new BMapGL.Polygon([new BMapGL.Point(112.216499, 31.055845), new BMapGL.Point(112.215564, 31.049379), new BMapGL.Point(112.212564, 31.049255), new BMapGL.Point(112.211468, 31.050377), new BMapGL.Point(112.210839, 31.051019), new BMapGL.Point(112.210938, 31.051568), new BMapGL.Point(112.211531, 31.052287), new BMapGL.Point(112.211369, 31.052697), new BMapGL.Point(112.211944, 31.052751), new BMapGL.Point(112.21119, 31.055056), new BMapGL.Point(112.21083, 31.057198), new BMapGL.Point(112.210866, 31.057624), new BMapGL.Point(112.211342, 31.057117), new BMapGL.Point(112.212106, 31.056661), new BMapGL.Point(112.214397, 31.056189)], { 
          strokeColor: "black", // 边界线颜色
            strokeWeight: 2, // 边界线宽度
            strokeOpacity: 0.5, // 边界线透明度
            fillColor: "blue", // 填充颜色
            fillOpacity: 0.1, // 填充透明度
            strokeStyle: "dashed", // 边界线样式 (虚线)
        });

        //竹皮河社区
        var polygon24 = new BMapGL.Polygon([new BMapGL.Point(112.206186, 31.059665), new BMapGL.Point(112.208144, 31.058877), new BMapGL.Point(112.209761, 31.058413), new BMapGL.Point(112.210767, 31.057655), new BMapGL.Point(112.210929, 31.056278), new BMapGL.Point(112.211181, 31.054994), new BMapGL.Point(112.211378, 31.054159), new BMapGL.Point(112.211863, 31.052767), new BMapGL.Point(112.211297, 31.052767), new BMapGL.Point(112.210893, 31.053378), new BMapGL.Point(112.210902, 31.05429), new BMapGL.Point(112.210776, 31.054577), new BMapGL.Point(112.210309, 31.054538), new BMapGL.Point(112.209258, 31.05453), new BMapGL.Point(112.208809, 31.054546), new BMapGL.Point(112.208288, 31.054507), new BMapGL.Point(112.205611, 31.054565), new BMapGL.Point(112.205575, 31.057369), new BMapGL.Point(112.205782, 31.058575)], { 
          strokeColor: "black", // 边界线颜色
          strokeWeight: 2, // 边界线宽度
          strokeOpacity: 0.5, // 边界线透明度
          fillColor: "yellow", // 填充颜色
          fillOpacity: 0.1, // 填充透明度
          strokeStyle: "dashed", // 边界线样式 (虚线)
        });

        //泉口社区
        var polygon25 = new BMapGL.Polygon([new BMapGL.Point(112.211432, 31.063037), new BMapGL.Point(112.208073, 31.060949), new BMapGL.Point(112.206276, 31.059665), new BMapGL.Point(112.207372, 31.059155), new BMapGL.Point(112.208091, 31.058985), new BMapGL.Point(112.208899, 31.058815), new BMapGL.Point(112.209276, 31.058737), new BMapGL.Point(112.210013, 31.058366), new BMapGL.Point(112.210758, 31.057778), new BMapGL.Point(112.211477, 31.057137), new BMapGL.Point(112.21207, 31.056754), new BMapGL.Point(112.212519, 31.056626), new BMapGL.Point(112.213907, 31.056363), new BMapGL.Point(112.216359, 31.055876), new BMapGL.Point(112.216413, 31.055911), new BMapGL.Point(112.216818, 31.061815), new BMapGL.Point(112.211338, 31.061908)], { 
          strokeColor: "black", // 边界线颜色
            strokeWeight: 2, // 边界线宽度
            strokeOpacity: 0.5, // 边界线透明度
            fillColor: "green", // 填充颜色
            fillOpacity: 0.1, // 填充透明度
            strokeStyle: "dashed", // 边界线样式 (虚线)
        });

        //苏畈桥社区
        var polygon26 = new BMapGL.Polygon([new BMapGL.Point(112.205346, 31.055277), new BMapGL.Point(112.202409, 31.055207), new BMapGL.Point(112.201987, 31.055304), new BMapGL.Point(112.20182, 31.055307), new BMapGL.Point(112.201232, 31.054727), new BMapGL.Point(112.200962, 31.054727), new BMapGL.Point(112.200397, 31.054553), new BMapGL.Point(112.19913, 31.054971), new BMapGL.Point(112.198321, 31.055118), new BMapGL.Point(112.196053, 31.055524), new BMapGL.Point(112.191018, 31.05656), new BMapGL.Point(112.192132, 31.058231), new BMapGL.Point(112.19356, 31.058401), new BMapGL.Point(112.195402, 31.05895), new BMapGL.Point(112.195905, 31.060311), new BMapGL.Point(112.195636, 31.060996), new BMapGL.Point(112.194629, 31.061924), new BMapGL.Point(112.195622, 31.062875), new BMapGL.Point(112.195685, 31.063633), new BMapGL.Point(112.195595, 31.064607), new BMapGL.Point(112.198685, 31.063447), new BMapGL.Point(112.201111, 31.062272), new BMapGL.Point(112.202782, 31.061483), new BMapGL.Point(112.206105, 31.059627), new BMapGL.Point(112.205683, 31.058691), new BMapGL.Point(112.20536, 31.057013)], { 
          strokeColor: "black", // 边界线颜色
          strokeWeight: 2, // 边界线宽度
          strokeOpacity: 0.5, // 边界线透明度
          fillColor: "red", // 填充颜色
          fillOpacity: 0.1, // 填充透明度
          strokeStyle: "dashed", // 边界线样式 (虚线)
        });
        
        //车站社区
        var polygon27 = new BMapGL.Polygon([new BMapGL.Point(112.217568, 31.047376), new BMapGL.Point(112.215407, 31.047616), new BMapGL.Point(112.215672, 31.049368), new BMapGL.Point(112.216054, 31.051935), new BMapGL.Point(112.216602, 31.05605), new BMapGL.Point(112.216952, 31.061904), new BMapGL.Point(112.219108, 31.061788), new BMapGL.Point(112.218821, 31.056761), new BMapGL.Point(112.218488, 31.05127),new BMapGL.Point(112.218331, 31.048641), new BMapGL.Point(112.21839, 31.047256)], { 
          strokeColor: "black", // 边界线颜色
          strokeWeight: 2, // 边界线宽度
          strokeOpacity: 0.5, // 边界线透明度
          fillColor: "yellow", // 填充颜色
          fillOpacity: 0.1, // 填充透明度
          strokeStyle: "dashed", // 边界线样式 (虚线)
        });
           
        //凯龙社区
        var polygon28 = new BMapGL.Polygon([new BMapGL.Point(112.19458, 31.062125), new BMapGL.Point(112.195442, 31.062883), new BMapGL.Point(112.195568, 31.064599), new BMapGL.Point(112.195595, 31.064669), new BMapGL.Point(112.194284, 31.065725), new BMapGL.Point(112.19546, 31.066993), new BMapGL.Point(112.196952, 31.068508), new BMapGL.Point(112.197275, 31.0699), new BMapGL.Point(112.197176, 31.070867), new BMapGL.Point(112.195047, 31.074733), new BMapGL.Point(112.192855, 31.077177), new BMapGL.Point(112.184555, 31.072908), new BMapGL.Point(112.188076, 31.065516), new BMapGL.Point(112.190124, 31.064186)], { 
          strokeColor: "black", // 边界线颜色
          strokeWeight: 2, // 边界线宽度
          strokeOpacity: 0.5, // 边界线透明度
          fillColor: "blue", // 填充颜色
          fillOpacity: 0.1, // 填充透明度
          strokeStyle: "dashed", // 边界线样式 (虚线)
        }); 
          
        //葛洲坝社区
        var polygon29 = new BMapGL.Polygon([new BMapGL.Point(112.202925, 31.068675), new BMapGL.Point(112.212555, 31.069765), new BMapGL.Point(112.21295, 31.069734), new BMapGL.Point(112.21313, 31.067708), new BMapGL.Point(112.213094, 31.066463), new BMapGL.Point(112.213094, 31.065899), new BMapGL.Point(112.211297, 31.065883), new BMapGL.Point(112.210471, 31.065844), new BMapGL.Point(112.20982, 31.065531), new BMapGL.Point(112.209788, 31.065168), new BMapGL.Point(112.20995, 31.064549), new BMapGL.Point(112.210049, 31.06436), new BMapGL.Point(112.210139, 31.063679), new BMapGL.Point(112.209981, 31.063339), new BMapGL.Point(112.209838, 31.063262), new BMapGL.Point(112.209407, 31.063227), new BMapGL.Point(112.209191, 31.063872), new BMapGL.Point(112.208706, 31.063892), new BMapGL.Point(112.208589, 31.063668), new BMapGL.Point(112.208585, 31.063405), new BMapGL.Point(112.208284, 31.063215), new BMapGL.Point(112.208306, 31.063091), new BMapGL.Point(112.208472, 31.062825), new BMapGL.Point(112.208409, 31.062523), new BMapGL.Point(112.208059, 31.061928), new BMapGL.Point(112.206447, 31.061154), new BMapGL.Point(112.205822, 31.061007), new BMapGL.Point(112.205301, 31.061096), new BMapGL.Point(112.204214, 31.061839), new BMapGL.Point(112.203891, 31.061877), new BMapGL.Point(112.203783, 31.061742), new BMapGL.Point(112.203797, 31.06156), new BMapGL.Point(112.203568, 31.061166), new BMapGL.Point(112.202791, 31.061634), new BMapGL.Point(112.202665, 31.062183), new BMapGL.Point(112.202269, 31.062345), new BMapGL.Point(112.201407, 31.062446), new BMapGL.Point(112.201156, 31.0625), new BMapGL.Point(112.200653, 31.062755), new BMapGL.Point(112.199943, 31.06332), new BMapGL.Point(112.199377, 31.06376), new BMapGL.Point(112.197589, 31.064248), new BMapGL.Point(112.196287, 31.065152), new BMapGL.Point(112.197464, 31.066366)], { 
          strokeColor: "black", // 边界线颜色
          strokeWeight: 2, // 边界线宽度
          strokeOpacity: 0.5, // 边界线透明度
          fillColor: "yellow", // 填充颜色
          fillOpacity: 0.1, // 填充透明度
          strokeStyle: "dashed", // 边界线样式 (虚线)
        });  
           
        //金龙泉社区
        var polygon30 = new BMapGL.Polygon([new BMapGL.Point(112.203967, 31.061576), new BMapGL.Point(112.203662, 31.061065), new BMapGL.Point(112.206114, 31.059774), new BMapGL.Point(112.206559, 31.060157), new BMapGL.Point(112.211504, 31.063358), new BMapGL.Point(112.211504, 31.06303), new BMapGL.Point(112.211392, 31.061951), new BMapGL.Point(112.213965, 31.061897), new BMapGL.Point(112.216795, 31.06185), new BMapGL.Point(112.219095, 31.061765), new BMapGL.Point(112.219346, 31.065848), new BMapGL.Point(112.219463, 31.068385), new BMapGL.Point(112.219364, 31.069491), new BMapGL.Point(112.219221, 31.070016), new BMapGL.Point(112.223263, 31.070457), new BMapGL.Point(112.222922, 31.073643), new BMapGL.Point(112.222922, 31.073798), new BMapGL.Point(112.221965, 31.073666), new BMapGL.Point(112.21945, 31.073415), new BMapGL.Point(112.218327, 31.073214), new BMapGL.Point(112.218857, 31.071675), new BMapGL.Point(112.219189, 31.070306), new BMapGL.Point(112.215596, 31.07009), new BMapGL.Point(112.213727, 31.069819), new BMapGL.Point(112.212973, 31.069719), new BMapGL.Point(112.213188, 31.067724), new BMapGL.Point(112.213152, 31.066479), new BMapGL.Point(112.213152, 31.065883), new BMapGL.Point(112.211383, 31.065891), new BMapGL.Point(112.210467, 31.065844), new BMapGL.Point(112.210085, 31.065524), new BMapGL.Point(112.210035, 31.065322), new BMapGL.Point(112.210233, 31.064541), new BMapGL.Point(112.210345, 31.063911), new BMapGL.Point(112.210278, 31.063486), new BMapGL.Point(112.210116, 31.063122), new BMapGL.Point(112.209887, 31.063018), new BMapGL.Point(112.20929, 31.062917), new BMapGL.Point(112.208881, 31.062844), new BMapGL.Point(112.208567, 31.062376), new BMapGL.Point(112.208382, 31.06202), new BMapGL.Point(112.20823, 31.061819), new BMapGL.Point(112.207664, 31.061491), new BMapGL.Point(112.206541, 31.06098), new BMapGL.Point(112.205858, 31.060814), new BMapGL.Point(112.205441, 31.060841), new BMapGL.Point(112.20505, 31.061038), new BMapGL.Point(112.204565, 31.061355), new BMapGL.Point(112.204232, 31.061576)], { 
            strokeColor: "black", // 边界线颜色
          strokeWeight: 2, // 边界线宽度
          strokeOpacity: 0.5, // 边界线透明度
          fillColor: "blue", // 填充颜色
          fillOpacity: 0.1, // 填充透明度
          strokeStyle: "dashed", // 边界线样式 (虚线)
        });


        this.map.addOverlay(polygon); 
        this.map.addOverlay(polygon2);
        this.map.addOverlay(polygon3); 
        this.map.addOverlay(polygon4); 
        this.map.addOverlay(polygon5); 
        this.map.addOverlay(polygon6);
        this.map.addOverlay(polygon7);
        this.map.addOverlay(polygon8); 
        this.map.addOverlay(polygon9); 
        this.map.addOverlay(polygon10); 
        this.map.addOverlay(polygon11);
        this.map.addOverlay(polygon12); 
        this.map.addOverlay(polygon13);
        this.map.addOverlay(polygon14); 
        this.map.addOverlay(polygon15);
        // this.map.addOverlay(polygon16); 
        // this.map.addOverlay(polygon17);
        // this.map.addOverlay(polygon18);

        // this.map.addOverlay(polygon19); 
        // this.map.addOverlay(polygon20);
        // this.map.addOverlay(polygon21); 
        // this.map.addOverlay(polygon22); 
        // this.map.addOverlay(polygon23); 
        // this.map.addOverlay(polygon24);
        // this.map.addOverlay(polygon25);
        // this.map.addOverlay(polygon26); 
        // this.map.addOverlay(polygon27); 
        // this.map.addOverlay(polygon28); 
        // this.map.addOverlay(polygon29);
        // this.map.addOverlay(polygon30); 
        
        // //地图样式
        // map.setMapStyleV2({     
        //   styleId: '012958c7835177dac34edf370a910abf'
        // });


        // 添加3D控件
        var navi3DCtrl = new BMapGL.NavigationControl3D(); 
        this.map.addControl(navi3DCtrl);
        var opts1 = {
                offset: new BMapGL.Size(5, 5)
            }
        // 添加3D地球控件
        this.map.addControl(new BMapGL.MapTypeControl(opts1)) //右上，地图模式

        // 创建小车图标
        var myIcon = new BMapGL.Icon(require("../assets/map-other.png"), new BMapGL.Size(30, 50));


        var data_info = [
          [112.20943,31.025503,"国网充电桩   地址：湖北省荆门市东宝区白云大道荆门供电公司营销部停车场<h4><a target='_blank' href='https://lbsyun.baidu.com/index.php?title=jspopularGL/guide/event' style='color:blue;'>到这去</a></h4>"],
          [112.2085,31.044111,"星星充电桩   地址：湖北省荆门市东宝区象山一路银泰城地面停车场<h4><a target='_blank' href='https://lbsyun.baidu.com/index.php?title=jspopularGL/guide/event' style='color:blue;'>到这去</a></h4>"],
          [112.210858,31.048335,"特来电充电桩   地址：湖北省荆门市东宝区象山二路浏河湾停车场<h4><a target='_blank' href='https://lbsyun.baidu.com/index.php?title=jspopularGL/guide/event' style='color:blue;'>到这去</a></h4>"],
          [112.20152,31.054456,"特来电充电桩   地址：湖北省荆门市东宝区青山路新晨御苑小区停车场<h4><a target='_blank' href='https://lbsyun.baidu.com/index.php?title=jspopularGL/guide/event' style='color:blue;'>到这去</a></h4>"],
          [112.221238,31.054503,"国网充电桩   地址：湖北省荆门市掇刀区九渊路银河星座停车场<h4><a target='_blank' href='https://lbsyun.baidu.com/index.php?title=jspopularGL/guide/event' style='color:blue;'>到这去</a></h4>"],
          [112.206173,31.060102,"国网充电桩   地址：湖北省荆门市东宝区泉口一路路灯管理局<h4><a target='_blank' href='https://lbsyun.baidu.com/index.php?title=jspopularGL/guide/event' style='color:blue;'>到这去</a></h4>"],
          [112.236815,31.07885,"国网充电桩   地址：湖北省荆门市东宝区泉口街道新桥实业有限公司<h4><a target='_blank' href='https://lbsyun.baidu.com/index.php?title=jspopularGL/guide/event' style='color:blue;'>到这去</a></h4>"],
          [112.248008,31.073059,"国网充电桩   地址：湖北省荆门市东宝区湖北兆泰电气公司<h4><a target='_blank' href='https://lbsyun.baidu.com/index.php?title=jspopularGL/guide/event' style='color:blue;'>到这去</a></h4>"],
          [112.209892,31.086505,"国网充电桩   地址：湖北省荆门市东宝区子陵铺镇长宁太和小区<h4><a target='_blank' href='https://lbsyun.baidu.com/index.php?title=jspopularGL/guide/event' style='color:blue;'>到这去</a></h4>"],
          [112.245429,31.051239,"国网充电桩   地址：湖北省荆门市掇刀区月亮湖路白庙充电站<h4><a target='_blank' href='https://lbsyun.baidu.com/index.php?title=jspopularGL/guide/event' style='color:blue;'>到这去</a></h4>"],
          [112.257467,31.049615,"国网充电桩   地址：湖北省荆门市东宝区城东营业厅<h4><a target='_blank' href='https://lbsyun.baidu.com/index.php?title=jspopularGL/guide/event' style='color:blue;'>到这去</a></h4>"],
        ];
  
        var opts = {
          min_width : 250,     // 信息窗口最小宽度
          min_height: 80,     // 信息窗口高度
          title : "充电桩信息" , // 信息窗口标题
          enableMessage:true//设置允许信息窗发送短息
        };   
  
        for(var i=0;i<data_info.length;i++){
          var marker = new BMapGL.Marker(new BMapGL.Point(data_info[i][0],data_info[i][1]), {icon: myIcon});  // 创建标注
          var content = data_info[i][2];
          this.map.addOverlay(marker); //将标注添加到地图
          addClickHandler(content,marker);
        }
  

        function addClickHandler(content,marker){
          marker.addEventListener("click",function(e){openInfo(content,e)});
        }
        function openInfo(content,e){
          var p = e.target;
          var point = new BMapGL.Point(p.getPosition().lng, p.getPosition().lat);
          var infoWindow = new BMapGL.InfoWindow(content,opts); //创建信息窗口 
          this.map.openInfoWindow(infoWindow,point); //开启信息窗口
        }
    }
  }
</script>

<style>
  .image-class{
    position: fixed;
    right: 0;
    bottom: 0;
    width: 100px;
    height: 100px;
    }
</style>
