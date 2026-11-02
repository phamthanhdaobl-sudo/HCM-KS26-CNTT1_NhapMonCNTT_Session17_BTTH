# HCM-KS26-CNTT1_NhapMonCNTT_Session17_BTTH
# BÀI TẬP TỔNG HỢP: NGÀY ĐẦU THỰC TẬP DEV TẠI CÔNG TY CÔNG NGHỆ

**Họ và tên:** Phạm Thành Đạo  
**Lớp:** HCM-KS26-CNTT1  
**Môn học:** Nhập môn CNTT – Session 16  
**Chủ đề:** Thiết lập môi trường trình duyệt và Debug website

---

# PHẦN A – THIẾT LẬP PROFILE VÀ BOOKMARK CHUẨN DEV

## Câu 1. Điều gì xảy ra khi sử dụng chung một Profile cho GitHub cá nhân và GitHub công ty?

Khi sử dụng chung một Profile Chrome để đăng nhập đồng thời GitHub cá nhân và GitHub công ty, có thể xảy ra hiện tượng xung đột phiên đăng nhập (Session Conflict).

**Nguyên nhân:**

- Chrome sử dụng Cookies để lưu thông tin xác thực và trạng thái đăng nhập của website.
- Các tab thông thường thuộc cùng một Profile có thể sử dụng chung kho Cookies.
- Khi đăng nhập tài khoản GitHub khác trên cùng tên miền github.com, Cookie xác thực có thể được thay thế bằng phiên đăng nhập mới.
- Điều này có thể khiến tài khoản trước đó bị chuyển đổi hoặc đăng xuất.

**Hậu quả:**

- Nhầm lẫn giữa tài khoản GitHub cá nhân và tài khoản công ty.
- Có nguy cơ gửi nhầm mã nguồn lên repository không đúng.
- Mất thời gian đăng nhập và chuyển đổi tài khoản liên tục.
- Tăng nguy cơ lộ thông tin cá nhân hoặc thông tin dự án.

**Giải pháp:** Sử dụng Dedicated Browser Profile để tạo các môi trường trình duyệt độc lập, mỗi Profile quản lý một tài khoản và phiên đăng nhập riêng.

## Câu 2. Áp dụng mô hình 3 Profile chuẩn Developer

| Profile | Tên đặt | Mục đích sử dụng |
|---|---|---|
| 1 | Personal | Quản lý tài khoản cá nhân như Gmail, Facebook, YouTube và GitHub cá nhân. |
| 2 | Company_Work | Phục vụ công việc tại công ty, đăng nhập GitHub công ty, hệ thống quản lý dự án và tài liệu nội bộ. |
| 3 | Sandbox_Test | Kiểm thử website, thử nghiệm API, kiểm tra Cookie, Local Storage và các chức năng trước khi báo cáo lỗi. |

### Chi tiết từng Profile

**1. Personal Profile**

- Màu nhận diện: Tím.
- Tài khoản: Gmail cá nhân, GitHub cá nhân, mạng xã hội.
- Bookmarks: Website học tập, giải trí và tài liệu cá nhân.
- Extensions: Tiện ích phục vụ nhu cầu cá nhân.

**2. Company_Work Profile**

- Màu nhận diện: Xanh dương.
- Tài khoản: GitHub công ty, email công việc, hệ thống quản lý dự án.
- Bookmarks: GitHub, tài liệu kỹ thuật, hệ thống nội bộ.
- Extensions: DevTools hỗ trợ lập trình, quản lý công việc và bảo mật.

**3. Sandbox_Test Profile**

- Màu nhận diện: Cam.
- Tài khoản: Tài khoản thử nghiệm được cấp.
- Bookmarks: Website kiểm thử, API, tài liệu debug.
- Extensions: JSON Formatter, công cụ hỗ trợ kiểm tra website.

