# tin-bai-9
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
