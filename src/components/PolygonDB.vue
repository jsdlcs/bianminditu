
<!-- PolygonDB.vue 东宝区社区范围图-->
<template>
    <div></div>
</template>
  
<script>
  export default {
    props: ['mapInstance'],
    mounted() {
    },
    watch: {
      mapInstance: {
        immediate: true,
        handler(newMapInstance) {
          if (newMapInstance) {
            var polygon = new BMapGL.Polygon(
              [
                new BMapGL.Point(112.205413, 31.029443),
                new BMapGL.Point(112.209743, 31.02846),
                new BMapGL.Point(112.20942, 31.027679),
                new BMapGL.Point(112.209159, 31.026712),
                new BMapGL.Point(112.209052, 31.025397),
                new BMapGL.Point(112.208539, 31.014379),
                new BMapGL.Point(112.208773, 31.013783),
                new BMapGL.Point(112.206689, 31.012925),
                new BMapGL.Point(112.206797, 31.016801),
                new BMapGL.Point(112.205934, 31.019091),
                new BMapGL.Point(112.20438, 31.022611)
              ],
              {
                strokeColor: "black",
                strokeWeight: 2,
                strokeOpacity: 0.5,
                fillColor: "red",
                fillOpacity: 0.1,
                strokeStyle: "dashed"
              }
            );


              //2东宝山社区
            var polygon2 = new BMapGL.Polygon(
            [
                new BMapGL.Point(112.210278,31.024089),
                new BMapGL.Point(112.211499,31.026224),
                new BMapGL.Point(112.21587, 31.031441), 
                new BMapGL.Point(112.214972, 31.031689), 
                new BMapGL.Point(112.214468, 31.031457), 
                new BMapGL.Point(112.212807, 31.032346),
                new BMapGL.Point(112.210183,31.029141),
                new BMapGL.Point(112.209465,31.02716),
                new BMapGL.Point(112.20933,31.026433),
                new BMapGL.Point(112.208998,31.022464),
                new BMapGL.Point(112.210085,31.022372),
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
            [
                new BMapGL.Point(112.208555,31.02873),
                new BMapGL.Point(112.208681,31.031902),
                new BMapGL.Point(112.207513,31.032475),
                new BMapGL.Point(112.207406,31.032753),
                new BMapGL.Point(112.208142,31.033016),
                new BMapGL.Point(112.208681,31.03348),
                new BMapGL.Point(112.21161,31.034316),
                new BMapGL.Point(112.214035,31.034316),
                new BMapGL.Point(112.210406,31.029937),
                new BMapGL.Point(112.209746,31.028502),
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
            [
            new BMapGL.Point(112.208924,31.022421),
                new BMapGL.Point(112.210141,31.022363),
                new BMapGL.Point(112.209813,31.017957),
                new BMapGL.Point(112.210136,31.016363),
                new BMapGL.Point(112.212005,31.016518),
                new BMapGL.Point(112.212706,31.015249),
                new BMapGL.Point(112.213424,31.01528),
                new BMapGL.Point(112.21382,31.016146),
                new BMapGL.Point(112.214969,31.015806),
                new BMapGL.Point(112.215454,31.014583),
                new BMapGL.Point(112.214413,31.011906),
                new BMapGL.Point(112.213676,31.011473),
                new BMapGL.Point(112.210873,31.011674),
                new BMapGL.Point(112.208717,31.014135),
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


            //添加社区区域图形
            newMapInstance.addOverlay(polygon);
            newMapInstance.addOverlay(polygon2);
            newMapInstance.addOverlay(polygon3); 
            newMapInstance.addOverlay(polygon4); 
            newMapInstance.addOverlay(polygon5); 
            newMapInstance.addOverlay(polygon6);
            newMapInstance.addOverlay(polygon7);
            newMapInstance.addOverlay(polygon8); 
            newMapInstance.addOverlay(polygon9); 
            newMapInstance.addOverlay(polygon10); 
            newMapInstance.addOverlay(polygon11);
            newMapInstance.addOverlay(polygon12); 
            newMapInstance.addOverlay(polygon13);
            newMapInstance.addOverlay(polygon14); 
            newMapInstance.addOverlay(polygon15);
            newMapInstance.addOverlay(polygon16); 
            newMapInstance.addOverlay(polygon17);
            newMapInstance.addOverlay(polygon18);
          }
        }
      }
    }
  };
</script>
  