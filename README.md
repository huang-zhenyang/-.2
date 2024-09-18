<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>图片展示</title>
    <style>
       .thumbnail {
            width: 100px;
            height: 100px; /* 统一高度 */
            object-fit: cover; /* 保持比例，裁剪多余部分 */
            cursor: pointer;
            margin: 5px;
        }
        #largeImage {
           display: block; /* 默认显示大图 */
            width: 400px;
            height: 400px; /* 统一高度 */
            object-fit: cover; /* 保持比例，裁剪多余部分 */
            margin-top: 20px;
        }
    </style>
</head>
<body>
<h1>点击小图片查看大图</h1>
<img src="作业图片/避火罩.png" class="thumbnail" onclick="showImage(this.src)">
<img src="作业图片/定风珠.png" class="thumbnail" onclick="showImage(this.src)">
<img src="作业图片/绣花针.png" class="thumbnail" onclick="showImage(this.src)">
<img src="作业图片/芭蕉扇.png" class="thumbnail" onclick="showImage(this.src)">
<img src="作业图片/不能.png" class="thumbnail" onclick="showImage(this.src)">

<img id="largeImage" src="" alt="大图">

<script>
        function showImage(src) {
            const largeImage = document.getElementById('largeImage');
            largeImage.src = src; // 使用小图片的 src
        }

        // 页面加载时显示第一张图片
        window.onload = function() {
            const firstThumbnail = document.querySelector('.thumbnail');
            showImage(firstThumbnail.src);
        }
    </script>
</body>
</html>