**Lợi ích:** Ba Profile có Cookies, History, Bookmarks và Extensions độc lập, giúp hạn chế xung đột phiên đăng nhập và tránh nhầm lẫn giữa môi trường cá nhân, công việc và kiểm thử.

## Câu 3. Thiết kế cấu trúc Bookmark gồm 3 thư mục

Đề xuất cấu trúc:

```text
BOOKMARK BAR
│
├── 📁 01_Development
│   ├── GitHub
│   └── MDN Web Docs
│
├── 📁 02_Work_Management
│   ├── Jira
│   └── Google Drive
│
└── 📁 03_Dev_Tools
    ├── JSON Formatter
    └── Chrome DevTools Documentation
```

**Giải thích cách phân loại:**

- 01_Development: Lưu các nền tảng quản lý mã nguồn và tài liệu lập trình.
- 02_Work_Management: Lưu các công cụ quản lý công việc và cộng tác nhóm.
- 03_Dev_Tools: Lưu các công cụ hỗ trợ kiểm thử và debug.

Các liên kết chính thức:

- GitHub: https://github.com/
- MDN Web Docs: https://developer.mozilla.org/
- Jira: https://www.atlassian.com/software/jira
- Google Drive: https://drive.google.com/
- Chrome DevTools: https://developer.chrome.com/docs/devtools/
- JSON Formatter: https://jsonformatter.org/

## Câu 4. Đồng nghiệp mượn máy 5 phút nên sử dụng chế độ nào?

**Lựa chọn: Guest Profile (Chế độ khách).**

**Lý do:**

- Tạo môi trường duyệt web tạm thời cho người khác.
- Không sử dụng dữ liệu của Profile cá nhân đang có.
- Không hiển thị Bookmarks và lịch sử của Profile chính.
- Khi đóng toàn bộ cửa sổ Guest, dữ liệu duyệt web của phiên khách sẽ bị xóa.

**Quy trình:**

1. Nhấn biểu tượng Profile trên Chrome.
2. Chọn Guest.
3. Cho đồng nghiệp sử dụng cửa sổ Guest.
4. Sau khi hoàn thành, đóng toàn bộ cửa sổ Guest.

**Không nên sử dụng Profile cá nhân hoặc để đồng nghiệp truy cập trực tiếp vào tài khoản GitHub công ty.**

---

# PHẦN B – CHỌN ĐÚNG EXTENSION HỖ TRỢ

## Câu 1. Chọn nhóm Extension phù hợp để đọc API JSON

**Lựa chọn: Dev Suite (Developer Suite).**

Tên tiện ích đề xuất: **JSON Formatter**.

**Mục đích:**

Khi mở một đường link API trả về dữ liệu JSON thô, nội dung thường được hiển thị thành một chuỗi văn bản dài, khó quan sát.

JSON Formatter giúp:

- Định dạng JSON thành cấu trúc dễ đọc.
- Hiển thị dữ liệu theo dạng phân cấp.
- Thụt lề và xuống dòng tự động.
- Hỗ trợ nhận biết các trường dữ liệu.
- Giúp Developer kiểm tra nhanh nội dung API Response.

**Ví dụ JSON thô:**

```json
{"id":1,"name":"Nguyen Van A","status":"active","role":"developer"}
```

**Sau khi định dạng:**

```json
{
  "id": 1,
  "name": "Nguyen Van A",
  "status": "active",
  "role": "developer"
}
```

### Vì sao không chọn hai nhóm còn lại?

**Productivity Suite:**

- Tập trung nâng cao năng suất làm việc.
- Hỗ trợ quản lý công việc, ghi chú và thời gian.
- Không phải nhóm chuyên dụng để định dạng và phân tích JSON.

**Security Suite:**

- Tập trung bảo vệ quyền riêng tư và an toàn trình duyệt.
- Hỗ trợ chặn quảng cáo độc hại, theo dõi và cảnh báo bảo mật.
- Không phải chức năng chính để trình bày dữ liệu JSON.

