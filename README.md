<!DOCTYPE html>
<html>
<head>
    <title>OAuth Callback</title>
</head>
<body>
    <h1>Authorization Successful!</h1>
    <p>Copy this code and use it in Discord:</p>
    <input type="text" id="code" readonly style="width: 100%; padding: 10px;">
    <button onclick="copyCode()">Copy Code</button>
    
    <script>
        const urlParams = new URLSearchParams(window.location.search);
        const code = urlParams.get('code');
        document.getElementById('code').value = code;
        
        function copyCode() {
            document.getElementById('code').select();
            document.execCommand('copy');
            alert('Code copied!');
        }
    </script>
</body>
</html>
