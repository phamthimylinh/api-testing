## 1. Katalon Studio là gì?

Katalon Studio là một công cụ **tự động hóa kiểm thử (automation testing)** mạnh mẽ, hỗ trợ kiểm thử trên nhiều nền tảng như **Web**, **API**, **Mobile**, và **Desktop**. Điểm đặc biệt của Katalon là nó được thiết kế để phù hợp với cả những người mới bắt đầu (như tester manual) và các chuyên gia automation testing.

- **Được phát triển bởi người Việt Nam**: Katalon Studio là sản phẩm của đội ngũ kỹ sư Việt Nam và quốc tế, rất tự hào đúng không nào?
- **Miễn phí và dễ sử dụng**: Phiên bản miễn phí của Katalon đã đủ mạnh để bạn thực hiện các kịch bản kiểm thử tự động mà không cần viết quá nhiều code.
- **Hỗ trợ codeless**: Bạn có thể tạo test case bằng cách ghi lại thao tác (Record) hoặc sử dụng giao diện kéo-thả, không cần biết lập trình sâu.

Nếu bạn đã quen với việc sử dụng **Postman** để kiểm thử API, Katalon Studio sẽ là bước tiến tiếp theo giúp bạn mở rộng khả năng kiểm thử, không chỉ với API mà còn với giao diện người dùng (UI) và ứng dụng di động.

## 2. Tại sao Tester Manual nên dùng Katalon Studio?

Tester manual thường quen với việc kiểm thử thủ công, nhập dữ liệu, kiểm tra kết quả bằng tay. Tuy nhiên, khi dự án lớn hơn, việc kiểm thử thủ công tốn rất nhiều thời gian và dễ xảy ra lỗi. Katalon Studio giúp bạn:

- **Tự động hóa quy trình kiểm thử**: Thay vì kiểm tra từng trường hợp thủ công, bạn có thể để Katalon tự động chạy các kịch bản kiểm thử.
- **Hỗ trợ kiểm thử API**: Nếu bạn đã dùng Postman để gửi request và kiểm tra response, Katalon cung cấp giao diện tương tự nhưng mạnh hơn, tích hợp với các kịch bản kiểm thử UI.
- **Tiết kiệm thời gian**: Katalon cho phép chạy nhiều test case cùng lúc và xuất báo cáo chi tiết.
- **Dễ học**: Với tester manual, Katalon có chế độ **Manual Mode** giúp bạn tạo test case mà không cần viết code.

## 3. So sánh Katalon Studio và Postman

Bạn đã quen với Postman, vậy Katalon Studio khác gì? Dưới đây là bảng so sánh để bạn hình dung:

| **Tiêu chí** | **Postman** | **Katalon Studio** |
| --- | --- | --- |
| **Mục đích chính** | Kiểm thử API | Kiểm thử tự động Web, API, Mobile, Desktop |
| **Giao diện** | Dễ dùng, tập trung vào API | Giao diện IDE, hỗ trợ cả API và UI |
| **Khả năng tự động hóa** | Hỗ trợ automation cơ bản (qua Collection Runner, Newman) | Tự động hóa toàn diện, tích hợp CI/CD |
| **Codeless** | Không, cần viết script JavaScript | Có, hỗ trợ Record và Manual Mode |
| **Hỗ trợ tester manual** | Phù hợp khi học API testing | Thân thiện với người mới, tích hợp cả UI và API |
| **Báo cáo** | Cơ bản, cần thêm công cụ như Newman | Báo cáo chi tiết, tích hợp sẵn |

**Kết luận**: Nếu bạn chỉ cần kiểm thử API, Postman là lựa chọn gọn nhẹ. Nhưng nếu bạn muốn mở rộng sang kiểm thử tự động toàn diện (UI + API), Katalon Studio là công cụ lý tưởng.

## 4. Các tính năng nổi bật của Katalon Studio cho Tester Manual

Dưới đây là những tính năng chính của Katalon Studio mà bạn, với vai trò tester manual, sẽ thấy hữu ích:

### 4.1. Kiểm thử API dễ dàng

