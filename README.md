<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>قائمة مهامي الذكية</title>
    <style>
        body { font-family: sans-serif; background-color: #f4f4f9; display: flex; justify-content: center; padding: 20px; }
        .container { background: white; padding: 20px; border-radius: 10px; box-shadow: 0 4px 6px rgba(0,0,0,0.1); width: 100%; max-width: 400px; }
        h2 { text-align: center; color: #333; }
        .input-group { display: flex; gap: 10px; }
        input { flex: 1; padding: 10px; border: 1px solid #ddd; border-radius: 5px; }
        button { padding: 10px; background-color: #28a745; color: white; border: none; border-radius: 5px; cursor: pointer; }
        ul { list-style: none; padding: 0; margin-top: 20px; }
        li { background: #eee; margin-bottom: 5px; padding: 10px; border-radius: 5px; display: flex; justify-content: space-between; }
    </style>
</head>
<body>

<div class="container">
    <h2>قائمة المهام</h2>
    <div class="input-group">
        <input type="text" id="taskInput" placeholder="اكتب مهمة جديدة...">
        <button onclick="addTask()">إضافة</button>
    </div>
    <ul id="taskList">
        </ul>
</div>

<script>
    function addTask() {
        let input = document.getElementById('taskInput');
        let ul = document.getElementById('taskList');
        if (input.value.trim() !== "") {
            let li = document.createElement('li');
            li.textContent = input.value;
            ul.appendChild(li);
            input.value = ""; // تفريغ الحقل بعد الإضافة
        }
    }
</script>

</body>
</html>
