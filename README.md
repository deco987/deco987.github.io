<!DOCTYPE html>
<html lang="zh-CN">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>线上测试</title>
    <!-- 引入Bootstrap CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet"
        integrity="sha384-T3c6CoIi6uLrA9TneNEoa7RxnatzjcDSCmG1MXxSR1GAsXEV/Dwwykc2MPK8M2HN" crossorigin="anonymous">
    <!-- 引入Chart.js -->
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <style>
        body {
            background-image: url('https://www.helloimg.com/i/2025/01/07/677cc44fd73c5.jpg');
            background-size: cover;
            background-position: center;
            background-repeat: no-repeat;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            min-height: 100vh;
            margin: 0;
        }

     .test-container {
            background-color: rgba(255, 255, 255, 0.8);
            border-radius: 15px;
            box-shadow: 0 0 15px rgba(0, 0, 0, 0.1);
            padding: 40px;
            width: 80%;
            max-width: 800px;
            margin: 0 auto;
        }

     .test-selection {
            margin-bottom: 30px;
        }

     .test-card {
            background-color: #f0f0f5;
            border-radius: 10px;
            box-shadow: 0 0 5px rgba(0, 0, 0, 0.1);
            padding: 20px;
            margin-bottom: 20px;
        }

     .question {
            font-size: 18px;
            font-weight: bold;
            margin-bottom: 15px;
        }

     .form-check {
            font-size: 16px;
        }

     .result {
            margin-top: 30px;
            font-weight: bold;
            text-align: center;
        }

     .btn-primary {
            background-color: #007bff;
            border-color: #007bff;
            padding: 12px 24px;
            font-size: 16px;
        }

     .btn-primary:hover {
            background-color: #0056b3;
            border-color: #0056b3;
        }

     .btn-clear {
            margin-top: 15px;
            padding: 12px 24px;
            font-size: 16px;
        }

     .chart-container {
            margin-top: 20px;
            width: 100%;
            max-width: 400px;
        }

      /* 新增样式，调整标题字号 */
      h1 {
            font-size: 24px; /* 缩小标题字号 */
        }
    </style>
</head>