- Katalon Studio hỗ trợ gửi các HTTP request (GET, POST, PUT, DELETE) giống Postman.
- Bạn có thể nhập tài liệu API (Swagger/OpenAPI) để tự động tạo các request, thay vì nhập thủ công như Postman.
- Hỗ trợ kiểm tra response (status code, JSON/XML) bằng giao diện trực quan hoặc script đơn giản.
- Ví dụ: Bạn có thể kiểm tra xem API trả về mã trạng thái 200 OK và dữ liệu JSON đúng như kỳ vọng không.

### 4.2. Chế độ Record & Playback

- **Record**: Katalon cho phép bạn ghi lại các thao tác trên trình duyệt (như click, nhập liệu) và tự động tạo test case.
- **Playback**: Chạy lại các thao tác đã ghi để kiểm tra xem ứng dụng có hoạt động đúng không.
- Đây là tính năng cực kỳ hữu ích cho tester manual, vì bạn không cần viết code.

### 4.3. Manual Mode

- Manual Mode cho phép bạn tạo test case bằng cách chọn các hành động (click, verify text, send request...) từ danh sách có sẵn.
- Ví dụ: Bạn có thể tạo một test case kiểm tra đăng nhập bằng cách:
    1. Gửi API POST để lấy token.
    2. Nhập token vào form đăng nhập trên UI.
    3. Kiểm tra xem trang chủ có hiển thị đúng không.

### 4.4. Hỗ trợ Data-Driven Testing

- Katalon cho phép bạn sử dụng dữ liệu từ file Excel/CSV để chạy cùng một test case với nhiều bộ dữ liệu khác nhau.
- Ví dụ: Kiểm tra API đăng nhập với 10 cặp email/password khác nhau chỉ trong một kịch bản.

### 4.5. Báo cáo chi tiết

- Sau khi chạy test, Katalon tạo báo cáo với thông tin như: số test case pass/fail, thời gian chạy, lỗi cụ thể.
- Báo cáo này dễ đọc và có thể gửi cho đội phát triển.

## 5. Hướng dẫn bắt đầu với Katalon Studio

### 5.1. Cài đặt Katalon Studio

1. **Tải Katalon Studio**:
    - Truy cập katalon.com và đăng ký tài khoản miễn phí.
    - Tải phiên bản **Standalone Edition** (dành cho người mới) về máy (hỗ trợ Windows, macOS, Linux).
2. **Cài đặt**:
    - Giải nén file tải về và chạy ứng dụng.
    - Đăng nhập bằng tài khoản Katalon đã đăng ký.
    - Nếu thấy Windows Security Alert, nhấn **Allow Access**.

### 5.2. Tạo dự án mới

1. Mở Katalon Studio, chọn **File > New > Project**.
2. Đặt tên dự án (ví dụ: "MyFirstAPIProject") và chọn loại dự án là **API/Web Service**.
3. Nhấn **OK** để tạo dự án.

### 5.3. Tạo test case API đơn giản

Giả sử bạn muốn kiểm tra một API GET từ petstore.swagger.io, tương tự cách bạn làm trong Postman:

1. **Thêm request API**:
    - Trong Katalon, vào **Object Repository**, nhấp **New > Web Service Request**.
    - Nhập URL: https://petstore.swagger.io/v2/pet/findByStatus?status=available.
    - Chọn phương thức **GET**.
    - Nhấn **Test Request** để kiểm tra response (tương tự nút Send trong Postman).
2. **Tạo test case**:
    - Vào **Test Cases**, nhấp **New > Test Case**.
    - Trong Manual Mode, thêm bước:
        - **Call Request**: Chọn request vừa tạo.
        - **Verify Status Code**: Kiểm tra mã trạng thái là 200.
        - **Verify JSON Response**: Kiểm tra một giá trị trong JSON (ví dụ: name của pet).
3. **Chạy test case**:
    - Nhấn nút **Run** và xem kết quả trong tab **Log Viewer**.
    - Katalon sẽ báo pass/fail và chi tiết lỗi (nếu có).

### 5.4. Kết hợp API và UI testing

