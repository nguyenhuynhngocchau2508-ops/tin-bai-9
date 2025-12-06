# tin-bai-9
<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bài 9 – Tin học 12</title>
    <style>
        body {font-family: Arial, sans-serif; padding: 20px; line-height: 1.6; background: #f5f5f5;}
        h1, h2 {color: #0f3e8a;}
        pre {background: #e5e7eb; padding: 10px; border-radius: 6px; overflow-x: auto;}
        code {background: #f3f4f6; padding: 2px 4px; border-radius: 4px;}
        .section {margin-bottom: 30px;}
    </style>
</head>
<body>

<h1>BÀI 9 – TIN HỌC 12</h1>

<div class="section">
    <h2>Câu hỏi trang 53</h2>
    <p><strong>Hỏi:</strong> Làm thế nào để tạo một danh sách lồng nhau với mức 1 đánh số 1, 2, 3,… và mức 2 dạng a, b, c?</p>

    <p><strong>Lời giải:</strong></p>
    <p>Sử dụng thẻ <code>&lt;ol&gt;</code> cho danh sách mức 1 và <code>&lt;ol type="a"&gt;</code> cho danh sách mức 2.</p>

    <pre><code>&lt;ol&gt;
    &lt;li&gt;Item 1&lt;/li&gt;
    &lt;li&gt;Item 2&lt;/li&gt;
    &lt;li&gt;Item 3
        &lt;ol type="a"&gt;
            &lt;li&gt;Subitem 1&lt;/li&gt;
            &lt;li&gt;Subitem 2&lt;/li&gt;
            &lt;li&gt;Subitem 3&lt;/li&gt;
        &lt;/ol&gt;
    &lt;/li&gt;
    &lt;li&gt;Item 4&lt;/li&gt;
&lt;/ol&gt;</code></pre>
</div>

<hr>

<div class="section">
    <h2>Câu hỏi trang 55</h2>
    <p><strong>Nhược điểm của bảng Hình 9.6:</strong> Các cột lồng nhau gây khó khăn cho việc nhập liệu.</p>
    <p><strong>Cách khắc phục:</strong> Tách các cột nhỏ thành các cột lớn riêng biệt để dễ nhìn và dễ nhập.</p>
</div>

<hr>

<div class="section">
    <h2>Luyện tập trang 56</h2>
    <p><strong>Yêu cầu:</strong> Sửa chương trình Hình 9.5a, dùng thuộc tính <code>style</code> để tạo viền và gán màu.</p>

    <pre><code>&lt;table style="border-collapse: collapse;"&gt;
    &lt;tr&gt;
        &lt;th rowspan="2" style="border: 2px solid blue;"&gt;Họ tên&lt;/th&gt;
        &lt;th colspan="3" style="border: 2px solid blue;"&gt;Điểm thi&lt;/th&gt;
    &lt;/tr&gt;

    &lt;tr&gt;
        &lt;td style="border: 2px solid red;"&gt;Toán&lt;/td&gt;
        &lt;td style="border: 2px solid yellow;"&gt;Vật lí&lt;/td&gt;
        &lt;td style="border: 2px solid green;"&gt;Hóa học&lt;/td&gt;
    &lt;/tr&gt;
&lt;/table&gt;</code></pre>
</div>

<hr>

<div class="section">
    <h2>Vận dụng trang 56</h2>
    <p><strong>Yêu cầu:</strong> Viết chương trình Python tạo tệp HTML chứa bảng dữ liệu nx4.</p>

    <pre><code>def generate_html_table(data):
    html_content = "&lt;table style='border-collapse: collapse;'&gt;"

    # Tiêu đề bảng
    html_content += "&lt;tr&gt;"
    html_content += "&lt;th style='border:2px solid blue;'&gt;Họ tên&lt;/th&gt;"
    html_content += "&lt;th style='border:2px solid blue;'&gt;Điểm Toán&lt;/th&gt;"
html_content += "&lt;th style='border:2px solid blue;'&gt;Điểm Vật lí&lt;/th&gt;"
    html_content += "&lt;th style='border:2px solid blue;'&gt;Điểm Hóa học&lt;/th&gt;"
    html_content += "&lt;/tr&gt;"

    # Dữ liệu bảng
    for row in data:
        html_content += "&lt;tr&gt;"
        for value in row:
            html_content += f"&lt;td style='border:1px solid black;'&gt;{value}&lt;/td&gt;"
        html_content += "&lt;/tr&gt;"

    html_content += "&lt;/table&gt;"
    return html_content


# Dữ liệu mẫu
initial_data = [
    ["Nguyễn Văn A", "8.5", "7.0", "9.0"],
    ["Trần Thị B", "7.0", "8.0", "8.5"]
]

new_data = [
    ["Lê Quang C", "6.5", "7.5", "8.0"],
    ["Phạm Thị D", "9.0", "8.5", "7.5"]
]

combined_data = initial_data + new_data

html_content = generate_html_table(combined_data)

with open("data_table.html", "w", encoding="utf-8") as file:
    file.write(html_content)

print("Tạo tệp HTML thành công!")</code></pre>

</div>

</body>
</html>
