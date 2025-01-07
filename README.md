<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>fkmt测试</title>
    <!-- 引入Bootstrap CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet"
        integrity="sha384-T3c6CoIi6uLrA9TneNEoa7RxnatzjcDSCmG1MXxSR1GAsXEV/Dwwykc2MPK8M2HN" crossorigin="anonymous">
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
            padding: 20px;
            width: 100%;
         // 定义维度得分//max-width: 8000px;
            margin: 0 auto;
        }

     .test-selection {
            margin-bottom: 30px;
        }

     .test-card {
            background-color: #f0f0f5;
            border-radius: 10px;
            box-shadow: 0 0 5px rgba(0, 0, 0, 0.1);
            padding: 15px;
            margin-bottom: 13px;
        }

     .question {
            font-size: 15px;
            font-weight: bold;
            margin-bottom: 15px;
        }

     .form-check {
            font-size: 13px;
        }

     .result {
            margin-top: 20px;
        }

     .btn-primary {
            background-color: #007bff;
            border-color: #007bff;
            padding: 12px 24px;
            font-size: 13px;
        }

     .btn-primary:hover {
            background-color: #0056b3;
            border-color: #0056b3;
        }

     .btn-clear {
            margin-top: 15px;
            padding: 12px 24px;
            font-size: 13px;
        }

        h1 {
            font-size: 20px;
        }

     .result-table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 15px;
        }

     .result-table th,
     .result-table td {
            border: 1px solid #ddd;
            padding: 15px;
            text-align: center;
        }
    </style>
</head>

