
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>YouTube Converter</title>
</head>
<body>
    <h1>YouTube Converter</h1>
    <h2>Convert YouTube Video to MP3</h2>
    <input type="text" id="mp3Link" placeholder="Enter YouTube link">
    <button onclick="convertToMP3()">Convert to MP3</button>
    <div id="mp3DownloadLink"></div>

    <h2>Convert YouTube Video to MP4</h2>
    <input type="text" id="mp4Link" placeholder="Enter YouTube link">
    <button onclick="convertToMP4()">Convert to MP4</button>
    <div id="mp4DownloadLink"></div>

    <script>
        function convertToMP3() {
            var mp3Link = document.getElementById("mp3Link").value;
            var mp3DownloadLink = document.getElementById("mp3DownloadLink");
            mp3DownloadLink.innerHTML = '<iframe src="https://api.vevioz.com/@api/button/mp3/' + mp3Link + '" style="width:100%;height:150px;border:none;" scrolling="no"></iframe>';
        }

        function convertToMP4() {
            var mp4Link = document.getElementById("mp4Link").value;
            var mp4DownloadLink = document.getElementById("mp4DownloadLink");
            mp4DownloadLink.innerHTML = '<iframe src="https://api.vevioz.com/@api/button/videos/1080/' + mp4Link + '" style="width:100%;height:150px;border:none;" scrolling="no"></iframe>';
        }
    </script>
</body>
</html>
