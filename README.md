# note.app
<!DOCTYPE html>
<html lang="zh-Hant">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>簡易筆記 App</title>
</head>
<body>
  <h2>我的筆記</h2>
  <textarea id="note" rows="12" style="width:100%;" placeholder="輸入筆記內容…"></textarea>
  <br><br>
  <button onclick="saveNote()">儲存</button>
  <button onclick="loadNote()">讀取</button>

  <script>
    function saveNote() {
      localStorage.setItem("myNote", document.getElementById("note").value);
      alert("筆記已儲存");
    }
    function loadNote() {
      document.getElementById("note").value =
        localStorage.getItem("myNote") || "";
    }
  </script>
</body>
</html>
