# Yanpf88880000.github.io
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8">
    <title>谭娅琦大王</title>
    <!-- 引入样式 -->
    <!-- <link rel="stylesheet" href="https://unpkg.com/element-ui/lib/theme-chalk/index.css"> -->
    <!-- import Vue before Element -->
    <!-- <script src="https://unpkg.com/vue@2/dist/vue.js"></script> -->
    <!-- 引入组件库 -->
    <!-- <script src="https://unpkg.com/element-ui/lib/index.js"></script> -->
    <link rel="stylesheet"
    href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css"/>
    <style>
      .logo {
        width: 120px;
        height: 120px;
        background-image: url("https://pb.nichi.co/bag-reopen-gas");
        background-repeat: no-repeat;
        background-size: contain;
        position: absolute;
        top: 25%;
        right: -5%;
        transform: translate(-50%, -50%);
        animation: spin 4s linear infinite;
        border-radius: 50%;
        overflow: hidden;

		}

		@keyframes spin {
			from {
				transform: translate(-50%, -50%) rotate(0deg);
			}
			to {
				transform: translate(-50%, -50%) rotate(360deg);
			}
		}
      body {
        background-color: #f5f5f5;
        /* background-color: #000; */
        font-family: Arial, sans-serif;
        text-align: center;
      }

      h1 {
        margin-top: 50px;
        color: #555;
      }

      .container {
        position: relative;
        margin: 50px auto;
        max-width: 600px;
        background-color: #fff;
        box-shadow: 0px 0px 10px 0px rgba(0,0,0,0.2);
        padding: 30px;
        border-radius: 5px;
        transition: all 0.3s ease-in-out;
      }

      .container:hover {
        box-shadow: 0px 0px 20px 0px rgba(0,0,0,0.3);
      }

      label {
        font-size: 18px;
        display: block;
        margin-bottom: 10px;
        color: #666;
        text-align: left;
      }

      input[type="datetime-local"] {
        padding: 8px;
        border-radius: 5px;
        border: none;
        box-shadow: 0px 0px 5px 0px rgba(0,0,0,0.1);
        width: 100%;
        margin-bottom: 20px;
      }

      button {
        padding: 10px 20px;
        border-radius: 5px;
        border: none;
        background-color: #0056b3;
        color: #fff;
        font-size: 16px;
        cursor: pointer;
        transition: all 0.3s ease-in-out;
      }

      button:hover {
        background-color: pink;
      }

      #result {
        font-size: 24px;
        margin-top: 30px;
        color: #007bff;
      }
      a{
		color: #C09853;
		text-decoration: none;
		}
		a:link{
			color: #353535;
			text-decoration: none;
		}
		a:hover{
			color: pink;
			text-decoration: underline;
		}
		a:active{
			color: #666666;
			text-decoration: none;
		}
        
    </style>
  </head>
  <body>
    <div class="snow"></div>
    <div class="container">
      <h1>计算两个时间的间隔天数</h1>
      <form>
        <label for="start">起始时间:</label>
        <input type="datetime-local" id="start" name="start">
        <label for="end">结束时间:</label>
        <input type="datetime-local" id="end" name="end">
        <button type="button" onclick="calculate()">计算</button>
      </form>
      <div id="result1"></div>
    </div>
    
    <div class="container">
      <audio id="music" src="http://m10.music.126.net/20230319212825/6d755831c2bc95380707968755911a86/ymusic/d19f/078b/e32f/65749afe3422e02b9003d8c5e4221d23.mp3" loop autoplay></audio>
      <h1 class="animate__animated animate__heartBeat animate__infinite">谭娅琦大王专用</h1>
      <h3>It's specifically designed for Yaqi Tan</h3>
      <div class="logo" onClick="play()" alt="user"></div>
      <form>
        <div>猜一猜2004年2月9日距今已经过去了多少天？</div>
        <br/>
        <button id="myButton" type="button" onclick="">点我查看</button>
      </form>
      <div id="result2"></div>
      <br/>
      <div><a href="https://www.douyin.com/user/MS4wLjABAAAAO8SMDkfRSDvvk45GQKUbAosb0A85blostWQzW8fY9Kc" target="_blank">感谢你们的关注！</a></div>
    </div>

    <script>
      // 获取按钮元素
      var button = document.getElementById("myButton");

      // 给按钮绑定点击事件
      button.addEventListener("click", function() {
        // 计算距离2004年2月9日已经过去的天数
        var birthday = new Date("2004/2/9");
        var today = new Date();
        var daysElapsed = Math.floor((today - birthday) / (24 * 60 * 60 * 1000));

        // 计算距离开始日期已经过去了多少毫秒
        const elapsedTime = Date.now() - birthday.getTime();
        // 将毫秒转换为年、月、天的格式
        var years = today.getFullYear() - birthday.getFullYear();
        var months = today.getMonth() - birthday.getMonth();
        if(months < 0){
            months = today.getMonth() - birthday.getMonth() + 12;
            years = years -1;
        }
        var days = today.getDate() - birthday.getDate();
        if(days < 0){
            days = today.getDate() - birthday.getDate() + 30;
            months = months - 1;
        }

        // 创建弹窗元素
        var popup = document.createElement("div");
        popup.innerHTML = "欢迎来到真实世界第" + daysElapsed + "天（即" + years + "年" + months + "月" + days + "天）" ;
        popup.style.position = "absolute";
        popup.style.top = "50%";
        popup.style.left = "50%";
        popup.style.transform = "translate(-50%, -50%)";
        popup.style.backgroundColor = "#fff";
        popup.style.padding = "20px";
        popup.style.borderRadius = "5px";
        popup.style.boxShadow = "0px 2px 10px rgba(0, 0, 0, 0.3)";

        for (var i = 0; i < 50; i++) {
	        var snowflake = document.createElement("div");
	        snowflake.className = "snow";
	        document.body.appendChild(snowflake);
        }

        // 将弹窗元素添加到页面中
        document.body.appendChild(popup);

        // 定时器，5秒后删除弹窗元素
        setTimeout(function() {
          document.body.removeChild(popup);
        }, 5000);
      });

     
      function calculate() {
        
        // alert("请输入起始时间和结束时间！");
        //计算多少天
        const start = new Date(document.getElementById("start").value);
        const end = new Date(document.getElementById("end").value);
        if(!start.getFullYear() || !end.getFullYear()){
            alert("请输入起始时间和结束时间！");
            return 0;
        }

        const diffTime = Math.abs(end - start);
        const diffDays = Math.ceil(diffTime / (1000 * 60 * 60 * 24));

        //计算xx年xx月xx天
        var date1 = new Date(document.getElementById("start").value);
		var date2 = new Date(document.getElementById("end").value);
        var years = date2.getFullYear() - date1.getFullYear();
        var months = date2.getMonth() - date1.getMonth();
        
        if(months < 0){
            months = date2.getMonth() - date1.getMonth() + 12;
            years = years -1;
        }
        var days = date2.getDate() - date1.getDate();
        if(days < 0){
            days = date2.getDate() - date1.getDate() + 30;
            months = months - 1;
        }

        const resultElement = document.getElementById("result1");
        resultElement.innerHTML = `两个时间之间间隔：<span>${diffDays}</span>天 (即${years}年${months}月${days}天）`;

        // 添加动画特效
        resultElement.style.opacity = "0";
        setTimeout(() => {
          resultElement.style.opacity = "1";
        }, 500);
      }

      window.onload = function(){ 
          var audio = document.getElementById('music');
         audio.pause();//打开页面时无音乐
      }
      function play() {
        var audio = document.getElementById('music');
        if (audio.paused) {
          audio.play();
          //document.getElementById('musicImg').src="images/play.png";
        }else{
          audio.pause();
          audio.currentTime = 0;//音乐从头播放
          //document.getElementById('musicImg').src="images/stop.png";
        }
      }

    </script>
  </body>
</html>
