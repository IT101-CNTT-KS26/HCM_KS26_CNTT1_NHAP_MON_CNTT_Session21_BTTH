# BÀI TẬP TỔNG HỢP (SESSION 21)
## Phần 1 - Googling đúng cách
### **1.** Giải thích vì sao câu hỏi "văn nói" ở mục 3b khiến Google trả về kết quả kém chất lượng.

- Vì Google không phải là con người, khi gõ câu "tại sao em cài node xong mà gõ npm nó không nhận vậy thầy ơi" Google sẽ tìm kiếm những bài viết trên mạng có chứa từ "thầy ơi", "tại sao", "em". Kết quả là nó sẽ dẫn bạn vào các trang tâm sự học đường, hoặc các diễn đàn hỏi đáp linh tinh thay vì các trang web chuyên về kỹ thuật.

### **2.** Bóc tách lỗi ở mục 3a theo **3 thành phần cốt lõi**:

| Thành phần | Nội dung |
| :--- | :--- |
| Tên phần mềm/Hệ điều hành | Node.js, npm, Windows 11, VS Code |
| Mã lỗi nguyên văn | 'npm' is not recognized as an internal or external command, operable program or batch file. |
| Thao tác đang làm | Gõ lệnh npm -v trong Terminal của VS Code. |

### **3.** 3. Viết **3 câu truy vấn Google** tối ưu, mỗi câu dùng 1 toán tử khác nhau:
- 1 câu giới hạn trong StackOverflow (site:)

    -> Dùng site: giới hạn StackOverflow: npm is not recognized site:stackoverflow.com

- 1 câu dùng ngoặc kép cho lỗi nguyên văn (" ")
   
   -> Dùng " " tìm chính xác lỗi: "npm' is not recognized as an internal or external command"

- 1 câu loại trừ các bài viết cũ không liên quan (-)
  
  -> Dùng - loại trừ bài viết cũ: npm is not recognized -mac -linux -xp


## Phần 2 – Thẩm định StackOverflow
### **1.** So sánh Câu trả lời A và B ở mục 3c theo **3 tiêu chí thẩm định uy tín**:

| Tiêu chí | Câu trở lời A | Câu trả lời B |
| :--- | :--- | :--- |
| Vote & Tích xanh | +186 Upvotes, Có Tích xanh | +2 Upvotes, Không tích xanh |
| Thời gian bài đăng | 2 năm trước (Cập nhật, phù hợp hiện tại) | 9 năm trước (Quá cũ) |
| Tags khớp hệ điều hành/phần mềm | node.js, windows, npm (khớp hoàn toàn) | node.js, windows-xp (Sai Hệ điều hành Windows 11)

### **2.** Kết luận bạn áp dụng câu trả lời nào và giải thích vì sao **Câu trả lời B** là một **"bẫy" nguy hiểm** nếu áp dụng nhầm.

- Chọn áp dụng câu trả lời A.

- Vì sao B lầ bẫy: Vì B khuyên can thiệp vào "driver mạng của Windows XP". Đây là thao tác hoàn toàn không liên quan đến lỗi đường dẫn của Node.js. Nếu làm theo, bạn có thể làm hỏng kết nối mạng của máy tính và phá vỡ tính ổn định của hệ điều hành.

### **3.** Theo **Quy trình 30 Giây Đọc lướt**, liệt kê đúng thứ tự các bước khi mở 1 trang StackOverflow mới (thay vì đọc dịch toàn bộ phần mô tả câu hỏi).

- **Nhìn tags và tiêu đề:** Xem có đúng ngôn ngữ, lỗi mình đang gặp không.

- **Kéo xuống câu trả lời:** Tìm câu có Tích xanh hoặc lượng Upvote cao nhất.

- **Đọc lướt dòng code, giải pháp:** Tập trung vào các code hoặc các bước in đậm để thử áp dụng, bỏ qua phần giải thích dài dòng của người hỏi.

## Phần 3 - Hỏi AI đúng cách và nhận diện rủi ro

### **1.** Lỗi vẫn còn sau khi làm theo Câu trả lời A (mục 3d). Viết 1 Prompt hoàn chỉnh theo **Công thức Prompt 3 Thành phần** (Ngữ cảnh – Lỗi Nguyên văn – Yêu cầu), có nêu rõ bạn **đã thử thêm PATH nhưng vẫn lỗi**.

