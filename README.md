<!DOCTYPE html>
<html lang="zh-CN">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>fkmt测试</title>
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

     .btn-clear {
            margin-top: 10px;
        }

     .test-selection {
            margin-bottom: 20px;
        }
    </style>
</head>

<body>
    <div class="test-container">
        <h1 class="text-center mb-4">测试题选择</h1>
        <div class="test-selection">
            <p>请选择想要进行的测试：</p>
            <input type="radio" id="test1Radio" name="testSelect" value="test1">
            <label for="test1Radio">测测你是fkmt中的谁</label><br>
            <input type="radio" id="test2Radio" name="testSelect" value="test2">
            <label for="test2Radio">测测你跟fkmt角色的缘分值</label>
        </div>
        <div id="test1Content" style="display: none;">
            <h1 class="text-center mb-4">测测你是fkmt中的谁</h1>
            <form id="testForm1">
                <div class="question">
                    <p>在每个题目中，选择一个最符合你自己的选项，不能遗漏。<br>注意:请按第一印象做最快的选择。<br>问题1：如果你中了500万大奖，你会选择？</p>
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
                    <p>问题2：我喜欢在团队项目中承担领导角色。</p>
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
            <div class="result" id="result1"></div>
            <button type="button" class="btn btn-secondary btn-clear w-100" id="clearButton1">返回选题</button>
        </div>
        <div id="test2Content" style="display: none;">
            <h1 class="text-center mb-4">测测你跟fkmt角色的缘分值</h1>
            <form id="testForm2">
                <div class="question">
                   <p>在每个题目中，选择一个最符合你自己的选项，不能遗漏。<br>注意:请按第一印象做最快的选择。<br>问题1：那个选项让你觉得更加困难？</p>
                    <div class="form-check">
                        <input class="form-check-input" type="radio" id="q21a1" name="q21" value="a">
                        <label class="form-check-label" for="q21a1">被喜欢的人讨厌</label>
                    </div>
                    <div class="form-check">
                        <input class="form-check-input" type="radio" id="q21a2" name="q21" value="b">
                        <label class="form-check-label" for="q21a2">失败，在我想达成的事情上</label>
                    </div>
                    <div class="form-check">
                        <input class="form-check-input" type="radio" id="q21a3" name="q21" value="c">
                        <label class="form-check-label" for="q21a3">孤独，不受人欢迎</label>
                    </div>
					<div class="form-check">
					    <input class="form-check-input" type="radio" id="q21a2" name="q21" value="d">
					    <label class="form-check-label" for="q21a4">失去我认为重要的东西</label>
					</div>
                </div>
                <div class="question">
                    <p>问题2：哪个选项更符合你？</p>
                    <div class="form-check">
                        <input class="form-check-input" type="radio" id="q22a1" name="q22" value="a">
                        <label class="form-check-label" for="q22a1">我更擅长利用性格魅力鼓励别人</label>
                    </div>
                    <div class="form-check">
                        <input class="form-check-input" type="radio" id="q22a2" name="q22" value="b">
                        <label class="form-check-label" for="q22a2">我更擅长在复杂的环境中随机应变</label>
                    </div>
                    <div class="form-check">
                        <input class="form-check-input" type="radio" id="q22a3" name="q22" value="c">
                        <label class="form-check-label" for="q22a3">我更擅长指定周密的计划并严格执行</label>
                    </div>
					<div class="form-check">
					    <input class="form-check-input" type="radio" id="q22a3" name="q22" value="d">
					    <label class="form-check-label" for="q22a4">我更相信自己有转危为安的能力</label>
					</div>
					<div class="form-check">
					    <input class="form-check-input" type="radio" id="q22a3" name="q22" value="e">
					    <label class="form-check-label" for="q22a5">我的情绪更稳定，冷静且能容忍</label>
					</div>
                </div>
                <button type="submit" class="btn btn-primary w-100">提交</button>
            </form>
            <div class="result" id="result2"></div>
            <button type="button" class="btn btn-secondary btn-clear w-100" id="clearButton2">返回选题</button>
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
                }
            });

            const testForm1 = document.getElementById('testForm1');
            const result1 = document.getElementById('result1');
            const clearButton1 = document.getElementById('clearButton1');

            testForm1.addEventListener('submit', function (e) {
                e.preventDefault();
                let score = 0;

                // 获取问题1的答案
                let q1 = document.querySelector('input[name="q1"]:checked');
                if (q1 && q1.value === 'a') {
                    score++;
                }

                // 获取问题2的答案
                let q2 = document.querySelector('input[name="q2"]:checked');
                if (q2) {
                    score += parseInt(q2.value);
                }

                // 获取问题3的答案
                let q3 = document.querySelector('input[name="q3"]:checked');
                if (q3 && q3.value === 'b') {
                    score++;
                }

                let resultText = "";
                if (score >= 7) {
                    resultText = "恭喜你，在原单选题测试中表现出色！";
                } else if (score >= 4 && score < 7) {
                    resultText = "很不错，答对了大部分题目，继续保持！";
                } else if (score >= 2 && score < 4) {
                    resultText = "答对了一些题目，你还可以在这些方面进一步探索哦。";
                } else {
                    resultText = "很遗憾，原单选题测试不太理想，别气馁，总结经验下次会更好！";
                }
                result1.innerHTML = resultText;
            });

            clearButton1.addEventListener('click', function () {
                const radios = document.querySelectorAll('input[type="radio"]', testForm1);
                radios.forEach(function (radio) {
                    radio.checked = false;
                });
                result1.innerHTML = '';
                test1Content.style.display = 'none';
                test1Radio.checked = false;
            });

            const testForm2 = document.getElementById('testForm2');
            const result2 = document.getElementById('result2');
            const clearButton2 = document.getElementById('clearButton2');

         testForm2.addEventListener('submit', function (e) {
             e.preventDefault();
             let score = 0;
         
             // 获取问题1的答案
             let q21 = document.querySelector('input[name="q21"]:checked');
             if (q21 && q21.value === 'b') {
                 score++;
             }
         
             // 获取问题2的答案
             let q22 = document.querySelector('input[name="q22"]:checked');
             if (q22 && q22.value === 'b') {
                 score++;
             }
         
             // 获取问题3的答案
          
         
             let resultText = "";
             if (score >= 7) {
                 resultText = "恭喜你，在原单选题测试中表现出色！";
             } else if (score >= 4 && score < 7) {
                 resultText = "很不错，答对了大部分题目，继续保持！";
             } else if (score >= 2 && score < 4) {
                 resultText = "答对了一些题目，你还可以在这些方面进一步探索哦。";
             } else {
                 resultText = "很遗憾，原单选题测试不太理想，别气馁，总结经验下次会更好！";
             }
             result2.innerHTML = resultText;
         });

            clearButton2.addEventListener('click', function () {
                const radios = document.querySelectorAll('input[type="radio"]', testForm2);
                radios.forEach(function (radio) {
                    radio.checked = false;
                });
                result2.innerHTML = '';
                test2Content.style.display = 'none';
                test2Radio.checked = false;
            });
        });
    </script>
    <!-- 引入Bootstrap JavaScript -->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.bundle.min.js"
        integrity="sha384-C6RzsynM9kWDrMNeT87bh95OGNyZPhcTNXj1NW7RuBCsyN/o0jlpcV8Qyq46cDfL"
        crossorigin="anonymous"></script>
</body>

</html>