<body>
    <div class="test-container">
        <h1 class="text-center mb-4">线上测试选择</h1>
        <div class="test-selection">
            <p>请选择要进行的测试：</p>
            <input type="radio" id="test1Radio" name="testSelect" value="test1">
            <label for="test1Radio">原单选题测试</label><br>
            <input type="radio" id="test2Radio" name="testSelect" value="test2">
            <label for="test2Radio">测测你是谁</label>
        </div>
        <div id="test1Content" style="display: none;">
            <h1 class="text-center mb-4">原单选题测试</h1>
            <form id="testForm1">
                <div class="test-card">
                    <div class="question">
                        <p>问题1：以下哪种动物是哺乳动物？</p>
                    </div>
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
                <div class="test-card">
                    <div class="question">
                        <p>问题2：我喜欢在团队项目中承担领导角色。</p>
                    </div>
                    <div class="form-check">
                        <input class="form-check-input" type="radio" id="q2a1" name="q2" value="1">
                        <label class="form-check-label" for="q2a1">最不符合</label>
                    </div>
                    <div class="form-check">
                        <input class="form-check-input" type="radio" id="q2a2" name="q2" value="2">
                        <label class="form-check-label" for="q2a2">不太符合</label>
                    </div>
                    <div class="form-check">
                        <input class="form-check-input" type="radio" id="q2a3" name="q2" value="3">
                        <label class="form-check-label" for="q2a3">一般</label>
                    </div>
                    <div class="form-check">
                        <input class="form-check-input" type="radio" id="q2a4" name="q2" value="4">
                        <label class="form-check-label" for="q2a4">比较符合</label>
                    </div>
                    <div class="form-check">
                        <input class="form-check-input" type="radio" id="q2a5" name="q2" value="5">
                        <label class="form-check-label" for="q2a5">最符合</label>
                    </div>
                </div>
                <div class="test-card">
                    <div class="question">
                        <p>问题3：中国的首都是？</p>
                    </div>
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
            <div class="result" id="result1"></div>
            <div class="chart-container">
                <canvas id="test1Chart"></canvas>
            </div>
            <button type="button" class="btn btn-secondary btn-clear w-100" id="clearButton1">清除答案</button>
        </div>
        <div id="test2Content" style="display: none;">
            <h1 class="text-center mb-4">测测你是谁</h1>
            <form id="testForm2">
                <div class="test-card">
                    <div class="question">
                        <p>问题1：当你独处时，你通常会做什么？</p>
                    </div>
                    <div class="form-check">
                        <input class="form-check-input" type="radio" id="q21a1" name="q21" value="a">
                        <label class="form-check-label" for="q21a1">阅读书籍</label>
                    </div>
                    <div class="form-check">
                        <input class="form-check-input" type="radio" id="q21a2" name="q21" value="b">
                        <label class="form-check-label" for="q21a2">听音乐</label>
                    </div>
                    <div class="form-check">
                        <input class="form-check-input" type="radio" id="q21a3" name="q21" value="c">
                        <label class="form-check-label" for="q21a3">做运动</label>
                    </div>
                </div>
                <div class="test-card">
                    <div class="question">
                        <p>问题2：你最喜欢的颜色是？</p>
                    </div>
                    <div class="form-check">
                        <input class="form-check-input" type="radio" id="q22a1" name="q22" value="a">
                        <label class="form-check-label" for="q22a1">蓝色</label>
                    </div>
                    <div class="form-check">
                        <input class="form-check-input" type="radio" id="q22a2" name="q22" value="b">
                        <label class="form-check-label" for="q22a2">红色</label>
                    </div>
                    <div class="form-check">
                        <input class="form-check-input" type="radio" id="q22a3" name="q22" value="c">
                        <label class="form-check-label" for="q22a3">绿色</label>
                    </div>
                </div>
                <button type="submit" class="btn btn-primary w-100">提交</button>
            </form>
            <div class="result" id="result2"></div>
            <div class="chart-container">
                <canvas id="test2Chart"></canvas>
            </div>
            <button type="button" class="btn btn-secondary btn-clear w-100" id="clearButton2">清除答案</button>
        </div>
    </div>

    <script>
        document.addEventListener('DOMContentLoaded', function () {
            const test1Radio = document.getElementById('test1Radio');
            const test2Radio = document.getElementById('test2Radio');
            const test1Content = document.getElementById('test1Content');
            const test2Content = document.getElementById('test2Content');

            test1Radio.addEventListener('change', function () {
                if (this.checked) {
                    test1Content.style.display = 'block';
                    test2Content.style.display = 'none';
                    const radios1 = document.querySelectorAll('input[type="radio"]', testForm1);
                    radios1.forEach(function (radio) {
                        radio.checked = false;
                    });
                    const result1Element = document.getElementById('result1');
                    result1Element.innerHTML = '';
                    const test1Chart = new Chart(document.getElementById('test1Chart'), {
                        type: 'bar',
                        data: {
                            labels: ['知识得分', '领导能力得分'],
                            datasets: [{
                                label: '维度得分',
                                data: [0, 0],
                                backgroundColor: 'rgba(54, 162, 235, 0.6)',
                                borderColor: 'rgba(54, 162, 235, 1)',
                                borderWidth: 1
                            }]
                        },
                        options: {
                            scales: {
                                y: {
                                    beginAtZero: true
                                }
                            }
                        }
                    });
                }
            });

            test2Radio.addEventListener('change', function () {
                if (this.checked) {
                    test1Content.style.display = 'none';
                    test2Content.style.display = 'block';
                    const radios2 = document.querySelectorAll('input[type="radio"]', testForm2);
                    radios2.forEach(function (radio) {
                        radio.checked = false;
                    });
                    const result2Element = document.getElementById('result2');
                    result2Element.innerHTML = '';
                    const test2Chart = new Chart(document.getElementById('test2Chart'), {
                        type: 'bar',
                        data: {
                            labels: ['兴趣爱好得分', '颜色偏好得分'],
                            datasets: [{
                                label: '维度得分',
                                data: [0, 0],
                                backgroundColor: 'rgba(255, 99, 132, 0.6)',
                                borderColor: 'rgba(255, 99, 132, 1)',
                                borderWidth: 1
                            }]
                        },
                        options: {
                            scales: {
                                y: {
                                    beginAtZero: true
                                }
                            }
                        }
                    });
                }
            });

            const testForm1 = document.getElementById('testForm1');
            const result1 = document.getElementById('result1');
            const clearButton1 = document.getElementById('clearButton1');
            const test1Chart = new Chart(document.getElementById('test1Chart'), {
                type: 'bar',
                data: {
                    labels: ['知识得分', '领导能力得分'],
                    datasets: [{
                        label: '维度得分',
                        data: [0, 0],
                        backgroundColor: 'rgba(54, 162, 235, 0.6)',
                        borderColor: 'rgba(54, 162, 235, 1)',
                        borderWidth: 1
                    }]
                },
                options: {
                    scales: {
                        y: {
                            beginAtZero: true
                        }
                    }
                }
            });

            testForm1.addEventListener('submit', function (e) {
                e.preventDefault();
                // 定义维度得分
                let knowledgeScore = 0;
                let leadershipScore = 0;

                // 获取问题1的答案
                let q1 = document.querySelector('input[name="q1"]:checked');
                if (q1 && q1.value === 'b') {
                    knowledgeScore += 1;
                }

                // 获取问题2的答案
                let q2 = document.querySelector('input[name="q2"]:checked');
                if (q2) {
                    leadershipScore += parseInt(q2.value);
                }

                // 获取问题3的答案
                let q3 = document.querySelector('input[name="q3"]:checked');
                if (q3 && q3.value === 'b') {
                    knowledgeScore += 1;
                }

                let resultText = "";
                if (knowledgeScore >= 2 && leadershipScore >= 7) {
                    resultText = "你在知识储备和领导能力方面都表现出色！";
                } else if (knowledgeScore >= 2 && leadershipScore < 7) {
                    resultText = "你有丰富的知识，但在领导能力方面还有提升空间。";
                } else if (knowledgeScore < 2 && leadershipScore >= 7) {
                    resultText = "你具备较强的领导潜力，但知识方面需要加强学习。";
                } else {
                    resultText = "你在知识和领导能力方面都有进步的空间，继续努力！";
                }
                result1.innerHTML = resultText;

                // 更新图表数据
                test1Chart.data.datasets[0].data = [knowledgeScore, leadershipScore];
                test1Chart.update();
            });

            clearButton1.addEventListener('click', function () {
                const radios = document.querySelectorAll('input[type="radio"]', testForm1);
                radios.forEach(function (radio) {
                    radio.checked = false;
                });
                result1.innerHTML = '';
                test1Content.style.display = 'none';
                test1Radio.checked = false;
                // 重置图表数据
                test1Chart.data.datasets[0].data = [0, 0];
                test1Chart.update();
            });

            const testForm2 = document.getElementById('testForm2');
            const result2 = document.getElementById('result2');
            const clearButton2 = document.getElementById('clearButton2');
            const test2Chart = new Chart(document.getElementById('test2Chart'), {
                type: 'bar',
                data: {
                    labels: ['兴趣爱好得分', '颜色偏好得分'],
                    datasets: [{
                        label: '维度得分',
                        data: [0, 0],
                        backgroundColor: 'rgba(255,