**Kết luận:** Dev Suite phù hợp nhất vì JSON Formatter phục vụ trực tiếp quá trình đọc, phân tích và kiểm thử dữ liệu API.

## Câu 2. Cấu hình quyền Site Access

**Lựa chọn: On click.**

**Giải thích:**

On click cho phép Extension chỉ truy cập nội dung website khi người dùng chủ động nhấn vào biểu tượng tiện ích.

Lợi ích:

- Hạn chế quyền truy cập không cần thiết.
- Giảm nguy cơ tiện ích đọc dữ liệu trên những website không liên quan.
- Phù hợp với nguyên tắc Least Privilege (Đặc quyền tối thiểu).
- Tăng khả năng kiểm soát quyền của Extension.

**Không chọn On all sites** vì quyền này cho phép Extension truy cập rộng hơn trên các website, làm tăng phạm vi dữ liệu có thể tiếp cận.

**Kết luận:** Sử dụng On click để chỉ cấp quyền khi thực sự cần định dạng dữ liệu JSON.

---

# PHẦN C – PHÂN TÍCH LUỒNG HTTP REQUEST

## Câu 1. Liệt kê 4 giai đoạn xử lý HTTP Request Flow

Khi nhập `test.internal-tool.com` vào thanh địa chỉ và nhấn Enter, trình duyệt thực hiện các giai đoạn chính:

### Giai đoạn 1: DNS Resolution (Phân giải tên miền)

- Trình duyệt kiểm tra thông tin DNS đã được lưu trong Cache.
- Nếu chưa có kết quả phù hợp, hệ thống thực hiện truy vấn DNS.
- DNS chuyển tên miền thành địa chỉ IP của máy chủ.

Ví dụ:

```text
test.internal-tool.com
          |
          v
      DNS Lookup
          |
          v
      IP Address
```

### Giai đoạn 2: Establish Connection (Thiết lập kết nối)

- Trình duyệt thiết lập kết nối TCP với máy chủ.
- Nếu sử dụng HTTPS, trình duyệt thực hiện TLS Handshake để thiết lập kết nối mã hóa.
- Sau khi kết nối thành công, trình duyệt có thể gửi yêu cầu HTTP.

### Giai đoạn 3: HTTP Request / Response

- Trình duyệt gửi HTTP Request đến máy chủ.
- Máy chủ tiếp nhận và xử lý yêu cầu.
- Máy chủ gửi HTTP Response về trình duyệt.
- Response bao gồm Status Code, Headers và Body.

Ví dụ:

```http
GET /home HTTP/1.1
Host: test.internal-tool.com
```

Máy chủ có thể trả về:

```http
HTTP/1.1 200 OK
Content-Type: text/html
```

### Giai đoạn 4: Browser Rendering (Phân tích và hiển thị)

- Trình duyệt phân tích HTML để xây dựng DOM.
- Phân tích CSS để xây dựng CSSOM.
- Kết hợp các thành phần để tính toán bố cục và hiển thị giao diện.
- Thực thi JavaScript và tải thêm tài nguyên như hình ảnh, CSS, API.

**Kết luận:** Bốn giai đoạn chính là DNS Resolution → Establish Connection → HTTP Request/Response → Browser Rendering.

## Câu 2. So sánh HTTP 404 và HTTP 500

| Tiêu chí | 404 Not Found | 500 Internal Server Error |
|---|---|---|
| Ý nghĩa | Không tìm thấy tài nguyên được yêu cầu. | Máy chủ gặp lỗi nội bộ khi xử lý yêu cầu. |
| Nhóm lỗi | 4xx – Client Error | 5xx – Server Error |
| Lỗi thường gặp | Sai URL, sai đường dẫn API, tài nguyên không tồn tại. | Lỗi code Backend, Database, cấu hình hoặc xử lý dữ liệu. |
| Hướng debug | Kiểm tra URL, endpoint, HTTP Method và tài nguyên. | Kiểm tra log Backend, Database và quá trình xử lý phía Server. |