Ví dụ: Bạn muốn kiểm tra quy trình đăng nhập:

1. Gửi API POST để lấy token.
2. Sử dụng token trong test case UI để đăng nhập vào website.
3. Katalon cho phép kết hợp cả hai loại kiểm thử trong cùng một dự án.

## 6. Hướng dẫn sử dụng cơ bản Katalon Studio cho API Testing (tương tự Postman)

Dưới đây là hướng dẫn chi tiết cách sử dụng Katalon Studio để kiểm thử API, với các tính năng tương tự như Postman như **Collection**, **biến**, và **script**. Những tính năng này sẽ giúp bạn dễ dàng chuyển từ Postman sang Katalon.

### 6.1. Tạo và quản lý Collection (tương tự Collection trong Postman)

Trong Postman, bạn sử dụng **Collection** để nhóm các request liên quan (ví dụ: tất cả request cho API đăng nhập, API lấy danh sách người dùng). Trong Katalon, bạn có thể tổ chức các request tương tự trong **Object Repository**.

### Cách tạo Collection trong Katalon:

1. Mở dự án, vào **Object Repository**.
2. Tạo một thư mục mới (nhấp chuột phải > **New > Folder**, đặt tên ví dụ: PetStoreAPI).
3. Trong thư mục này, thêm các **Web Service Request**:
    - Nhấp **New > Web Service Request**.
    - Nhập thông tin request (URL, phương thức, header, body...).
    - Ví dụ: Tạo hai request:
        - **GET Pets**: https://petstore.swagger.io/v2/pet/findByStatus?status=available.
        - **POST Pet**: https://petstore.swagger.io/v2/pet với body JSON để thêm một pet mới.
4. Nhóm các request này giống như một Collection trong Postman. Bạn có thể chạy từng request riêng lẻ hoặc kết hợp chúng trong một **Test Suite**.

### Chạy Collection:

- Tạo một **Test Suite** (nhấp **File > New > Test Suite**).
- Thêm các test case sử dụng các request trong thư mục PetStoreAPI.
- Nhấn **Run** để chạy toàn bộ Test Suite, tương tự chạy Collection trong Postman.

### 6.2. Sử dụng biến (tương tự Variables trong Postman)

Postman cho phép bạn sử dụng **Variables** (Global, Collection, Environment) để lưu trữ dữ liệu như URL base, token, hoặc tham số. Katalon Studio cũng hỗ trợ **Variables** để tái sử dụng dữ liệu trong các request và test case.

### Cách tạo và sử dụng biến trong Katalon:

1. **Tạo Global Variable**:
    - Vào **Project > Settings > Global Variables**.
    - Thêm biến, ví dụ:
        - base_url = https://petstore.swagger.io/v2.
        - api_token = your_token_here (có thể cập nhật động sau).
2. **Sử dụng biến trong request**:
    - Khi tạo Web Service Request, thay vì nhập URL đầy đủ, bạn dùng: ${base_url}/pet/findByStatus?status=available.
    - Trong body hoặc header, bạn có thể dùng biến: ${api_token}.
3. **Cập nhật biến động**:
    - Ví dụ: Sau khi gửi API POST để lấy token, bạn có thể lưu token vào biến:
        - Trong test case, thêm bước **Script** (chuyển sang tab Script):
            
            ```groovy
            import com.kms.katalon.core.webservice.keyword.WSBuiltInKeywords as WS
            def response = WS.sendRequest(findTestObject('PetStoreAPI/POST_Login'))
            def token = response.getResponseBodyContent().jsonPath().get('token')
            GlobalVariable.api_token = token
            ```
            

### So sánh với Postman:

- Trong Postman, bạn dùng pm.globals.set("token", value) để lưu biến.
- Trong Katalon, bạn dùng GlobalVariable.ten_bien = gia_tri trong script Groovy.

### 6.3. Viết script để xử lý logic (tương tự Pre-request Script và Tests trong Postman)

Postman cho phép bạn viết JavaScript trong **Pre-request Script** (xử lý trước khi gửi request) và **Tests** (kiểm tra response). Katalon Studio sử dụng **Groovy**, một ngôn ngữ đơn giản và dễ học, để viết script trong test case.