- **Ngữ cảnh:** Tôi vừa cài Node.js trên Windows. Mở Terminal trong VS Code và gõ lệnh npm -v. Tôi đã thử thêm đường dẫn C:\Program Files\nodejs\ vào biến môi trường PATH rồi khởi động lại Terminal nhưng vẫn không được.

- **Lỗi nguyên văn:** 
'npm' is not recognized as an internal or external command, operable program or batch file.

- **Yêu cầu:** Hãy giải thích ngắn gọn nguyên nhân vì sao thêm PATH rồi vẫn lỗi và đưa ra các bước khắc phục chi tiết tiếp theo.

### **2.** Đọc câu trả lời của AI ở mục 3e. Áp dụng **3 Nguyên tắc An toàn Vàng** để chỉ ra: đây có phải câu trả lời an toàn để làm theo không? Vì sao?

- **Không an toàn.** Tuyệt đối không được làm theo.

- **Vì sao?** Lệnh del /f /s /q C:\Windows\System32\* là lệnh xóa toàn bộ file hệ thống cốt lõi của Windows (System32). Nếu nhấn Enter, máy tính sẽ hỏng hệ điều hành ngay lập tức. Đây là lỗi AI Hallucination (Ảo giác AI) cực kỳ nguy hiểm, vi phạm nghiêm trọng nguyên tắc vàng: "Không copy-paste mù quáng mã lệnh phá hoại/can thiệp sâu vào hệ điều hành".

### **3.** Nếu là bạn, bạn sẽ **phản hồi/hỏi lại AI** như thế nào trước khi quyết định có chạy lệnh đó hay không?

- **Cách phản hồi lại AI:** "Lệnh bạn vừa đưa ra là lệnh xóa file hệ thống Windows, đây là thao tác gây nguyên hiểm đến máy của tôi. Hãy dừng việc đưa ra các lệnh can thiệp hệ điều hành. Hãy tập trung giải quyết lỗi PATH của Node.js một cách an toàn." (Hoặc tốt nhất là mở một phiên Chat mới để AI xóa ngữ cảnh cũ).

## Phần 4 - Viết Bug Report chuẩn để nhờ hỗ trợ

**Sau khi thử cả 3 bước trên vẫn chưa hết lỗi, bạn quyết định nhắn tin nhờ trợ giảng của lớp hỗ trợ.**

### **1.** Viết 1 tin nhắn kiểu **"Tin nhắn Kém"** (mù mờ, thiếu ngữ cảnh) như ví dụ đã học.

"Thầy ơi máy em cài Node xong bị lỗi tiếng Anh dài lắm, em làm theo mạng chỉ sửa PATH rồi mà gõ npm nó vẫn lỗi. Cứu em với!"

### **2.** Viết lại thành 1 tin nhắn chuẩn, đầy đủ **4 mảnh ghép của Bug Reporting Framework**:

| Mảnh ghép | Nội dung trong tin nhắn của bạn |
| :--- | :--- |
| Context | Em vừa cài Node.js trên Windows 11. Em mở Terminal trong VS Code gõ lệnh npm -v. Em đã thử thêm đường dẫn C:\Program Files\nodejs\ vào PATH và mở lại Terminal nhưng vẫn không được. |
| Expected | Gõ lệnh sẽ hiển thị ra phiên bản của npm đang cài đặt. |
| Actual | Terminal báo lỗi đỏ, không nhận diện được lệnh npm. |
| Log & Screenshot | Lỗi nguyên văn: 'npm' is not recognized as an internal or external command...(Đính kèm ảnh chụp màn hình Terminal báo lỗi và ảnh hộp thoại Environment Variables em đã cấu hình). |

### **3.** Nêu đúng **phím tắt chụp màn hình trên Windows** đã học và **1 lưu ý bảo mật** khi đính kèm ảnh chụp.

- **Phím tắt chụp màn hình (Windows):** Windows + Shift + S.

- **Lưu ý bảo mật:** Phải bôi đen/làm mờ (censor) các thông tin nhạy cảm vô tình lọt vào ảnh chụp như: Mật khẩu, API Key, Token, đoạn chat cá nhân hoặc email trước khi gửi cho người khác.