### A. HTTP 404 Not Found

Ví dụ:

```http
GET /api/users/999
```

Máy chủ trả về:

```http
404 Not Found
```

Giải thích:

Máy chủ không tìm thấy tài nguyên tương ứng với đường dẫn yêu cầu.

Hướng debug:

1. Kiểm tra URL có chính xác không.
2. Kiểm tra endpoint API.
3. Kiểm tra HTTP Method như GET, POST, PUT hoặc DELETE.
4. Xác nhận tài nguyên có tồn tại hay không.

### B. HTTP 500 Internal Server Error

Ví dụ:

```http
GET /api/users
```

Máy chủ trả về:

```http
500 Internal Server Error
```

Giải thích:

Máy chủ gặp lỗi không mong muốn trong quá trình xử lý yêu cầu.

Hướng debug:

1. Kiểm tra nội dung Response.
2. Kiểm tra lỗi trong Console nếu có.
3. Báo Backend Developer kiểm tra Server Logs.
4. Kiểm tra Database, cấu hình và logic xử lý API.

**Kết luận:**

- 404: Ưu tiên kiểm tra đường dẫn và tài nguyên được yêu cầu.
- 500: Ưu tiên kiểm tra lỗi xử lý phía máy chủ.

Lưu ý: Không phải mọi lỗi 404 đều do người dùng nhập sai URL; tài nguyên cũng có thể đã bị xóa hoặc máy chủ cấu hình sai định tuyến.

## Câu 3. Tab nào dùng để xem HTTP Status Code?

**Lựa chọn: Network.**

Lý do:

Network ghi nhận các yêu cầu và phản hồi HTTP được trình duyệt thực hiện trong quá trình tải trang.

Trong Network có thể xem:

- Request URL.
- Request Method.
- Status Code.
- Response Headers.
- Request Headers.
- Response Body.
- Thời gian tải tài nguyên.

### Vì sao không chọn các Tab còn lại?

**Elements:**

- Kiểm tra cấu trúc HTML.
- Kiểm tra và chỉnh sửa CSS trực tiếp.
- Không phải nơi chuyên dụng để xem mã trạng thái HTTP của từng request.

**Console:**

- Hiển thị lỗi JavaScript.
- Hiển thị cảnh báo và thông báo.
- Có thể xuất hiện thông báo lỗi mạng nhưng không phải nơi quản lý đầy đủ HTTP Request/Response.

**Application:**

- Quản lý Cookies.
- Kiểm tra Local Storage và Session Storage.
- Xem Cache Storage và Service Workers.
- Không phải nơi chuyên dụng để theo dõi Status Code.

**Kết luận:** Network là Tab chính xác để kiểm tra HTTP Status Code.

---

# PHẦN D – CHẨN ĐOÁN CACHE VÀ COOKIES

## Câu 1. Dev sửa CSS nhưng F5 vẫn thấy giao diện cũ

### Nguyên nhân

Nguyên nhân có thể là Browser Cache.

Trình duyệt lưu các tài nguyên tĩnh như:

- CSS.
- JavaScript.
- Hình ảnh.
- Font chữ.

Khi người dùng nhấn F5, trình duyệt có thể sử dụng tài nguyên đã lưu trong Cache thay vì tải lại hoàn toàn phiên bản mới từ máy chủ.

Do đó, mặc dù Developer đã sửa CSS, trình duyệt vẫn hiển thị giao diện cũ.

### Cách khắc phục

**Cách 1: Hard Reload**

Trên Windows:

```text
Ctrl + Shift + R
```

Trên macOS:

```text
Command + Shift + R
```

Thao tác này yêu cầu trình duyệt tải lại trang và bỏ qua nhiều tài nguyên Cache thông thường.

**Cách 2: Empty Cache and Hard Reload**

