# TOOL CRAWL DỮ LIỆU THỜI KHÓA BIỂU HCMUTE - SỬ DỤNG SELENIUM PYTHON
## Giới thiệu
Đây là một Project cuối kỳ môn Tin học trong kỹ thuật sử dụng thư viện Selenium để crawl dữ liệu thời khóa biểu của trường ĐH SPKT (HCMUTE).

[Link video báo cáo](https://www.youtube.com/watch?v=xUdoQLjIr50&t=10s)

## Tài nguyên
* Thư viện Selenium Python - [Tài liệu tham khảo!](https://selenium-python.readthedocs.io/)
* Microsoft Edge Driver - [Link tải bản mới nhất!](https://developer.microsoft.com/en-us/microsoft-edge/tools/webdriver/)

## Ghi chú
Những option này giúp tắt các lỗi hay gặp khi sử dụng MSEdge Driver, và còn nhằm mục đích cho driver chạy ngầm, không hiển thị lên màn hình.
```python
options = EdgeOptions()
options.use_chromium = True
options.add_argument('headless')
options.add_argument('window-size=1920x1080')
options.add_argument("disable-gpu")
options.binary_location = r"C:\Program Files (x86)\Microsoft\Edge\Application\msedge.exe"
driver = Edge(executable_path='.\Driver\msedgedriver.exe', options=options)
```
## Tool sẽ xuất ra một file JSON dạng như sau
```json
{
  "THỨ 2": [
    {
      "Tên môn: ": "Giáo dục quốc phòng 1(ĐH) [1]",
      "Giờ học: ": "07g00 -> 11g30",
      "Tiết học: ": "Tiết 1-5",
      "Giáo viên: ": "GV: Trịnh Công Tứ",
      "Phòng học: ": "QP402"
    },
    {
      "Tên môn: ": "Sức bền vật liệu [3]",
      "Giờ học: ": "12g30 -> 15g10",
      "Tiết học: ": "Tiết 7-9",
      "Giáo viên: ": "GV: Nguyễn Thị Bích Liễu",
      "Phòng học: ": "A4-402"
    },
    {
      "Tên môn: ": "Toán ứng dụng –Cơ khí [3]",
      "Giờ học: ": "15g10 -> 17g50",
      "Tiết học: ": "Tiết 10-12",
      "Giáo viên: ": "GV: Nguyễn Vũ Lân",
      "Phòng học: ": "A4-302"
    }
  ],
  "THỨ 3": [
    {
      "Tên môn: ": "Giáo dục quốc phòng 3(ĐH) [2]",
      "Giờ học: ": "12g30 -> 17g50",
      "Tiết học: ": "Tiết 7-12",
      "Giáo viên: ": "GV: Trịnh Công Tứ",
      "Phòng học: ": "QPNT08"
    }
  ],
  "THỨ 4": [
    {
      "Tên môn: ": "Kỹ thuật điện – Điện tử [3]",
      "Giờ học: ": "08g50 -> 11g30",
      "Tiết học: ": "Tiết 3-5",
      "Giáo viên: ": "GV: Vũ Quang Huy",
      "Phòng học: ": "NI ACADEMY"
    }
  ],
  "THỨ 5": [
    {
      "Tên môn: ": "Lập trình ứng dụng trong kỹ thuật [3]",
      "Giờ học: ": "07g00 -> 10g30",
      "Tiết học: ": "Tiết 1-4",
      "Giáo viên: ": "GV: Trần Nhật Quang",
      "Phòng học: ": "A2-402"
    }
  ],
  "THỨ 6": [
    {
      "Tên môn: ": "Toán 3 [3]",
      "Giờ học: ": "12g30 -> 15g10",
      "Tiết học: ": "Tiết 7-9",
      "Giáo viên: ": "GV: Bành Đức Dũng",
      "Phòng học: ": "A2-303"
    }
  ],
  "THỨ 7": []
}
```
