<html lang="zh-CN">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>线上单选题测试</title>
    <!-- 引入Bootstrap CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet"
        integrity="sha384-T3c6CoIi6uLrA9TneNEoa7RxnatzjcDSCmG1MXxSR1GAsXEV/Dwwykc2MPK8M2HN" crossorigin="anonymous">
    <style>
        body {
            background-color: #f8f9fa;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            min-height: 100vh;
            margin: 0;
        }

     .test-container {
            background-color: #fff;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            padding: 30px;
            width: 80%;
            max-width: 600px;
        }

     .question {
            margin-bottom: 20px;
        }

     .result {
            margin-top: 20px;
            font-weight: bold;
            text-align: center;
        }

     .btn-primary {
            background-color: #007bff;
            border-color: #007bff;
        }

     .btn-primary:hover {
            background-color: #0056b3;
            border-color: #0056b3;
        }
    </style>
</head>

<body>
    <div class="test-container">
        <h1 class="text-center mb-4">线上单选题测试</h1>
        <form id="testForm">
            <div class="question">
                <p>问题1：以下哪种动物是哺乳动物？</p>
                <div class="form-check">
                    <input class="form-check-input" type="radio" id="q1a1" name="q1" value="a">
                    <label class="form-check-label" for="q1a1">蛇</label>
                </div>
                <div class="form-check">
                    <input class="form-check-input" type="radio" id="q1a2" name="q1" value="b">
                    <label class="form-check-label" for="q1a2">猫</label>
                </div>
                <div class="form-check">
                    <input class="form-check-input" type="radio" id="q1a3" name="q1" value="c">
                    <label class="form-check-label" for="q1a3">鸡</label>
                </div>
            </div>
            <div class="question">
                <p>问题2：地球的自转周期大约是？</p>
                <div class="form-check">
                    <input class="form-check-input" type="radio" id="q2a1" name="q2" value="a">
                    <label class="form-check-label" for="q2a1">12小时</label>
                </div>
                <div class="form-check">
                    <input class="form-check-input" type="radio" id="q2a2" name="q2" value="b">
                    <label class="form-check-label" for="q2a2">24小时</label>
                </div>
                <div class="form-check">
                    <input class="form-check-input" type="radio" id="q2a3" name="q2" value="c">
                    <label class="form-check-label" for="q2a3">365天</label>
                </div>
            </div>
            <div class="question">
                <p>问题3：中国的首都是？</p>
                <div class="form-check">
                    <input class="form-check-input" type="radio" id="q3a1" name="q3" value="a">
                    <label class="form-check-label" for="q3a1">上海</label>
                </div>
                <div class="form-check">
                    <input class="form-check-input" type="radio" id="q3a2" name="q3" value="b">
                    <label class="form-check-label" for="q3a2">北京</label>
                </div>
                <div class="form-check">
                    <input class="form-check-input" type="radio" id="q3a3" name="q3" value="c">
                    <label class="form-check-label" for="q3a3">广州</label>
                </div>
            </div>
            <button type="submit" class="btn btn-primary w-100">提交</button>
        </form>
        <div class="result" id="result"></div>
    </div>

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
    <!-- 引入Bootstrap JavaScript -->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.bundle.min.js"
        integrity="sha384-C6RzsynM9kWDrMNeT87bh95OGNyZPhcTNXj1NW7RuBCsyN/o0jlpcV8Qyq46cDfL"
        crossorigin="anonymous"></script>
</body>

</html>