1. Mở Chrome DevTools bằng F12.
2. Nhấn giữ hoặc nhấp chuột phải vào nút Reload của trình duyệt.
3. Chọn Empty Cache and Hard Reload.

Thao tác này xóa Cache của trình duyệt và tải lại trang.

**Cách 3: Disable Cache**

1. Mở DevTools.
2. Chọn tab Network.
3. Tích vào ô Disable cache.
4. Tải lại trang để kiểm tra.

Lưu ý: Disable cache chỉ có hiệu lực khi DevTools đang mở.

**Kết luận:** Ưu tiên Hard Reload hoặc Empty Cache and Hard Reload để kiểm tra CSS mới.

## Câu 2. Cookie session_id không có dấu tích HttpOnly

### Nguy cơ bảo mật

Thuộc tính HttpOnly giúp ngăn JavaScript phía trình duyệt truy cập trực tiếp vào Cookie thông qua các API như `document.cookie`.

Nếu Cookie `session_id` không có thuộc tính HttpOnly, JavaScript trên trang có thể đọc được giá trị Cookie này.

Nếu website tồn tại lỗ hổng Cross-Site Scripting (XSS), kẻ tấn công có thể chèn JavaScript độc hại để lấy cắp Cookie phiên đăng nhập.

### Tên loại tấn công

**Cross-Site Scripting (XSS).**

### Hậu quả

- Đánh cắp Session Cookie.
- Chiếm quyền phiên đăng nhập (Session Hijacking).
- Truy cập trái phép vào tài khoản của người dùng nếu Cookie bị đánh cắp còn hiệu lực.

### Biện pháp khắc phục

- Thiết lập thuộc tính HttpOnly cho Cookie phiên đăng nhập.
- Sử dụng Secure để chỉ gửi Cookie qua HTTPS.
- Cấu hình SameSite phù hợp để hạn chế một số hình thức tấn công liên quan đến yêu cầu giả mạo.
- Kiểm tra và xử lý dữ liệu đầu vào để ngăn XSS.

**Kết luận:** Cookie `session_id` nên được thiết lập HttpOnly để giảm nguy cơ JavaScript độc hại đánh cắp thông tin phiên đăng nhập.

## Câu 3. Chỉ muốn đăng xuất nhưng vẫn giữ Cache ảnh và CSS

**Thao tác: Xóa Cookie của website, không xóa toàn bộ Browsing Data.**

Cách thực hiện trong Chrome DevTools:

1. Mở DevTools.
2. Chọn tab Application.
3. Tìm mục Storage.
4. Mở Cookies.
5. Chọn domain của website.
6. Tìm Cookie `session_id`.
7. Xóa Cookie này bằng biểu tượng xóa hoặc Delete.
8. Tải lại trang và kiểm tra trạng thái đăng nhập.

**Kết quả:**

- Phiên đăng nhập được xóa nếu `session_id` là Cookie xác thực cần thiết.
- Cache ảnh và CSS vẫn được giữ lại.
- Không cần xóa toàn bộ lịch sử hoặc dữ liệu trình duyệt.

**Lưu ý:** Một số website sử dụng nhiều Cookie hoặc cơ chế xác thực khác như token, nên xóa riêng `session_id` chưa chắc đã đăng xuất hoàn toàn. Cách chính xác nhất vẫn là sử dụng chức năng Logout của website.

---

# PHẦN E – DEBUG BẰNG INSPECT ELEMENT VÀ NETWORK TAB

## Câu 1. Nút Đăng nhập bị lệch màu so với thiết kế

**Công cụ sử dụng: Inspect Element trong tab Elements.**

### Các bước thực hiện

**Bước 1:** Mở website `test.internal-tool.com`.

**Bước 2:** Nhấn F12 để mở Chrome DevTools.

**Bước 3:** Chọn tab Elements.

**Bước 4:** Nhấn biểu tượng Select Element (hình mũi tên trong khung) hoặc sử dụng tổ hợp:

