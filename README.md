<!DOCTYPE html>
<html lang="ko">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>랜덤 문자열 생성</title>
<style>
    body {
        font-family: Arial, sans-serif;
        text-align: center;
        margin: 50px;
    }
    button {
        font-size: 18px;
        padding: 10px 20px;
        cursor: pointer;
        background-color: #007bff;
        color: white;
        border: none;
        border-radius: 5px;
    }
    button:hover {
        background-color: #0056b3;
    }
    #result {
        margin-top: 20px;
        font-size: 24px;
    }
</style>
</head>
<body>
    <h1>랜덤 문자열 생성기</h1>
    <button id="generateBtn">랜덤 문자열 생성</button>
    <div id="result"></div>

    <script>
        function generateRandomString() {
            const characters = 'ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789!@#?_';
            let result = '';
            const length = 8;
            for (let i = 0; i < length; i++) {
                const randomIndex = Math.floor(Math.random() * characters.length);
                result += characters[randomIndex];
            }
            return result;
        }

        const generateBtn = document.getElementById('generateBtn');
        generateBtn.addEventListener('click', function() {
            const randomString = generateRandomString();
            const resultDiv = document.getElementById('result');
            resultDiv.textContent = '생성된 문자열: ' + randomString;
        });
    </script>
</body>
</html>