<body>
    <div class="test-container">
        <h1 class="text-center mb-4">测试选择</h1>
        <div class="test-selection">
            <p>请选择要进行的测试：</p>
            <input type="radio" id="test1Radio" name="testSelect" value="test1">
            <label for="test1Radio">测测你是fkmt几级学者（缓慢更新中）</label><br>
            <input type="radio" id="test2Radio" name="testSelect" value="test2">
            <label for="test2Radio">测测你跟fkmt角色的缘分值</label>
        </div>
        <div id="test1Content" style="display: none;">
            <h1 class="text-center mb-4">测测你是fkmt几级学者</h1>
            <form id="testForm1">
					 <div class="form-check">
						<p>本测试题只包含开司，斗牌，天河街，银与金，霸王传，涯的内容</p> <p>注意:每题都有且只有一个选项正确（不会可以蒙，运势对fkmt人也是至关重要的）</p>
				</div>
                <div class="test-card">
                    <div class="question">
                         <p>问题1：赤木在麻将界被称为“鬼神赤木”，算上天和街浪子和斗牌传说的全部内容，赤木一共胡过几次役满？</p>
                    </div>
                    <div class="form-check">
                        <input class="form-check-input" type="radio" id="q1a1" name="q1" value="a">
                        <label class="form-check-label" for="q1a1">1次</label>
                    </div>
                    <div class="form-check">
                        <input class="form-check-input" type="radio" id="q1a2" name="q1" value="b">
                        <label class="form-check-label" for="q1a2">2次</label>
                    </div>
                    <div class="form-check">
                        <input class="form-check-input" type="radio" id="q1a3" name="q1" value="c">
                        <label class="form-check-label" for="q1a3">3次</label>
                    </div>
					<div class="form-check">
					    <input class="form-check-input" type="radio" id="q1a4" name="q1" value="d">
					    <label class="form-check-label" for="q1a4">4次</label>
					</div>
					</div>
					<div class="test-card">
					<div class="question">
					     <p>问题2：以下哪种役满类型赤木没有胡过？</p>
					</div>
					<div class="form-check">
					    <input class="form-check-input" type="radio" id="q2a1" name="q2" value="a">
					    <label class="form-check-label" for="q2a1">字一色</label>
					</div>
					<div class="form-check">
					    <input class="form-check-input" type="radio" id="q2a2" name="q2" value="b">
					    <label class="form-check-label" for="q2a2">大三元</label>
					</div>
					<div class="form-check">
					    <input class="form-check-input" type="radio" id="q2a3" name="q2" value="c">
					    <label class="form-check-label" for="q2a3">四暗刻</label>
					</div>
					<div class="form-check">
					    <input class="form-check-input" type="radio" id="q2a4" name="q2" value="d">
					    <label class="form-check-label" for="q2a4">累计役满</label>
					</div>
					</div>
					<div class="test-card">
					<div class="question">
					     <p>问题3：天几乎可以称得上fkmt里最有女人缘的一位主角，问故事刚开始时，天跟几位女性同住？</p>
					</div>
					<div class="form-check">
					    <input class="form-check-input" type="radio" id="q3a1" name="q3" value="a">
					    <label class="form-check-label" for="q3a1">1位</label>
					</div>
					<div class="form-check">
					    <input class="form-check-input" type="radio" id="q3a2" name="q3" value="b">
					    <label class="form-check-label" for="q3a2">2位</label>
					</div>
					<div class="form-check">
					    <input class="form-check-input" type="radio" id="q3a3" name="q3" value="c">
					    <label class="form-check-label" for="q3a3">3位</label>
					</div>
					<div class="form-check">
					    <input class="form-check-input" type="radio" id="q3a4" name="q3" value="d">
					    <label class="form-check-label" for="q3a4">4位</label>
					</div>
					</div>
					<div class="test-card">
					<div class="question">
					     <p>问题4：大家都知道假赤木平山幸雄，是一个跟赤木完全不同类型的天才，只可惜天妒英才英年早逝，年纪轻轻就死在麻将桌上……问平山的忌日是哪一天？</p>
					</div>
					<div class="form-check">
					    <input class="form-check-input" type="radio" id="q4a1" name="q4" value="a">
					    <label class="form-check-label" for="q4a1">3月15号</label>
					</div>
					<div class="form-check">
					    <input class="form-check-input" type="radio" id="q4a2" name="q4" value="b">
					    <label class="form-check-label" for="q4a2">6月9号</label>
					</div>
					<div class="form-check">
					    <input class="form-check-input" type="radio" id="q4a3" name="q4" value="c">
					    <label class="form-check-label" for="q4a3">8月1号</label>
					</div>
					<div class="form-check">
					    <input class="form-check-input" type="radio" id="q4a4" name="q4" value="d">
					    <label class="form-check-label" for="q4a4">11月18号</label>
					</div>
					</div>
					<div class="test-card">
					<div class="question">
					     <p>问题5：鹫巢与赤木对决的那晚被称为“传说的一夜”，在这传说的一夜中，鹫巢大人大概输了多少钱？（算上赤木应得的部分）</p>
					</div>
					<div class="form-check">
					    <input class="form-check-input" type="radio" id="q5a1" name="q5" value="a">
					    <label class="form-check-label" for="q5a1">五亿</label>
					</div>
					<div class="form-check">
					    <input class="form-check-input" type="radio" id="q5a2" name="q5" value="b">
					    <label class="form-check-label" for="q5a2">六亿</label>
					</div>
					<div class="form-check">
					    <input class="form-check-input" type="radio" id="q5a3" name="q5" value="c">
					    <label class="form-check-label" for="q5a3">七亿</label>
					</div>
					<div class="form-check">
					    <input class="form-check-input" type="radio" id="q5a4" name="q5" value="d">
					    <label class="form-check-label" for="q5a5">八亿</label>
					</div>
				
					
					
					
                </div>
                <button type="submit" class="btn btn-primary w-100">提交</button>
            </form>
            <div id="result1" class="result"></div>
            <button type="button" class="btn btn-secondary btn-clear w-100" id="clearButton1">返回选题</button>
        </div>
        <div id="test2Content" style="display: none;">
            <h1 class="text-center mb-4">测测你跟fkmt角色的缘分值</h1>
            <form id="testForm2">
				<div class="form-check">
						<p>本测试题只包含开司，斗牌，天河街，银与金，霸王传，涯的内容</p> <p>注意:每题都有且只有一个选项正确（不会可以蒙，运势对fkmt人也是至关重要的）</p>
				</div>
                <div class="test-card">
                    <div class="question">
                        <p>问题1：下列哪项让你觉得更加困难？</p>
                    </div>
                    <div class="form-check">
                        <input class="form-check-input" type="radio" id="q21a1" name="q21" value="a">
                        <label class="form-check-label" for="q21a1">被喜欢的人讨厌</label>
                    </div>
                    <div class="form-check">
                        <input class="form-check-input" type="radio" id="q21a2" name="q21" value="b">
                        <label class="form-check-label" for="q21a2">失去重要的人</label>
                    </div>
                    <div class="form-check">
                        <input class="form-check-input" type="radio" id="q21a3" name="q21" value="c">
                        <label class="form-check-label" for="q21a3">孤独，不被人群接纳</label>
                    </div>
					<div class="form-check">
					    <input class="form-check-input" type="radio" id="q21a4" name="q21" value="d">
					    <label class="form-check-label" for="q21a4">拼尽全力却最终失败</label>
					</div>
                </div>
                <div class="test-card">
                    <div class="question">
                        <p>问题2：你的人际关系怎么样？</p>
                    </div>
                    <div class="form-check">
                        <input class="form-check-input" type="radio" id="q22a1" name="q22" value="a">
                        <label class="form-check-label" for="q22a1">我总是能在各个领域交到很多朋友</label>
                    </div>
                    <div class="form-check">
                        <input class="form-check-input" type="radio" id="q22a2" name="q22" value="b">
                        <label class="form-check-label" for="q22a2">我很喜欢认识新人，只是结果有时候不尽如人意</label>
                    </div>
                    <div class="form-check">
                        <input class="form-check-input" type="radio" id="q22a3" name="q22" value="c">
                        <label class="form-check-label" for="q22a3">我不太热衷于交朋友，有那么几个知心朋友就够了</label>
                    </div>
					<div class="form-check">
					    <input class="form-check-input" type="radio" id="q22a4" name="q22" value="d">
					    <label class="form-check-label" for="q22a4">我平等地讨厌每一个人，比起跟人相处，我更喜欢跟猫狗玩</label>
					</div>
                </div>
				<div class="test-card">
				    <div class="question">
				        <p>问题3：你对自己未来的人生有规划吗？</p>
				    </div>
				    <div class="form-check">
				        <input class="form-check-input" type="radio" id="q23a1" name="q23" value="a">
				        <label class="form-check-label" for="q23a1">我是个活在当下的人，对未来没什么实感</label>
				    </div>
				    <div class="form-check">
				        <input class="form-check-input" type="radio" id="q23a2" name="q23" value="b">
				        <label class="form-check-label" for="q23a2">我只会计划一下人生大事，比如去哪里工作，是否结婚……剩下的就随机应变了</label>
				    </div>
				    <div class="form-check">
				        <input class="form-check-input" type="radio" id="q23a3" name="q23" value="c">
				        <label class="form-check-label" for="q23a3">我喜欢在无聊的时候计划一下我的未来，不过不会想得很全面，也不一定会去执行</label>
				    </div>
					<div class="form-check">
					    <input class="form-check-input" type="radio" id="q23a4" name="q23" value="d">
					    <label class="form-check-label" for="q23a4">我对未来有着清晰的认识和预感，我知道自己想要成为什么样的人，并且在为那个目标而努力着</label>
					</div>
				</div>
				<div class="test-card">
				    <div class="question">
				        <p>问题4：你如何看待赌博？</p>
				    </div>
				    <div class="form-check">
				        <input class="form-check-input" type="radio" id="q24a1" name="q24" value="a">
				        <label class="form-check-label" for="q24a1">赌博是很可怕的东西，看看赌博相关的作品就是我的极限了</label>
				    </div>
				    <div class="form-check">
				        <input class="form-check-input" type="radio" id="q24a2" name="q24" value="b">
				        <label class="form-check-label" for="q24a2">小赌怡情，我偶尔会跟熟人打打赌钱的扑克麻将，不会赌得很大</label>
				    </div>
				    <div class="form-check">
				        <input class="form-check-input" type="radio" id="q24a3" name="q24" value="c">
				        <label class="form-check-label" for="q24a3">赌博就是胜负，哪怕在平时我也会跟朋友就某事赌两块钱</label>
				    </div>
					<div class="form-check">
					    <input class="form-check-input" type="radio" id="q24a4" name="q24" value="d">
					    <label class="form-check-label" for="q24a4">我很想试试fkmt中那种惊险刺激的赌博，哪怕输掉的代价很沉重也无所谓</label>
					</div>
				</div>
				<div class="test-card">
				    <div class="question">
				        <p>问题5：假如你有一千块钱，以下几个赌局中，你会参加哪一个？</p>
				    </div>
				    <div class="form-check">
				        <input class="form-check-input" type="radio" id="q25a1" name="q25" value="a">
				        <label class="form-check-label" for="q25a1">猜数字赌局，从1-10中猜一个数字，猜对了奖励一万块钱，猜错了失去一千块钱</label>
				    </div>
				    <div class="form-check">
				        <input class="form-check-input" type="radio" id="q25a2" name="q25" value="b">
				        <label class="form-check-label" for="q25a2">猜骰子大小的赌局，猜对了奖励五百块，猜错了失去五百块</label>
				    </div>
				    <div class="form-check">
				        <input class="form-check-input" type="radio" id="q25a3" name="q25" value="c">
				        <label class="form-check-label" for="q25a3">根据言行判断人是否说谎的赌局，判断对了奖励八百块，错了失去八百块</label>
				    </div>
					<div class="form-check">
					    <input class="form-check-input" type="radio" id="q25a4" name="q25" value="d">
					    <label class="form-check-label" for="q25a4">规则复杂的私人赌局，输赢金额均无上限</label>
					</div>
					<div class="form-check">
					    <input class="form-check-input" type="radio" id="q25a5" name="q25" value="e">
					    <label class="form-check-label" for="q25a5">我一个都不会参加</label>
					</div>
				</div>
				
				
				
				
				
				
                <button type="submit" class="btn btn-primary w-100">提交</button>
            </form>
            <div id="result2" class="result"></div>
            <button type="button" class="btn btn-secondary btn-clear w-100" id="clearButton2">清除答案</button>
        </div>
    </div>

    <script>
        document.addEventListener('DOMContentLoaded', function () {
            const test1Radio = document.getElementById('test1Radio');
            const test2Radio = document.getElementById('test2Radio');
            const test1Content = document.getElementById('test1Content');
            const test2Content = document.getElementById('test2Content');
            const result1 = document.getElementById('result1');
            const result2 = document.getElementById('result2');

            const handleTestChange = function () {
                if (this === test1Radio) {
                    test1Content.style.display = 'block';
                    test2Content.style.display = 'none';
                    const radios1 = document.querySelectorAll('input[type="radio"]', testForm1);
                    radios1.forEach(function (radio) {
                        radio.checked = false;
                    });
                    result1.innerHTML = '';
                } else if (this === test2Radio) {
                    test1Content.style.display = 'none';
                    test2Content.style.display = 'block';
                    const radios2 = document.querySelectorAll('input[type="radio"]', testForm2);
                    radios2.forEach(function (radio) {
                        radio.checked = false;
                    });
                    result2.innerHTML = '';
                }
            };

            test1Radio.addEventListener('change', handleTestChange);
            test2Radio.addEventListener('change', handleTestChange);

            const testForm1 = document.getElementById('testForm1');
            const clearButton1 = document.getElementById('clearButton1');

            testForm1.addEventListener('submit', function (e) {
                e.preventDefault();
                // 定义维度得分
                let knowledgeScore = 0;

                // 获取问题1的答案
                let q1 = document.querySelector('input[name="q1"]:checked');
                if (q1 && q1.value === 'b') {
                    knowledgeScore += 1;
                }

                let resultText = "";
                if (knowledgeScore >= 1) {
                    resultText = "你答对了，知识掌握不错！";
                } else {
                    resultText = "你在知识方面还有进步空间。";
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
            const clearButton2 = document.getElementById('clearButton2');

            testForm2.addEventListener('submit', function (e) {
                e.preventDefault();
                // 定义维度得分
                let hobbyScore = 0;
                let colorPreferenceScore = 0;

                // 获取问题1的答案
                let q21 = document.querySelector('input[name="q21"]:checked');
                if (q21) {
                    if (q21.value === 'a') {
                        hobbyScore += 1;
                    } else if (q21.value === 'b') {
                        hobbyScore += 2;
                    } else if (q21.value === 'c') {
                        hobbyScore += 3;
                    }
                }

                // 获取问题2的答案
                let q22 = document.querySelector('input[name="q22"]:checked');
                if (q22) {
                    if (q22.value === 'a') {
                        colorPreferenceScore += 1;
                    } else if (q22.value === 'b') {
                        colorPreferenceScore += 2;
                    } else if (q22.value === 'c') {
                        colorPreferenceScore += 3;
                    }
                }

                let resultTableHTML = '<table class="result-table"><tr><th>维度名称</th><th>结论</th></tr>';
                // 兴趣爱好得分结论
                let hobbyResult = "";
                if (hobbyScore >= 2) {
                    hobbyResult = "你有丰富的兴趣爱好";
                } else {
                    hobbyResult = "你可以尝试培养更多兴趣爱好";
                }
                resultTableHTML += `<tr><td>兴趣爱好得分</td><td>${hobbyResult}</td></tr>`;
                // 颜色偏好得分结论
                let colorResult = "";
                if (colorPreferenceScore >= 2) {
                    colorResult = "你对颜色有明确的偏好";
                } else {
                    colorResult = "你对颜色的偏好不太明显";
                }
                resultTableHTML += `<tr><td>颜色偏好得分</td><td>${colorResult}</td></tr></table>`;
                result2.innerHTML = resultTableHTML;
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
</body>