```text
Ctrl + Shift + C
```

Trên macOS:

```text
Command + Shift + C
```

**Bước 5:** Di chuyển chuột đến nút Đăng nhập và nhấp chọn phần tử.

**Bước 6:** Tìm thuộc tính CSS trong khu vực Styles.

Ví dụ:

```css
.login-button {
    background-color: #007BFF;
    color: #FFFFFF;
}
```

**Bước 7:** Nhấp vào giá trị `background-color` và thử thay đổi màu theo thiết kế.

Ví dụ:

```css
background-color: #0056D2;
```

**Bước 8:** Quan sát giao diện sau khi thay đổi.

### Kết quả

Nếu nút hiển thị đúng màu thiết kế sau khi thay đổi CSS trực tiếp trong DevTools, có thể báo lại cho Developer rằng nguyên nhân liên quan đến thuộc tính CSS của phần tử.

**Lưu ý:** Thay đổi trong Elements chỉ có tác dụng tạm thời trên trình duyệt. Không chỉnh sửa file CSS gốc của dự án.

## Câu 2. Quy trình 4 Bước Debugging khi API Request hiển thị màu đỏ

Khi một request API xuất hiện dòng màu đỏ trong Network, cần thực hiện quy trình kiểm tra sau:

### Bước 1: Reproduce the Error (Tái hiện lỗi)

- Mở website `test.internal-tool.com`.
- Mở DevTools và chọn Network.
- Thực hiện lại thao tác gây lỗi.
- Quan sát request API xuất hiện màu đỏ.

Mục tiêu: Xác định lỗi có thể tái hiện được và biết thao tác nào gây ra lỗi.

### Bước 2: Inspect the Request (Kiểm tra yêu cầu)

Nhấp vào request bị lỗi và kiểm tra:

- Request URL.
- Request Method.
- Request Headers.
- Query Parameters.
- Request Payload nếu có.

Mục tiêu: Xác định trình duyệt đang gửi yêu cầu gì và gửi đến địa chỉ nào.

### Bước 3: Analyze the Response (Phân tích phản hồi)

Kiểm tra:

- HTTP Status Code.
- Response Headers.
- Response Body.
- Thông báo lỗi trong Console.
- Thời gian phản hồi và thông tin liên quan.

Ví dụ:

- 400 Bad Request: Yêu cầu không hợp lệ.
- 401 Unauthorized: Chưa xác thực hoặc không hợp lệ.
- 403 Forbidden: Không có quyền truy cập.
- 404 Not Found: Không tìm thấy tài nguyên.
- 500 Internal Server Error: Máy chủ gặp lỗi nội bộ.

Mục tiêu: Xác định lỗi thuộc phía Client, Server, xác thực hay kết nối mạng.

### Bước 4: Report and Verify (Báo cáo và kiểm chứng)

- Ghi lại URL và HTTP Method.
- Ghi lại Status Code.
- Chụp ảnh request lỗi trong Network.
- Ghi lại Response Body và thông báo lỗi.
- Báo cáo cho Developer hoặc Backend Developer phụ trách.
- Sau khi được sửa lỗi, thực hiện lại thao tác để xác nhận kết quả.

**Kết luận:** Không tự ý sửa file dự án. Chỉ thực hiện kiểm tra và xác minh lỗi trên trình duyệt theo đúng phạm vi được giao.

## Câu 3. Chỉ xem API và đảm bảo dữ liệu mới nhất trên Network

Cần thực hiện đúng hai thao tác:

### Thao tác 1: Chọn bộ lọc Fetch/XHR

1. Mở DevTools.
2. Chọn tab Network.
3. Nhấn vào bộ lọc Fetch/XHR.

**Tác dụng:**

Chỉ hiển thị các request được thực hiện thông qua Fetch API và XMLHttpRequest, thường được sử dụng để gọi API.

