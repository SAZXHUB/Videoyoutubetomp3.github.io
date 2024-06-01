<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>YouTube to MP3 Converter</title>
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.2.1/jquery.min.js"></script>
    <script src="https://ytconverter.github.io/converter.js"></script>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f2f2f2;
        }
        .container {
            max-width: 500px;
            margin: 0 auto;
            padding: 20px;
            background-color: #fff;
            border-radius: 5px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        h1 {
            text-align: center;
            color: #333;
        }
        input[type="text"] {
            width: 100%;
            padding: 10px;
            margin-bottom: 10px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        button {
            display: block;
            width: 100%;
            padding: 10px;
            background-color: #4caf50;
            color: #fff;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        button:hover {
            background-color: #45a049;
        }
        .download-link {
            margin-top: 20px;
            text-align: center;
        }
        .download-link a {
            display: inline-block;
            padding: 10px 20px;
            background-color: #3498db;
            color: #fff;
            text-decoration: none;
            border-radius: 5px;
        }
        .download-link a:hover {
            background-color: #2980b9;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>YouTube to MP3 Converter</h1>
        <input type="text" id="youtubeLink" placeholder="Enter YouTube link">
        <button onclick="convertToMP3()">Convert to MP3</button>
        <div class="download-link" id="downloadLink"></div>
    </div>

    <script>
        function convertToMP3() {
            var youtubeLink = document.getElementById("youtubeLink").value;
            YTConverter.getMP3(youtubeLink, function(err, mp3Link) {
                if (err) {
                    console.error("Error:", err);
                } else {
                    var downloadLink = '<a href="' + mp3Link + '" download>Download MP3</a>';
                    document.getElementById("downloadLink").innerHTML = downloadLink;
                }
            });
        }
    </script>
</body>
</html>
