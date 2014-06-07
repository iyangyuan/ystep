ystep 流程、步骤插件
=============
  
相关链接
-------------
  
[ystep在线演示](http://www.kpdown.com/ystep/ "ystep在线演示-开辟软件站赞助")
  
简介
-------------
  
`ystep`是一款`jQuery`流程、步骤插件。在网站设计中，经常会用到步骤指示，做某件事一共需要几个步骤，现在正处于哪个步骤，对用户而言是非常有帮助的，不仅能让用户思路清晰，也能带给用户一种无形的激励。  
鉴于目前并无经典易用的类似插件，`ystep`就此诞生。  
  
特点
-------------
  
设计简洁，方便易用。  
体积小巧，便于集成。  
代码稳重，安全可靠。  
自由定制，步骤无限制。
兼容性强，`Webkit`(谷歌)、`Gecko`(火狐)内核系列全兼容，`IE`系列除了极品`IE6`，其它全兼容。  
  
使用说明
-------------
  
引入ystep的`js`、`css`文件  
  
    <!-- 引入ystep样式 -->
    <link rel="stylesheet" href="css/ystep.css">
    <!-- 引入jquery -->
    <script src="js/jquery.min.js"></script>
    <!-- 引入ystep插件 -->
    <script src="js/ystep.js"></script>
  
加载ystep  
  
    //根据jQuery选择器找到需要加载ystep的容器
    //loadStep 方法可以初始化ystep
    $(".ystep1").loadStep({
      //ystep的外观大小
      //可选值：small,large
      size: "small",
      //ystep配色方案
      //可选值：green,blue
      color: "green",
      //ystep中包含的步骤
      steps: [{
        //步骤名称
        title: "发起",
        //步骤内容(鼠标移动到本步骤节点时，会提示该内容)
        content: "实名用户/公益组织发起项目"
      },{
        title: "审核",
        content: "乐捐平台工作人员审核项目"
      }]
    });
  
操作ystep  
  
    //所有跳转操作，仅需在加载ystep的容器上调用即可
    //跳转到下一个步骤
    $(".ystep1").nextStep();
    //跳转到上一个步骤
    $(".ystep1").prevStep();
    //跳转到指定步骤
    $(".ystep1").setStep(2);
    //获取当前在第几步
    $(".ystep1").getStep();
  
完整示例
-------------
  
    <!DOCTYPE html>
    <html>
      <head>
        <title>ystep流程、步骤插件 —— Powerd By YangYuan</title>
        <meta name="keywords" content="ystep,jQuery流程、步骤插件"/>
        <meta name="description" content="ystep,jQuery流程、步骤插件"/>
        <meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <!-- 引入ystep样式 -->
        <link rel="stylesheet" href="css/ystep.css">
      </head>
      <body>
      
      <br><br><br><br><br>
      <!-- ystep容器 -->
      <div class="ystep1"></div>
      
      <!-- 引入jquery -->
      <script src="js/jquery.min.js"></script>
      <!-- 引入ystep插件 -->
      <script src="js/ystep.js"></script>
      <script>
        //根据jQuery选择器找到需要加载ystep的容器
        //loadStep 方法可以初始化ystep
        $(".ystep1").loadStep({
          //ystep的外观大小
          //可选值：small,large
          size: "small",
          //ystep配色方案
          //可选值：green,blue
          color: "green",
          //ystep中包含的步骤
          steps: [{
            //步骤名称
            title: "发起",
            //步骤内容(鼠标移动到本步骤节点时，会提示该内容)
            content: "实名用户/公益组织发起项目"
          },{
            title: "审核",
            content: "乐捐平台工作人员审核项目"
          },{
            title: "募款",
            content: "乐捐项目上线接受公众募款"
          },{
            title: "执行",
            content: "项目执行者线下开展救护行动"
          },{
            title: "结项",
            content: "项目执行者公示善款使用报告"
          }]
        });
        
        //跳转到下一个步骤
        //$(".ystep1").nextStep();
        //跳转到上一个步骤
        //$(".ystep1").prevStep();
        //跳转到指定步骤
        //$(".ystep1").setStep(2);
        //获取当前在第几步
        //$(".ystep1").getStep();
        
      </script>
      </body>
    </html>
  