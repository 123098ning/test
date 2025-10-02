<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>心算测试 - 连续减法挑战</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://cdn.jsdelivr.net/npm/font-awesome@4.7.0/css/font-awesome.min.css" rel="stylesheet">
    
    <!-- 配置Tailwind自定义颜色和字体 -->
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        primary: '#3B82F6',
                        secondary: '#10B981',
                        danger: '#EF4444',
                        dark: '#1E293B',
                        light: '#F8FAFC'
                    },
                    fontFamily: {
                        sans: ['Inter', 'system-ui', 'sans-serif'],
                    },
                }
            }
        }
    </script>
    
    <style type="text/tailwindcss">
        @layer utilities {
            .content-auto {
                content-visibility: auto;
            }
            .text-shadow {
                text-shadow: 0 2px 4px rgba(0,0,0,0.1);
            }
            .transition-custom {
                transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
            }
        }
    </style>
</head>
<body class="bg-gradient-to-br from-light to-blue-50 min-h-screen font-sans text-dark flex flex-col items-center justify-center p-4">
    <!-- 主容器 -->
    <div class="max-w-md w-full bg-white rounded-2xl shadow-xl overflow-hidden transform transition-all duration-500">
        <!-- 开始界面 -->
        <div id="start-screen" class="p-8 text-center">
            <div class="mb-8">
                <i class="fa fa-calculator text-primary text-6xl mb-4 animate-pulse"></i>
                <h1 class="text-[clamp(2rem,5vw,3rem)] font-bold text-dark mb-2 text-shadow">数字测试</h1>
                <p class="text-gray-600 text-lg">挑战你的心算能力</p>
            </div>
            
            <div class="mb-8 bg-blue-50 rounded-xl p-6 text-left">
                <h2 class="font-semibold text-lg mb-3 flex items-center">
                    <i class="fa fa-info-circle text-primary mr-2"></i>测试说明
                </h2>
                <ul class="space-y-2 text-gray-700">
                    <li class="flex items-start">
                        <i class="fa fa-check-circle text-secondary mt-1 mr-2"></i>
                        <span>从2025开始，连续减去17</span>
                    </li>
                    <li class="flex items-start">
                        <i class="fa fa-check-circle text-secondary mt-1 mr-2"></i>
                        <span>每次计算有15秒时间限制</span>
                    </li>
                    <li class="flex items-start">
                        <i class="fa fa-check-circle text-secondary mt-1 mr-2"></i>
                        <span>超时或答错均从2025重新开始</span>
                    </li>
                    <li class="flex items-start">
                        <i class="fa fa-check-circle text-secondary mt-1 mr-2"></i>
                        <span>测试将在5分钟后结束</span>
                    </li>
                </ul>
            </div>
            
            <button id="start-btn" class="w-full bg-primary hover:bg-primary/90 text-white font-bold py-3 px-6 rounded-lg shadow-lg hover:shadow-xl transform hover:-translate-y-1 transition-custom flex items-center justify-center">
                <i class="fa fa-play mr-2"></i> 开始测试
            </button>
        </div>
        
        <!-- 测试界面 -->
        <div id="test-screen" class="p-8 hidden">
            <!-- 进度和计时 -->
            <div class="flex justify-between items-center mb-6">
                <div class="bg-gray-100 rounded-full px-4 py-2 flex items-center">
                    <i class="fa fa-history text-primary mr-2"></i>
                    <span id="current-streak" class="font-medium">当前连续: 0</span>
                </div>
                <div class="bg-gray-100 rounded-full px-4 py-2 flex items-center">
                    <i class="fa fa-clock-o text-primary mr-2"></i>
                    <span id="test-timer" class="font-medium">5:00</span>
                </div>
            </div>
            
            <!-- 题目计时器 -->
            <div class="w-full bg-gray-200 rounded-full h-2.5 mb-8">
                <div id="question-timer-bar" class="bg-primary h-2.5 rounded-full transition-all duration-1000" style="width: 100%"></div>
            </div>
            
            <!-- 题目 -->
            <div class="mb-8 text-center">
                <p class="text-gray-600 mb-2">请计算：</p>
                <h2 id="question" class="text-[clamp(1.8rem,5vw,2.5rem)] font-bold text-dark">2025 - 17 = ?</h2>
            </div>
            
            <!-- 答案输入 -->
            <div class="mb-6">
                <input type="number" id="answer" 
                       class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-primary focus:border-primary text-xl transition-custom"
                       placeholder="请输入答案" autocomplete="off" inputmode="numeric">
            </div>
            
            <!-- 反馈信息 -->
            <div id="feedback" class="mb-6 h-8 text-center hidden"></div>
            
            <!-- 提交按钮 -->
            <button id="submit-btn" class="w-full bg-primary hover:bg-primary/90 text-white font-bold py-3 px-6 rounded-lg shadow-lg hover:shadow-xl transform hover:-translate-y-1 transition-custom disabled:opacity-50 disabled:cursor-not-allowed disabled:hover:-translate-y-0">
                提交答案
            </button>
        </div>
        
        <!-- 结束界面 -->
        <div id="end-screen" class="p-8 text-center hidden">
            <div class="mb-8">
                <i class="fa fa-check-circle text-6xl mb-4 text-secondary"></i>
                <h2 class="text-2xl font-bold mb-4">测试完毕</h2>
                <p class="text-gray-600 text-lg">请返回问卷继续答题</p>
            </div>
            
            <div class="bg-gray-50 rounded-xl p-6 mb-8">
                <h3 class="font-semibold text-gray-700 mb-3">测试统计</h3>
                <div class="flex justify-between items-center mb-2">
                    <span class="text-gray-600">最长连续正确</span>
                    <span id="max-streak" class="font-bold">0</span>
                </div>
                <div class="flex justify-between items-center">
                    <span class="text-gray-600">总正确次数</span>
                    <span id="total-correct" class="font-bold">0</span>
                </div>
            </div>
            
            <button id="restart-btn" class="w-full bg-primary hover:bg-primary/90 text-white font-bold py-3 px-6 rounded-lg shadow-lg hover:shadow-xl transform hover:-translate-y-1 transition-custom">
                <i class="fa fa-refresh mr-2"></i> 重新测试
            </button>
        </div>
    </div>
    
    <script>
        // 全局变量
        let currentNumber = 2025;
        let currentStreak = 0;
        let maxStreak = 0;
        let totalCorrect = 0;
        let questionTimerInterval;
        let testTimerInterval;
        let timeLeft = 15; // 每题15秒
        let totalTestTime = 300; // 总测试时间5分钟(300秒)
        
        // DOM元素
        const startScreen = document.getElementById('start-screen');
        const testScreen = document.getElementById('test-screen');
        const endScreen = document.getElementById('end-screen');
        const startBtn = document.getElementById('start-btn');
        const submitBtn = document.getElementById('submit-btn');
        const restartBtn = document.getElementById('restart-btn');
        const answerInput = document.getElementById('answer');
        const questionElement = document.getElementById('question');
        const currentStreakElement = document.getElementById('current-streak');
        const testTimerElement = document.getElementById('test-timer');
        const questionTimerBar = document.getElementById('question-timer-bar');
        const feedbackElement = document.getElementById('feedback');
        const maxStreakElement = document.getElementById('max-streak');
        const totalCorrectElement = document.getElementById('total-correct');
        
        // 开始测试
        startBtn.addEventListener('click', startTest);
        
        // 提交答案
        submitBtn.addEventListener('click', checkAnswer);
        
        // 回车键提交答案
        answerInput.addEventListener('keypress', (e) => {
            if (e.key === 'Enter') {
                checkAnswer();
            }
        });
        
        // 重新测试
        restartBtn.addEventListener('click', resetTest);
        
        // 开始测试函数
        function startTest() {
            startScreen.classList.add('hidden');
            testScreen.classList.remove('hidden');
            
            // 重置测试数据
            resetTestData();
            
            // 开始计时
            startQuestionTimer();
            startTestTimer();
            
            // 聚焦输入框
            answerInput.focus();
        }
        
        // 重置测试数据
        function resetTestData() {
            currentNumber = 2025;
            currentStreak = 0;
            totalCorrect = 0;
            timeLeft = 15;
            updateQuestion();
            updateStreakDisplay();
        }
        
        // 检查答案
        function checkAnswer() {
            // 清除当前题目的计时器
            clearInterval(questionTimerInterval);
            
            const userAnswer = parseInt(answerInput.value);
            const correctAnswer = currentNumber - 17;
            
            // 检查答案是否正确
            if (userAnswer === correctAnswer) {
                // 答案正确
                totalCorrect++;
                currentStreak++;
                maxStreak = Math.max(maxStreak, currentStreak);
                showFeedback('正确！', 'text-secondary');
                
                // 更新当前数字
                currentNumber = correctAnswer;
                
                // 准备下一题
                setTimeout(() => {
                    feedbackElement.classList.add('hidden');
                    answerInput.value = '';
                    timeLeft = 15;
                    updateQuestion();
                    startQuestionTimer();
                    answerInput.focus();
                }, 1000);
            } else {
                // 答案错误，重新开始
                showFeedback(`错误，正确答案是 ${correctAnswer}，将重新开始`, 'text-danger');
                
                setTimeout(() => {
                    feedbackElement.classList.add('hidden');
                    answerInput.value = '';
                    resetTestData();
                    startQuestionTimer();
                    answerInput.focus();
                }, 2000);
            }
            
            updateStreakDisplay();
        }
        
        // 显示反馈信息
        function showFeedback(message, colorClass) {
            feedbackElement.textContent = message;
            feedbackElement.className = `mb-6 h-8 text-center font-medium ${colorClass}`;
            feedbackElement.classList.remove('hidden');
        }
        
        // 更新题目
        function updateQuestion() {
            questionElement.textContent = `${currentNumber} - 17 = ?`;
        }
        
        // 更新连续正确显示
        function updateStreakDisplay() {
            currentStreakElement.textContent = `当前连续: ${currentStreak}`;
        }
        
        // 开始题目计时器
        function startQuestionTimer() {
            updateQuestionTimerDisplay();
            
            questionTimerInterval = setInterval(() => {
                timeLeft--;
                updateQuestionTimerDisplay();
                
                // 超时处理
                if (timeLeft <= 0) {
                    clearInterval(questionTimerInterval);
                    showFeedback('时间到！将重新开始', 'text-danger');
                    
                    setTimeout(() => {
                        feedbackElement.classList.add('hidden');
                        answerInput.value = '';
                        resetTestData();
                        startQuestionTimer();
                        answerInput.focus();
                    }, 2000);
                }
            }, 1000);
        }
        
        // 更新题目计时器显示
        function updateQuestionTimerDisplay() {
            const percentage = (timeLeft / 15) * 100;
            questionTimerBar.style.width = `${percentage}%`;
            
            // 时间快用完时变色提醒
            if (timeLeft <= 5) {
                questionTimerBar.classList.remove('bg-primary');
                questionTimerBar.classList.add('bg-danger');
            } else {
                questionTimerBar.classList.remove('bg-danger');
                questionTimerBar.classList.add('bg-primary');
            }
        }
        
        // 开始总测试计时器
        function startTestTimer() {
            updateTestTimerDisplay();
            
            testTimerInterval = setInterval(() => {
                totalTestTime--;
                updateTestTimerDisplay();
                
                // 测试时间结束
                if (totalTestTime <= 0) {
                    endTest();
                }
            }, 1000);
        }
        
        // 更新总测试计时器显示
        function updateTestTimerDisplay() {
            const minutes = Math.floor(totalTestTime / 60);
            const seconds = totalTestTime % 60;
            testTimerElement.textContent = `${minutes}:${seconds < 10 ? '0' + seconds : seconds}`;
            
            // 最后10秒变红提醒
            if (totalTestTime <= 10) {
                testTimerElement.classList.add('text-danger');
            } else {
                testTimerElement.classList.remove('text-danger');
            }
        }
        
        // 结束测试
        function endTest() {
            // 清除所有计时器
            clearInterval(questionTimerInterval);
            clearInterval(testTimerInterval);
            
            // 显示结束界面
            testScreen.classList.add('hidden');
            endScreen.classList.remove('hidden');
            
            // 更新统计信息
            maxStreakElement.textContent = maxStreak;
            totalCorrectElement.textContent = totalCorrect;
        }
        
        // 重置测试
        function resetTest() {
            // 清除所有计时器
            clearInterval(questionTimerInterval);
            clearInterval(testTimerInterval);
            
            // 重置时间
            totalTestTime = 300;
            timeLeft = 15;
            
            // 重置统计
            maxStreak = 0;
            
            // 切换到开始界面
            endScreen.classList.add('hidden');
            startScreen.classList.remove('hidden');
            
            // 重置UI
            answerInput.value = '';
            questionElement.textContent = '2025 - 17 = ?';
            testTimerElement.classList.remove('text-danger');
            questionTimerBar.classList.remove('bg-danger');
            questionTimerBar.classList.add('bg-primary');
        }
    </script>
</body>
</html>
