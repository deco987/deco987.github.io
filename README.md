<html lang="zh-CN">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>fkmt 测试</title>
    <!-- 引入 Bootstrap CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet"
        integrity="sha384-T3c6CoIi6uLrA9TneNEoa7RxnatzjcDSCmG1MXxSR1GAsXEV/Dwwykc2MPK8M2HN" crossorigin="anonymous">
    <style>
        body {
            background-image: url('https://www.helloimg.com/i/2025/01/07/677cc44fd73c5.jpg'); // 修正背景图片路径
            background-size: cover;
			background-attachment: fixed;
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
			margin-bottom: 5px; 
        }

      .result {
            margin-top: 13px;
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
            <label for="test1Radio">你是 fkmt 几级学者（施工中）</label><br>
            <input type="radio" id="test2Radio" name="testSelect" value="test2">
            <label for="test2Radio">测测你跟 fkmt 角色的缘分值</label>
        </div>
        <div id="test1Content" style="display: none;">
            <h1 class="text-center mb-4">测测你是 fkmt 几级学者</h1>
            <form id="testForm1">
                <div class="form-check">
                    <p>本测试题只包含开司，斗牌，天河街，银与金，霸王传，涯的内容</p>
                    <p>注意:每题都有且只有一个选项正确（不会可以蒙，运势对 fkmt 人也是至关重要的）</p>
                </div>
                <div class="test-card">
                    <div class="question">
                        <p>问题 1：赤木在麻将界被称为“鬼神赤木”，算上天和街浪子和斗牌传说的全部内容，赤木一共胡过几次役满？</p>
                    </div>
                    <div class="form-check">
                        <input class="form-check-input" type="radio" id="q1a1" name="q1" value="a">
                        <label class="form-check-label" for="q1a1">1 次</label>
                    </div>
                    <div class="form-check">
                        <input class="form-check-input" type="radio" id="q1a2" name="q1" value="b">
                        <label class="form-check-label" for="q1a2">2 次</label>
                    </div>
                    <div class="form-check">
                        <input class="form-check-input" type="radio" id="q1a3" name="q1" value="c">
                        <label class="form-check-label" for="q1a3">3 次</label>
                    </div>
                    <div class="form-check">
                        <input class="form-check-input" type="radio" id="q1a4" name="q1" value="d">
                        <label class="form-check-label" for="q1a4">4 次</label>
                    </div>
                </div>
                <button type="submit" class="btn btn-primary w-100">提交</button>
            </form>
            <div id="result1" class="result"></div>
            <button type="button" class="btn btn-secondary btn-clear w-100" id="clearButton1">返回选题</button>
        </div>
        <div id="test2Content" style="display: none;">
            <h1 class="text-center mb-4">测测你跟 fkmt 角色的缘分值</h1>
            <form id="testForm2">
                <div class="test-card">
                    <div class="question">
                        <p>问题 1：下列哪项让你觉得更加困难？</p>
                    </div>
                    <div class="form-check">
                        <input class="form-check-input" type="radio" id="q21a1" name="q21" value="a">
                        <label class="form-check-label" for="q21a1">迷失，忘却自己的本心</label>
                    </div>
                    <div class="form-check">
                        <input class="form-check-input" type="radio" id="q21a2" name="q21" value="b">
                        <label class="form-check-label" for="q21a2">失去重要的人或东西</label>
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
				<div class="test-card">
				    <div class="question">
				        <p>问题6：如果你在赌局中已经取得了胜利，你会选择再来一次吗？</p>
				    </div>
				    <div class="form-check">
				        <input class="form-check-input" type="radio" id="q26a1" name="q26" value="a">
				        <label class="form-check-label" for="q26a1">加倍，再来</label>
				    </div>
				    <div class="form-check">
				        <input class="form-check-input" type="radio" id="q26a2" name="q26" value="b">
				        <label class="form-check-label" for="q26a2">再尝试一次，如果运气有下跌就收手</label>
				    </div>
				    <div class="form-check">
				        <input class="form-check-input" type="radio" id="q26a3" name="q26" value="c">
				        <label class="form-check-label" for="q26a3">我会给自己设定一个限度（比如赢一千或者输一千），达到限度之后会收手</label>
				    </div>
					<div class="form-check">
					    <input class="form-check-input" type="radio" id="q26a4" name="q26" value="d">
					    <label class="form-check-label" for="q26a4">果断收手</label>
					</div>
				</div>
				<div class="test-card">
				    <div class="question">
				        <p>问题7：如果有一个输赢都很大的赌局，需要多人才能进入，你会不会拉一个队友参加？</p>
				    </div>
				    <div class="form-check">
				        <input class="form-check-input" type="radio" id="q27a1" name="q27" value="a">
				        <label class="form-check-label" for="q27a1">我不会，输掉的代价太沉重了，我不能代替别人决定他们的命运</label>
				    </div>
				    <div class="form-check">
				        <input class="form-check-input" type="radio" id="q27a2" name="q27" value="b">
				        <label class="form-check-label" for="q27a2">我不会主动参加，但如果有人邀请我，我也可以试试</label>
				    </div>
				    <div class="form-check">
				        <input class="form-check-input" type="radio" id="q27a3" name="q27" value="c">
				        <label class="form-check-label" for="q27a3">如果有合适的队友人选，我会去尝试一下</label>
				    </div>
					<div class="form-check">
					    <input class="form-check-input" type="radio" id="q27a4" name="q27" value="d">
					    <label class="form-check-label" for="q27a4">我会参加，并且主动去寻找合适的队友</label>
					</div>
				</div>
				<div class="test-card">
				    <div class="question">
				        <p>问题8：你会怎样说服选择的同伴加入赌局？</p>
				    </div>
				    <div class="form-check">
				        <input class="form-check-input" type="radio" id="q28a1" name="q28" value="a">
				        <label class="form-check-label" for="q28a1">找我的朋友，我们的关系很好，只要我开口，他一定会参加</label>
				    </div>
				    <div class="form-check">
				        <input class="form-check-input" type="radio" id="q28a2" name="q28" value="b">
				        <label class="form-check-label" for="q28a2">向他哭诉我很需要这笔钱，求他入伙帮我这一把</label>
				    </div>
				    <div class="form-check">
				        <input class="form-check-input" type="radio" id="q28a3" name="q28" value="c">
				        <label class="form-check-label" for="q28a3">向他解释我为赌局做的准备，让他相信我会成功</label>
				    </div>
					<div class="form-check">
					    <input class="form-check-input" type="radio" id="q28a4" name="q28" value="d">
					    <label class="form-check-label" for="q28a4">向他坦诚我知道的一切，就连明言自己所求利益是钱也一样</label>
					</div>
				</div>
				<div class="test-card">
				    <div class="question">
				        <p>问题9：你觉得自己的第六感准确吗？</p>
				    </div>
				    <div class="form-check">
				        <input class="form-check-input" type="radio" id="q29a1" name="q29" value="a">
				        <label class="form-check-label" for="q29a1">当然，无论概率多小，只要是我坚信的事情，通通都变为了现实</label>
				    </div>
				    <div class="form-check">
				        <input class="form-check-input" type="radio" id="q29a2" name="q29" value="b">
				        <label class="form-check-label" for="q29a2">他还挺常见的，只是有时候准有时候不准，我也抓不住他</label>
				    </div>
				    <div class="form-check">
				        <input class="form-check-input" type="radio" id="q29a3" name="q29" value="c">
				        <label class="form-check-label" for="q29a3">他只在非常偶然的情况下出现过一次两次，不过每次都帮了我很多</label>
				    </div>
					<div class="form-check">
					    <input class="form-check-input" type="radio" id="q29a4" name="q29" value="d">
					    <label class="form-check-label" for="q29a4">第六感都是虚的， 我没有第六感</label>
					</div>
				</div>
				<div class="test-card">
				    <div class="question">
				        <p>问题10：现在，第六感告诉你，投资房地产将会赚大钱，你会去吗？</p>
				    </div>
				    <div class="form-check">
				        <input class="form-check-input" type="radio" id="q2111a1" name="q2111" value="a">
				        <label class="form-check-label" for="q2111a1">房地产都凉啦，不可能把钱浪费在那种地方</label>
				    </div>
				    <div class="form-check">
				        <input class="form-check-input" type="radio" id="q2111a2" name="q2111" value="b">
				        <label class="form-check-label" for="q2111a2">我回去了解一下，哪怕不投资，多了解一下经济情况也是好的</label>
				    </div>
				    <div class="form-check">
				        <input class="form-check-input" type="radio" id="q2111a3" name="q2111" value="c">
				        <label class="form-check-label" for="q2111a3">我会试试水，选择靠谱的人做谨慎的投资</label>
				    </div>
					<div class="form-check">
					    <input class="form-check-input" type="radio" id="q2111a4" name="q2111" value="d">
					    <label class="form-check-label" for="q2111a4">我会去赚破产的房地产商人的钱</label>
					</div>
				</div>
				<div class="test-card">
				    <div class="question">
				        <p>问题11：现在，你的第六感告诉你，眼前的这个其貌不扬的人会是你命中注定的伴侣，你会去搭讪吗？</p>
				    </div>
				    <div class="form-check">
				        <input class="form-check-input" type="radio" id="q211a1" name="q211" value="a">
				        <label class="form-check-label" for="q211a1">想那么多干嘛，喜欢就去搭讪喽</label>
				    </div>
				    <div class="form-check">
				        <input class="form-check-input" type="radio" id="q211a2" name="q211" value="b">
				        <label class="form-check-label" for="q211a2">记下他的脸，如果有缘分还能再相遇，就去搭讪</label>
				    </div>
				    <div class="form-check">
				        <input class="form-check-input" type="radio" id="q211a3" name="q211" value="c">
				        <label class="form-check-label" for="q211a3">我社恐，张不开嘴</label>
				    </div>
					<div class="form-check">
					    <input class="form-check-input" type="radio" id="q211a4" name="q211" value="d">
					    <label class="form-check-label" for="q211a4">我命中注定的伴侣是赌博和胜利，不是人</label>
					</div>
				</div>
				<div class="test-card">
				    <div class="question">
				        <p>问题12：在学校时期你遵守校规校纪吗？</p>
				    </div>
				    <div class="form-check">
				        <input class="form-check-input" type="radio" id="q212a1" name="q212" value="a">
				        <label class="form-check-label" for="q212a1">我一直有遵守，哪怕有些时候是被迫的</label>
				    </div>
				    <div class="form-check">
				        <input class="form-check-input" type="radio" id="q212a2" name="q212" value="b">
				        <label class="form-check-label" for="q212a2">大多数时候都会遵守，只是偶尔会有一点点无伤大雅的小意外</label>
				    </div>
				    <div class="form-check">
				        <input class="form-check-input" type="radio" id="q212a3" name="q212" value="c">
				        <label class="form-check-label" for="q212a3">什么是校规校纪，那东西我想听的时候听，不想听的时候他就不存在</label>
				    </div>
					<div class="form-check">
					    <input class="form-check-input" type="radio" id="q212a4" name="q212" value="d">
					    <label class="form-check-label" for="q212a4">我很看不惯那些莫名其妙的规则，有时我甚至会刻意违背他们</label>
					</div>
				</div>
				
	
				
                <button type="submit" class="btn btn-primary w-100">提交</button>
            </form>
            <div id="result2" class="result"></div>
            <button type="button" class="btn btn-secondary btn-clear w-100" id="clearButton2">返回选题</button>
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

                // 获取问题 1 的答案
                let q1 = document.querySelector('input[name="q1"]:checked');
                if (q1 && q1.value === 'b') {
                    knowledgeScore += 1;
                }

                let resultText = "";
                if (knowledgeScore >= 1) {
                    resultText = "还在施工";
                } else {
                    resultText = "还在施工";
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
                // 一次性定义所有变量
                let kaisi = 0, heye = 0, chimu = 0, jiuchao = 0, pingshan = 0, shenyu = 0, tian = 0, ling = 0, biao = 0, ya = 0, yiner = 0, sentian = 0;

                // 获取问题 1 的答案
                let q21 = document.querySelector('input[name="q21"]:checked');
                if (q21) {
                    if (q21.value === 'a') {
                        chimu += 1;
                        sentian += 1;
                        biao += 1;
                        shenyu += 1;
                    } else if (q21.value === 'b') {
                        pingshan += 1;
                        ling += 1;
                    } else if (q21.value === 'c') {
                        kaisi += 1;
                        heye += 1;
                        tian += 1;
                    } else if (q21.value === 'd') {
                        jiuchao += 1;
                        yiner += 1;
                        ya += 1;
                    }
                }
			// 获取问题2的答案
			let q22 = document.querySelector('input[name="q22"]:checked');
			if (q22) {
			    if (q22.value === 'a') {
			        tian += 1;
			        ling += 1;
			        yiner += 1;
			        jiuchao += 1;
			    } else if (q22.value === 'b') {
			        sentian += 1;
			        kaisi += 1;
			        heye += 1;
			    } else if (q22.value === 'c') {
			        biao += 1;
			        shenyu += 1;
			        pingshan += 1;
			    } else if (q22.value === 'd') {
			        chimu += 1;
			        ya += 1;
			    }
			}
			
			let q23 = document.querySelector('input[name="q23"]:checked');
			if (q23) {
			    if (q23.value === 'a') {
			        chimu += 1;
			        kaisi += 1;
			        ya += 1;
			    } else if (q23.value === 'b') {
			        shenyu += 1;
			        tian += 1;
			        ling += 1;
			        pingshan += 1;
			    } else if (q23.value === 'c') {
			        heye += 1;
			        sentian += 1;
			        biao += 1;
			    } else if (q23.value === 'd') {
			        jiuchao += 1;
			        yiner += 1;
			        sentian += 1;
			    }
			}
			
			let q24 = document.querySelector('input[name="q24"]:checked');
			if (q24) {
			    if (q24.value === 'a') {
			        ya += 1;
			    } else if (q24.value === 'b') {
			        pingshan += 1;
			        shenyu += 1;
			    } else if (q24.value === 'c') {
			        kaisi += 1;
			        jiuchao += 1;
			        tian += 1;
			        ling += 1;
			        biao += 1;
			    } else if (q24.value === 'd') {
			        chimu += 1;
			        heye += 1;
			        yiner += 1;
			        sentian += 1;
			    }
			}
			
			let q25 = document.querySelector('input[name="q25"]:checked');
			if (q25) {
			    if (q25.value === 'a') {
			        kaisi += 1;
			        heye += 1;
			        jiuchao += 1;
			    } else if (q25.value === 'b') {
			        tian += 1;
			    } else if (q25.value === 'c') {
			        ling += 1;
			        biao += 1;
			    } else if (q25.value === 'd') {
			        yiner += 1;
			        sentian += 1;
			        chimu += 1;
			    } else if (q25.value === 'e') {
			        pingshan += 1;
			        shenyu += 1;
			        ya += 1;
			    }
			}
			
			let q26 = document.querySelector('input[name="q26"]:checked');
			if (q26) {
			    if (q26.value === 'a') {
			        chimu += 1;
			        jiuchao += 1;
			        shenyu += 1;
			        kaisi += 1;
			    } else if (q26.value === 'b') {
			        biao += 1;
			        sentian += 1;
			        tian += 1;
			    } else if (q26.value === 'c') {
			        heye += 1;
			        ling += 1;
			        biao += 1;
			        yiner += 1;
			    } else if (q26.value === 'd') {
			        pingshan += 1;
			        ya += 1;
			    }
			}
			
			let q27 = document.querySelector('input[name="q27"]:checked');
			if (q27) {
			    if (q27.value === 'a') {
			        ling += 1;
			        ya += 1;
			    } else if (q27.value === 'b') {
			        chimu += 1; // 修正拼写错误
			        pingshan += 1;
			    } else if (q27.value === 'c') {
			        heye += 1;
			        tian += 1;
			        shenyu += 1;
			        sentian += 1;
			    } else if (q27.value === 'd') {
			        kaisi += 1;
			        jiuchao += 1;
			        yiner += 1;
			        biao += 1;
			    }
			}
			
			let q28 = document.querySelector('input[name="q28"]:checked');
			if (q28) {
			    if (q28.value === 'a') {
			        kaisi += 1;
			        tian += 1;
			        shenyu += 1;
			    } else if (q28.value === 'b') {
			        // 根据业务逻辑补充代码
			        // 例如这里假设不做任何处理
			    } else if (q28.value === 'c') {
			        heye += 1;
			        jiuchao += 1;
			        pingshan += 1;
			        yiner += 1;
			        biao += 1;
			    } else if (q28.value === 'd') {
			        chimu += 1;
			        sentian += 1;
			        ya += 1;
			        ling += 1;
			    }
			}
			
			let q29 = document.querySelector('input[name="q29"]:checked');
			if (q29) {
			    if (q29.value === 'a') {
			        chimu += 1;
			        jiuchao += 1;
			        shenyu += 1;
			    } else if (q29.value === 'b') {
			        kaisi += 1;
			        yiner += 1;
			        sentian += 1;
			        ling += 1;
			    } else if (q29.value === 'c') {
			        heye += 1;
			        tian += 1;
			        biao += 1;
			    } else if (q29.value === 'd') {
			        pingshan += 1;
			        ya += 1;
			    }
			}
			
			let q2111 = document.querySelector('input[name="q2111"]:checked');
			if (q2111) { // 修正判断变量
			    if (q2111.value === 'a') {
			        kaisi += 1;
			        pingshan += 1;
			        ya += 1;
			    } else if (q2111.value === 'b') {
			        tian += 1;
			        ling += 1;
			    } else if (q2111.value === 'c') {
			        shenyu += 1;
			        biao += 1;
			    } else if (q2111.value === 'd') {
			        heye += 1;
			        chimu += 1;
			        jiuchao += 1;
			        yiner += 1;
			        sentian += 1;
			    }
			}
			
			let q211 = document.querySelector('input[name="q211"]:checked');
			if (q211) {
			    if (q211.value === 'a') {
			        heye += 1;
			        tian += 1;
			        biao += 1;
			    } else if (q211.value === 'b') {
			        pingshan += 1;
			        ling += 1;
			    } else if (q211.value === 'c') {
			        kaisi += 1;
			        ya += 1;
			    } else if (q211.value === 'd') {
			        chimu += 1;
			        jiuchao += 1;
			        shenyu += 1;
			        yiner += 1;
			        sentian += 1;
			    }
			}
			
			let q212 = document.querySelector('input[name="q212"]:checked');
			if (q212) {
			    if (q212.value === 'a') {
			        pingshan += 1;
			        ling += 1;
			        biao += 1;
			    } else if (q212.value === 'b') {
			        kaisi += 1;
			        tian += 1;
			        ya += 1;
			    } else if (q212.value === 'c') {
			        chimu += 1;
			        jiuchao += 1;
			        shenyu += 1;
			        yiner += 1;
			    } else if (q212.value === 'd') {
			        heye += 1;
			        sentian += 1;
			    }
			}
			
			
			
               // 假设这些变量在之前的代码中已经根据用户回答进行了相应的赋值
               // 开司
               kaisi = kaisi * 140 / 12;
               kaisi = kaisi > 100? 100 : kaisi;
               
               // heye
               heye = heye * 140 / 12;
               heye = heye > 100? 100 : heye;
               
               // chimu
               chimu = chimu * 140 / 12;
               chimu = chimu > 100? 100 : chimu;
               
               // jiuchao
               jiuchao = jiuchao * 140 / 12;
               jiuchao = jiuchao > 100? 100 : jiuchao;
               
               // pingshan
               pingshan = pingshan * 140 / 12;
               pingshan = pingshan > 100? 100 : pingshan;
               
               // shenyu
               shenyu = shenyu * 140 / 12;
               shenyu = shenyu > 100? 100 : shenyu;
               
               // tian
               tian = tian * 140 / 12;
               tian = tian > 100? 100 : tian;
               
               // ling
               ling = ling * 140 / 12;
               ling = ling > 100? 100 : ling;
               
               // biao
               biao = biao * 140 / 12;
               biao = biao > 100? 100 : biao;
               
               // ya
               ya = ya * 140 / 12;
               ya = ya > 100? 100 : ya;
               
               // yiner
               yiner = yiner * 140 / 12;
               yiner = yiner > 100? 100 : yiner;
               
               // sentian
               sentian = sentian * 140 / 12;
               sentian = sentian > 100? 100 : sentian;

                let resultTableHTML = '<table class="result-table"><tr><th>角色</th><th>缘分值</th><th>结论</th></tr>';

                // 开司
                let kaisiResult = "";
                if (kaisi < 20) {
                    kaisiResult = "你们的缘分值太浅了，几乎是两个世界的人。就算在大街上路过，见过一两面，也没有办法给彼此留下任何印象。";
                } else if (kaisi < 45) {
                    kaisiResult = "开司是你家附近一只没药救的赌狗，你见过他在输光身上的所有钱之后哭天喊地地向身边人借钱的样子，不知道处于什么目的，你把今天赢到的钱给了他……赌狗太可怕了，看到开司的境况后，你下定决心戒了赌，并且再不跟他来往";
                } else if (kaisi < 70) {
                    kaisiResult = "你赌输钱的时候被开司拉入了伙，赢了一大把。以此为契机，你决定这辈子都认开司做大哥，为他执鞭坠镫，鞍前马后……直到，有人花钱请你坑他一把";
                } else if (kaisi >= 70) {
                    kaisiResult = "作为跟开司同睡一个被窝的伙伴，你已经意识到开司是个无可救药的赌狗了。不过能咋办呢，接受现实吧。平时多长双眼睛盯着他，别又一个不小心欠一屁股高利贷了";
                }
                resultTableHTML += `<tr><td>开司</td><td>${Math.round(kaisi)}%</td><td>${kaisiResult}</td></tr>`;

               let heyeResult = "";
               if (heye < 20) {
                   heyeResult = "你们的缘分值太浅了，几乎是两个世界的人。就算在大街上路过，见过一两面，也没有办法给彼此留下任何印象。";
               } else if(heye < 60){
                   heyeResult = "你是小说家兵藤和也的粉丝，从他刚出道起就一直关注着他了。某次签售会上，你如愿见到了他本人，还拿到了他的亲笔签名，这本书你要收藏一辈子";
                 } else if (heye >= 60){
               			  heyeResult = "你跟和也得缘分很深哦，他还特意以你为素材写过一本小说呢"
               }
               resultTableHTML += `<tr><td>和也</td><td>${Math.round(heye)}%</td><td>${heyeResult}</td></tr>`;
               // 兴趣爱好得分结论
               let chimuResult = "";
               if (chimu < 20) {
                   chimuResult = "你们的缘分值太浅了，几乎是两个世界的人。就算在大街上路过，见过一两面，也没有办法给彼此留下任何印象。";
               } else if(chimu < 60){
                   chimuResult = "赤木是麻将界的传说，你花费了多年的积蓄，才换来跟他打一个半庄的机会……然后……你输了（这似乎是理所当然的）。他嘲讽了你一顿，半夜睡不着回忆的时候，你竟然有种被骂爽了的感觉";
               	   } else if (chimu >= 60){
               			  chimuResult = "你跟赤木的缘分匪浅，你疯狂地迷恋着他，将他作为人生的目标和榜样，幻想着能成为像他一样的人。赤木不擅长人际交往，他尝试过直接给你钱，给你买可以定居的房子和店铺，辞职去其他城市生活，半夜从床上溜走。。。可都没有办法甩开你。最后，他不得不习惯了有你在身边的生活"
               }
               resultTableHTML += `<tr><td>赤木</td><td>${Math.round(chimu)}%</td><td>${chimuResult}</td></tr>`;
               // 兴趣爱好得分结论
               let jiuchaoResult = "";
               if (jiuchao < 20) {
                   jiuchaoResult = "你们的缘分值太浅了，几乎是两个世界的人。就算在大街上路过，见过一两面，也没有办法给彼此留下任何印象。";
               } else if(jiuchao < 60){
                   jiuchaoResult = "你听过鹫巢大人的名字，和他那恐怖的鹫巢麻将。。。所以，你拒绝了麻将代打的请求";
               	 } else if (jiuchao >= 60){
               			  jiuchaoResult = "你跟鹫巢大人的缘分匪浅。帮他在雨夜埋人的是你，站在他身后旁观麻将的是你，帮他拿输血袋的是你，帮他推轮椅的还是你。。。你的一切都是为鹫巢大人而生，你的一切思考都是为了鹫巢大人的利益，你存在的意义就是为鹫巢大人服务，白服已经不是一份简单的工作了，是一种信仰"
               }
               resultTableHTML += `<tr><td>鹫巢</td><td>${Math.round(jiuchao)}%</td><td>${jiuchaoResult}</td></tr>`;
               // 兴趣爱好得分结论
               let pingshanResult = "";
               if (pingshan < 20) {
                   pingshanResult = "你们的缘分值太浅了，几乎是两个世界的人。就算在大街上路过，见过一两面，也没有办法给彼此留下任何印象。";
               } else if(pingshan <= 60){
                   pingshanResult = "你对这个跟黑谁会气质格格不入的年轻人有点印象，不过也不是很深。他大概是某个组织的麻将代打，技术挺不错的。相当长的一段时间后，你才意识到自己已经很久没见过这个异常乖巧的年轻人了。。。他大概是从良了吧，他这样的人，在白道上才能过上好的生活啊";
               	 } else if (pingshan >= 60){
               			  pingshanResult = "悲报，你死了<br>喜报，你埋平山隔壁"
               }
               resultTableHTML += `<tr><td>平山</td><td>${Math.round(pingshan)}%</td><td>${pingshanResult}</td></tr>`;
               // 兴趣爱好得分结论
               let shenyuResult = "";
               if (shenyu < 20) {
                   shenyuResult = "你们的缘分值太浅了，几乎是两个世界的人。就算在大街上路过，见过一两面，也没有办法给彼此留下任何印象。";
               } else if(shenyu < 45){
                   shenyuResult = "你跟他打过几局麻将，这个老登不知道用了什么手法，三四巡就能胡牌还胡得不小，简直不是个人……你不止输光了钱，还憋了一肚子火，这辈子你都不想再跟他碰面了";
               	 } else if(shenyu < 70){
               		 shenyuResult = "他是那个能重塑你xp的男人，你这辈子都离不开他了，你已经完全变成他的形了"
               		  } else if (shenyu >= 70){
               			  shenyuResult = "在神域生命的最后时刻，一直都是你陪在他身边。他的记性越来越差，可如果你想要的话，他还是会陪你搓两局麻将。。。偶尔你逆风翻盘的时候，老头看着你的脸上，会露出欣慰的微笑。。。他输了，他或许不该笑的，这时候的你意识到，哪怕到了现在这种程度，你依旧在被神域先生照顾和宠爱着"
               }
               resultTableHTML += `<tr><td>神域</td><td>${Math.round(shenyu)}%</td><td>${shenyuResult}</td></tr>`;
               // 兴趣爱好得分结论
               let tianResult = "";
               if (tian < 20) {
                   tianResult = "你们的缘分值太浅了，几乎是两个世界的人。就算在大街上路过，见过一两面，也没有办法给彼此留下任何印象。";
               } else if(tian < 45){
                   tianResult = "暂时没写……";
               	 } else if(tian < 70){
               		 tianResult = "暂时没写……"
               		  } else if( tian >= 70){
               			  tianResult = "你跟他的缘分深到什么程度呢，是能到“没有血缘的亲人”的程度，经过多年的感情培养（还有你单方面的心理建设），最终你接受了他的求婚，成为了天家的第三位太太，跟上面的两位姐姐一起，过上了一家四口搓麻的幸福生活"
               }
               resultTableHTML += `<tr><td>天</td><td>${Math.round(tian)}%</td><td>${tianResult}</td></tr>`;
               // 兴趣爱好得分结论
               let lingResult = "";
               if (ling < 20) {
                   lingResult = "你们的缘分值太浅了，几乎是两个世界的人。就算在大街上路过，见过一两面，也没有办法给彼此留下任何印象。";
               } else if(ling < 45){
                   lingResult = "你跟零只是点头之交，从任何角度来看都非常优秀的一个人，令人不解的是他学了如此多的知识却没有一个明确的目标，并且有一股近乎天真的善恶分明的正义感";
               	 } else if(ling < 70){
               		 lingResult = "你是义贼团伙的成员，受到了零的很多帮助，你很佩服零，就算自己没有什么能力也想尽一切可能在他身边帮助他"
               		  } else if( ling >= 70){
               			  lingResult = "你是个比零更厉害的人物，让他难得地用仰视而非俯视的角度去看待你"
               }
               resultTableHTML += `<tr><td>零</td><td>${Math.round(ling)}%</td><td>${lingResult}</td></tr>`;
               // 兴趣爱好得分结论
               let biaoResult = "";
               if (biao < 20) {
                   biaoResult = "你们的缘分值太浅了，几乎是两个世界的人。就算在大街上路过，见过一两面，也没有办法给彼此留下任何印象。";
               } else if(biao < 45){
                   biaoResult = "你在人群中多看了这个小孩一眼，他的特征很突出，但是融入人群的时候不知为何没有什么存在感，但一旦将目光放到他身上就很难再移开了";
               	 } else if(biao < 70){
               		 biaoResult = "你是标大人的狗，你对他各方各面的能力佩服得五体投地，你觉得自己生来就是为了侍奉他保护他的"
               		  } else if( biao >= 70){
               			  biaoResult = "你这个天才的才能获得了标的青睐，让他觉得可以把自己的伟业托付给你，你们约定好了有缘再见"
               }
               resultTableHTML += `<tr><td>标</td><td>${Math.round(biao)}%</td><td>${biaoResult}</td></tr>`;
               // 兴趣爱好得分结论
               let yaResult = "";
               if (ya < 20) {
                   yaResult = "你们的缘分值太浅了，几乎是两个世界的人。就算在大街上路过，见过一两面，也没有办法给彼此留下任何印象。";
               } else if(ya< 45){
                   yaResult = "嗯，楼下新来的这个小保安，体格真不错。细看的话，脸也还可以，虽然有一道疤，但是并不凶。整个人看起来呆呆笨笨的，很好骗的样子……有机会的话，可以……";
               	 } else if(ya < 70){
               		 yaResult = "期初你举得他脸上和手腕上的伤疤充满故事，他的表情像是能杀人一样。了解了之后你觉得这个人其实和普通人没多大差别，就是偶尔会有些固执。但偶尔你也会想说不定他真的是能杀人的那种人"
               		  } else if( ya >= 70){
               			  yaResult = "涯不经常跟外人说话，你是少有的，能听他讲真心话的人。他会跟你说他的人生态度，他对未来的计划，还有他最近看了什么书。你和他的关系好得远超预期——意思是你已经明白了他是个将孤立一词贯彻到底的男人，但如果他需要找人一起合作的话，你是头几个他会想起来的人"
               }
               resultTableHTML += `<tr><td>涯</td><td>${Math.round(ya)}%</td><td>${yaResult}</td></tr>`;
               // 兴趣爱好得分结论
               let yinerResult = "";
               if (yiner < 20) {
                   yinerResult = "你们的缘分值太浅了，几乎是两个世界的人。就算在大街上路过，见过一两面，也没有办法给彼此留下任何印象。";
               } else if(yiner < 45){
                   yinerResult = "你听说过银王的大名，在地下金融界赫赫有名的风云人物，毁掉了很多人的恶魔。。。起初你对他有些恐惧，但当你真的跪在他面前，声泪俱下地恳求他给你一份贷款时，他却只是拍了拍你的肩膀，说他理解你的辛苦，愿意资助你去国外国外躲一段时间，他甚至为你买了保险。。。这一刻，你觉得那些所谓恶魔的传言都是假的，世上还是好人多啊";
               	 } else if(yiner < 70){
               		 yinerResult = "你是被银王捡选出来的年轻人，各种层面上都符合一个完美工具人的要求，你被他诱骗入伙，被他利用来达成某项目的，最后被他抛弃在黑暗街巷的角落"
               		  } else if( yiner >= 70){
               			  yinerResult = "你是银二命中注定的伴侣，你们有着相同的抱负，相同的野心，相同的胆识，相同的命运。你跟在他的身后，重复着他年轻时走过的道道路"
               }
               resultTableHTML += `<tr><td>银二</td><td>${Math.round(yiner)}%</td><td>${yinerResult}</td></tr>`;
               // 兴趣爱好得分结论
               let sentianResult = "";
               if (sentian < 20) {
                   sentianResult = "你们的缘分值太浅了，几乎是两个世界的人。就算在大街上路过，见过一两面，也没有办法给彼此留下任何印象。";
               } else if(sentian < 45){
                   sentianResult = "你们有点儿缘分，某次赌马，你跟在他后面买了同一匹马获胜……结果可想而知，你觉得这个年轻人大概触怒了幸运女神，干啥啥倒霉，幸好你们的缘分也就到此为止，之后再也不会见面了";
               	 } else if(sentian < 70){
               		 sentianResult = "你跟森田共事过那么一两次，他确实是个还算有能力的年轻人，运气也好，但是远远没有达到银王口中非他不可的程度，你不理解为什么银二那么欣赏他……不过硬要说的话，继续跟他共事也挺好的把"
               		  } else if( sentian >= 70){
               			  sentianResult = "你跟森田的关系匪浅，你是能看到他身上与众不同才能得人，他就像是你挖掘的宝藏一样，珍贵，耀眼，并且越来越耀眼……最关键的是，他还像狗狗一样一直都听你的话，你让干啥他干啥，爽的一批"
               }
               resultTableHTML += `<tr><td>森田</td><td>${Math.round(sentian)}%</td><td>${sentianResult}</td></tr>`;
                       

                resultTableHTML += `</table>`;
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

</html>
