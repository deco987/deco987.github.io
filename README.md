<!DOCTYPE html>
<html lang="zh-CN">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>线上单选题测试</title>
    <style>
        body {
            font-family: Arial, sans-serif;
        }

        h1 {
            text-align: center;
        }

      .question {
            margin-bottom: 20px;
        }

      .result {
            margin-top: 20px;
            font-weight: bold;
        }
    </style>
</head>

<body>
    <h1>线上单选题测试</h1>
    <form id="testForm">
        <div class="question">
            <p>问题1：以下哪种动物是哺乳动物？</p>
            <input type="radio" id="q1a1" name="q1" value="a"> 蛇
            <input type="radio" id="q1a2" name="q1" value="b"> 猫
            <input type="radio" id="q1a3" name="q1" value="c"> 鸡
        </div>
        <div class="question">
            <p>问题2：地球的自转周期大约是？</p>
            <input type="radio" id="q2a1" name="q2" value="a"> 12小时
            <input type="radio" id="q2a2" name="q2" value="b"> 24小时
            <input type="radio" id="q2a3" name="q2" value="c"> 365天
        </div>
        <div class="question">
            <p>问题3：中国的首都是？</p>
            <input type="radio" id="q3a1" name="q3" value="a"> 上海
            <input type="radio" id="q3a2" name="q3" value="b"> 北京
            <input type="radio" id="q3a3" name="q3" value="c"> 广州
        </div>
        <input type="submit" value="提交">
    </form>
    <div class="result" id="result"></div>

    <script>
        document.getElementById('testForm').addEventListener('submit', function (e) {
            e.preventDefault();// 阻止表单默认提交行为

            let score = 0;

            // 获取问题1的答案
            let q1 = document.querySelector('input[name="q1"]:checked');
            if (q1 && q1.value === 'b') {
                score++;
            }

            // 获取问题2的答案
            let q2 = document.querySelector('input[name="q2"]:checked');
            if (q2 && q2.value === 'b') {
                score++;
            }

            // 获取问题3的答案
            let q3 = document.querySelector('input[name="q3"]:checked');
            if (q3 && q3.value === 'b') {
                score++;
            }

            let resultDiv = document.getElementById('result');
            resultDiv.innerHTML = `你的得分是：${score}/3`;
        });
    </script>
</body>

</html>