Giúp loại bỏ phần lớn các request tải hình ảnh, CSS, font và các tài nguyên tĩnh khác khỏi danh sách đang quan sát.

### Thao tác 2: Bật Disable Cache

1. Vẫn ở tab Network.
2. Tìm tùy chọn Disable cache.
3. Tích chọn vào ô này.
4. Đảm bảo DevTools đang mở.
5. Tải lại trang hoặc thực hiện lại thao tác gọi API.

**Tác dụng:**

Hạn chế việc sử dụng HTTP Cache của trình duyệt, giúp kiểm tra dữ liệu mới nhất từ máy chủ.

**Kết luận:**

Hai thao tác cần thực hiện là:

1. Fetch/XHR – Lọc các request API.
2. Disable Cache – Hạn chế sử dụng dữ liệu từ HTTP Cache của trình duyệt.

Lưu ý: Disable Cache không bảo đảm API luôn trả dữ liệu mới nhất nếu phía máy chủ, CDN hoặc Service Worker vẫn có cơ chế Cache riêng.

---

# TỔNG KẾT BÀI TẬP

Qua bài tập tổng hợp, em đã vận dụng kiến thức Session 16 vào tình huống thực tế của một Developer mới bắt đầu thực tập tại công ty công nghệ.

Các kiến thức quan trọng đã được áp dụng:

| Nội dung | Kiến thức vận dụng |
|---|---|
| Browser Profile | Phân tách Personal, Company_Work và Sandbox_Test |
| Bookmark | Phân loại tài liệu thành 3 thư mục |
| Extensions | Chọn Dev Suite và JSON Formatter |
| Site Access | Áp dụng On click và Least Privilege |
| HTTP Request Flow | DNS, Connection, Request/Response, Rendering |
| HTTP Status Code | Phân biệt 404 và 500 |
| DevTools | Sử dụng Elements, Console, Network, Application |
| Cache | Hard Reload, Disable Cache |
| Cookies | HttpOnly, XSS, Session Hijacking |
| Inspect Element | Kiểm tra và thay đổi CSS tạm thời |
| Network Debugging | Fetch/XHR, Status Code, Request và Response |

## KẾT LUẬN

Việc thiết lập môi trường trình duyệt khoa học giúp Developer quản lý nhiều tài khoản, hạn chế xung đột phiên đăng nhập và tăng hiệu suất làm việc.

Bên cạnh đó, việc hiểu HTTP Request Flow, Cache, Cookies và sử dụng thành thạo Chrome DevTools giúp Developer xác định nguyên nhân của các lỗi giao diện và lỗi API nhanh chóng hơn.

Đối với một thực tập sinh Developer, đây là những kỹ năng nền tảng quan trọng để làm việc hiệu quả, bảo đảm an toàn dữ liệu và phối hợp tốt với các thành viên trong nhóm phát triển phần mềm.

**Đề xuất:** Duy trì mô hình 3 Profile, quản lý Extension theo nguyên tắc đặc quyền tối thiểu và sử dụng DevTools làm công cụ kiểm tra chính trước khi báo cáo lỗi cho Mentor.

---

**TÀI LIỆU THAM KHẢO**

1. Chrome for Developers – Chrome DevTools Documentation: https://developer.chrome.com/docs/devtools/
2. MDN Web Docs – HTTP Overview: https://developer.mozilla.org/en-US/docs/Web/HTTP
3. MDN Web Docs – HTTP Status Codes: https://developer.mozilla.org/en-US/docs/Web/HTTP/Reference/Status
4. MDN Web Docs – Cookies: https://developer.mozilla.org/en-US/docs/Web/HTTP/Cookies
5. Google Chrome Help – Manage Chrome Profiles: https://support.google.com/chrome/answer/2364824
6. Chrome Extensions Documentation – Site Access and Permissions: https://developer.chrome.com/docs/extensions/develop/concepts/declare-permissions