### Ví dụ: Kiểm thử API POST trong Katalon

Giả sử bạn muốn gửi API POST để tạo pet mới và kiểm tra response, tương tự cách bạn làm trong Postman.

1. **Tạo request POST**:
    - Trong **Object Repository**, tạo request:
        - URL: ${base_url}/pet.
        - Phương thức: POST.
        - Body JSON:
            
            ```json
            {
              "id": 123,
              "name": "MyPet",
              "status": "available"
            }
            ```
            
2. **Tạo test case**:
    - Trong **Test Cases**, tạo test case mới.
    - Thêm bước **Send Request** (gọi request POST vừa tạo).
    - Thêm bước **Verify Status Code**: Kiểm tra mã trạng thái là 200.
3. **Viết script để kiểm tra response**:
    - Chuyển sang tab **Script** của test case, thêm code Groovy:
        
        ```groovy
        import com.kms.katalon.core.webservice.keyword.WSBuiltInKeywords as WS
        def response = WS.sendRequest(findTestObject('PetStoreAPI/POST_Pet'))
        WS.verifyResponseStatusCode(response, 200)
        def jsonResponse = response.getResponseBodyContent().jsonPath()
        WS.verifyElementPropertyValue(response, 'name', 'MyPet')
        ```
        

### So sánh với Postman:

- Trong Postman, bạn viết:
    
    ```jsx
    pm.test("Check pet name", function () {
        var jsonData = pm.response.json();
        pm.expect(jsonData.name).to.eql("MyPet");
    });
    ```
    
- Trong Katalon, bạn dùng Groovy và các keyword như WS.verifyElementPropertyValue để kiểm tra tương tự.

### 6.4. Tích hợp dữ liệu từ file ngoài (tương tự Data Files trong Postman)

Postman cho phép bạn nhập file CSV/JSON để chạy Collection với nhiều bộ dữ liệu. Katalon hỗ trợ **Data Files** để làm điều tương tự.

### Cách sử dụng Data Files:

1. Tạo file Excel/CSV với dữ liệu, ví dụ:
    
    ```
    id,name,status
    123,MyPet,available
    456,YourPet,sold
    ```
    
2. Trong Katalon, vào **Data Files**, nhấp **New > Data File** và nhập file CSV.
3. Trong Test Suite, chọn **Data Binding**:
    - Gán file CSV vào test case.
    - Sử dụng biến trong request, ví dụ: ${id}, ${name}, ${status}.
4. Chạy Test Suite để kiểm tra API với từng dòng dữ liệu.

### So sánh với Postman:

- Postman: Dùng file CSV/JSON trong Collection Runner.
- Katalon: Dùng Data Files và tích hợp trực tiếp vào Test Suite.

### 6.5. Tạo báo cáo và lưu kết quả

Sau khi chạy Test Suite, Katalon tự động tạo báo cáo chi tiết trong tab **Reports**:

- Hiển thị số lượng test case pass/fail.
- Lưu log chi tiết của từng request/response.
- Xuất báo cáo dưới dạng HTML, PDF, hoặc CSV.

So với Postman, báo cáo của Katalon tích hợp sẵn và dễ đọc hơn, không cần công cụ bổ sung như Newman.

## 7. Lợi ích khi dùng Katalon Studio so với chỉ dùng Postman

- **Tích hợp toàn diện**: Katalon cho phép kiểm thử cả API và UI trong cùng một công cụ, trong khi Postman chỉ tập trung vào API.
- **Dễ dàng mở rộng**: Bạn có thể tích hợp Katalon với Git, Jenkins để tự động hóa CI/CD, điều mà Postman cần thêm công cụ như Newman.
- **Hỗ trợ tester manual**: Các tính năng như Record, Manual Mode giúp bạn làm quen với automation mà không cần học lập trình ngay.
- **Cộng đồng và tài liệu phong phú**: Katalon có cộng đồng hỗ trợ lớn và nhiều tài liệu miễn phí, phù hợp cho người mới.
