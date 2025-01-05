# Passive-Voice-Test
<!DOCTYPE html>
<html lang="az">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Passive Voice Test</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            text-align: center;
            margin: 0;
            padding: 0;
        }
        .container {
            max-width: 700px;
            margin: 50px auto;
            padding: 20px;
            background: white;
            border-radius: 10px;
            box-shadow: 0 0 15px rgba(0,0,0,0.1);
        }
        h1 {
            color: #333;
        }
        .question {
            margin: 15px 0;
            text-align: left;
        }
        button {
            background-color: #4CAF50;
            color: white;
            border: none;
            padding: 10px 20px;
            border-radius: 5px;
            cursor: pointer;
            margin-top: 20px;
        }
        button:hover {
            background-color: #45a049;
        }
        #result {
            margin-top: 20px;
            font-size: 22px;
            font-weight: bold;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Passive Voice Test</h1>
        <form id="quizForm">
            <!-- Sual 1 -->
            <div class="question">
                <p>1. The letter ___ (send) yesterday.</p>
                <input type="radio" name="q1" value="a"> a) is sent<br>
                <input type="radio" name="q1" value="b"> b) was sent<br>
                <input type="radio" name="q1" value="c"> c) will be sent<br>
            </div>

            <!-- Sual 2 -->
            <div class="question">
                <p>2. The cake ___ (bake) every weekend.</p>
                <input type="radio" name="q2" value="a"> a) is baked<br>
                <input type="radio" name="q2" value="b"> b) was baked<br>
                <input type="radio" name="q2" value="c"> c) will be baked<br>
            </div>

            <!-- Sual 3 -->
            <div class="question">
                <p>3. The book ___ (read) by the students now.</p>
                <input type="radio" name="q3" value="a"> a) is read<br>
                <input type="radio" name="q3" value="b"> b) is being read<br>
                <input type="radio" name="q3" value="c"> c) was being read<br>
            </div>

            <!-- Sual 4 -->
            <div class="question">
                <p>4. This house ___ (build) in 1990.</p>
                <input type="radio" name="q4" value="a"> a) was built<br>
                <input type="radio" name="q4" value="b"> b) is built<br>
                <input type="radio" name="q4" value="c"> c) will be built<br>
            </div>

            <!-- Sual 5 -->
            <div class="question">
                <p>5. The work ___ (finish) tomorrow.</p>
                <input type="radio" name="q5" value="a"> a) is finished<br>
                <input type="radio" name="q5" value="b"> b) will be finished<br>
                <input type="radio" name="q5" value="c"> c) was finished<br>
            </div>

            <!-- Sual 6 -->
            <div class="question">
                <p>6. My room ___ (clean) yesterday.</p>
                <input type="radio" name="q6" value="a"> a) was cleaned<br>
                <input type="radio" name="q6" value="b"> b) is cleaned<br>
                <input type="radio" name="q6" value="c"> c) will be cleaned<br>
            </div>

            <!-- Sual 7 -->
            <div class="question">
                <p>7. The report ___ (prepare) by the manager now.</p>
                <input type="radio" name="q7" value="a"> a) is being prepared<br>
                <input type="radio" name="q7" value="b"> b) has been prepared<br>
                <input type="radio" name="q7" value="c"> c) was prepared<br>
            </div>

            <!-- Sual 8 -->
            <div class="question">
                <p>8. The package ___ (deliver) next week.</p>
                <input type="radio" name="q8" value="a"> a) will be delivered<br>
                <input type="radio" name="q8" value="b"> b) is delivered<br>
                <input type="radio" name="q8" value="c"> c) was delivered<br>
            </div>

            <!-- Sual 9 -->
            <div class="question">
                <p>9. The project ___ (complete) last month.</p>
                <input type="radio" name="q9" value="a"> a) was completed<br>
                <input type="radio" name="q9" value="b"> b) is completed<br>
                <input type="radio" name="q9" value="c"> c) has been completed<br>
            </div>

            <!-- Sual 10 -->
            <div class="question">
                <p>10. The food ___ (serve) now.</p>
                <input type="radio" name="q10" value="a"> a) is being served<br>
                <input type="radio" name="q10" value="b"> b) was served<br>
                <input type="radio" name="q10" value="c"> c) will be served<br>
            </div>

            <!-- Yoxla Butonu -->
            <button type="button" onclick="checkAnswers()">Yoxla</button>
        </form>

        <!-- Nəticə -->
        <div id="result"></div>
    </div>

    <!-- JavaScript Kodu -->
    <script>
        function checkAnswers() {
            const answers = {
                q1: "b", q2: "a", q3: "b", q4: "a", q5: "b",
                q6: "a", q7: "a", q8: "a", q9: "a", q10: "a"
            };
            let score = 0;

            for (const question in answers) {
                const selectedOption = document.querySelector(`input[name="${question}"]:checked`);
                if (selectedOption && selectedOption.value === answers[question]) {
                    score += 10;
                }
            }

            const resultDiv = document.getElementById('result');
            if (score === 100) {
                resultDiv.innerHTML = `<p style="color:green; font-size:24px;">TƏBRİKLƏR! Xalınız: ${score}</p>`;
            } else {
                resultDiv.innerHTML = `<p style="color:red; font-size:24px;">MƏLƏSF, BİRAZ ÇALIŞMALISIN. Xalınız: ${score}</p>`;
            }
        }
    </script>
</body>
</html>
