<!DOCTYPE html>
<html lang="zh">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>表白页面</title>
<style>
  body, html {
    height: 100%;
    margin: 0;
    font-family: 'Arial', sans-serif;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    background-color: #ffe0e0;
  }

  .confession {
    text-align: center;
  }

  .confession h1 {
    font-size: 2em;
    margin-bottom: 0.25em;
  }

  .confession p {
    font-size: 1.5em;
    margin-top: 0;
  }

  .heart {
    position: relative;
    width: 100px;
    height: 90px;
    animation: pulse 1s infinite;
    margin-bottom: 20px;
  }

  .heart:before,
  .heart:after {
    position: absolute;
    content: "";
    left: 50px;
    top: 0;
    width: 50px;
    height: 80px;
    background: red;
    border-radius: 50px 50px 0 0;
    transform: rotate(-45deg);
    transform-origin: 0 100%;
  }

  .heart:after {
    left: 0;
    transform: rotate(45deg);
    transform-origin: 100% 100%;
  }

  @keyframes pulse {
    0% {
      transform: scale(1);
    }
    50% {
      transform: scale(1.1);
    }
    100% {
      transform: scale(1);
    }
  }

  button {
    font-size: 1em;
    padding: 10px 20px;
    margin: 5px;
    cursor: pointer;
  }
</style>
</head>
<body>

<div class="confession">
  <div class="heart"></div>
  <h1>我爱你</h1>
  <p>愿意跟我一起走下去吗？</p>
  <button id="yes">愿意</button>
  <button id="no">不愿意</button>
</div>

<script>
  // 获取按钮元素
  var yesButton = document.getElementById('yes');
  var noButton = document.getElementById('no');

  // 为按钮添加点击事件监听器
  yesButton.addEventListener('click', function() {
    console.log('✌，那我们明天去领证吧！');
    alert('✌，那我们明天去领证吧！');
  });

  noButton.addEventListener('click', function() {
    console.log('拒绝无效！！！你还可以再选一次。');
    alert('拒绝无效！！！你还可以再选一次。');
  });
</script>

</body>
</html>
