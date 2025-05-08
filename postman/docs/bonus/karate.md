## 1. Karate Framework là gì?

Karate Framework là một công cụ **tự động hóa kiểm thử API** mã nguồn mở, được thiết kế để đơn giản hóa việc kiểm thử API, mock, kiểm thử hiệu suất, và thậm chí cả kiểm thử UI trong một framework thống nhất. Karate nổi bật với cú pháp dễ đọc, dựa trên **Gherkin** (tương tự Cucumber), giúp cả những người không giỏi lập trình (như tester manual) cũng có thể sử dụng.

- **Nguyên tắc KISS**: Karate tuân theo triết lý "Keep It Simple, Stupid" – giữ mọi thứ đơn giản nhất có thể.
- **Không cần viết code phức tạp**: Bạn viết test case bằng cú pháp Gherkin trong các file .feature, không cần viết "glue code" như Cucumber.
- **Hỗ trợ đa dạng**: Karate hỗ trợ kiểm thử API (REST, SOAP), GraphQL, kiểm thử hiệu suất (tích hợp Gatling), mock API, và cả kiểm thử UI (dựa trên WebDriver).

Nếu bạn đã quen với **Postman** để kiểm thử API, Karate sẽ là bước tiến tiếp theo giúp bạn tự động hóa kiểm thử API một cách mạnh mẽ hơn, với khả năng tích hợp vào quy trình CI/CD và viết kịch bản kiểm thử dễ dàng.

## 2. Tại sao Tester Manual nên dùng Karate Framework?

Tester manual thường quen với việc kiểm thử thủ công, nhập dữ liệu và kiểm tra kết quả bằng tay. Khi dự án lớn hơn, việc này trở nên tốn thời gian và dễ xảy ra lỗi. Karate Framework giúp bạn:

- **Tự động hóa kiểm thử API**: Thay vì gửi request thủ công trong Postman, Karate tự động chạy các kịch bản kiểm thử và kiểm tra response.
- **Dễ học với tester manual**: Cú pháp Gherkin đơn giản, gần với ngôn ngữ tự nhiên, không yêu cầu kỹ năng lập trình sâu.
- **Hỗ trợ kiểm thử phức tạp**: Karate cho phép kiểm tra JSON/XML phức tạp, tích hợp dữ liệu từ file ngoài, và thực hiện kiểm thử song song.
- **Báo cáo chi tiết**: Karate tự động tạo báo cáo HTML dễ đọc, giúp bạn theo dõi kết quả kiểm thử.

## 3. So sánh Karate Framework và Postman

Bạn đã quen với Postman, vậy Karate Framework khác gì? Dưới đây là bảng so sánh:

| **Tiêu chí** | **Postman** | **Karate Framework** |
| --- | --- | --- |
| **Mục đích chính** | Kiểm thử API thủ công và tự động cơ bản | Tự động hóa kiểm thử API, mock, hiệu suất, UI |
| **Giao diện** | Giao diện đồ họa, dễ dùng | Dựa trên file .feature, cần IDE như IntelliJ |
| **Khả năng tự động hóa** | Hỗ trợ cơ bản qua Collection Runner, Newman | Tự động hóa mạnh mẽ, tích hợp CI/CD |
| **Codeless** | Có giao diện, nhưng automation cần JavaScript | Cú pháp Gherkin, không cần code phức tạp |
| **Hỗ trợ tester manual** | Phù hợp cho API testing thủ công | Thân thiện với người mới, tích hợp đa dạng |
| **Báo cáo** | Cơ bản, cần thêm Newman | Báo cáo HTML chi tiết, tích hợp sẵn |

**Kết luận**: Postman phù hợp cho kiểm thử API thủ công hoặc automation đơn giản. Karate Framework lý tưởng cho tự động hóa kiểm thử API phức tạp, tích hợp vào quy trình phát triển phần mềm, và hỗ trợ cả UI testing.

## 4. Các tính năng nổi bật của Karate Framework cho Tester Manual

Dưới đây là những tính năng chính của Karate mà tester manual sẽ thấy hữu ích:

### 4.1. Kiểm thử API dễ dàng

- Karate hỗ trợ các phương thức HTTP (GET, POST, PUT, DELETE) và kiểm tra response (JSON, XML) với cú pháp đơn giản.
- Tích hợp JsonPath và XPath để kiểm tra dữ liệu phức tạp trong response.
- Ví dụ: Kiểm tra API trả về status code 200 và giá trị cụ thể trong JSON.

### 4.2. Cú pháp Gherkin thân thiện

- Test case được viết trong file .feature bằng ngôn ngữ gần với tự nhiên.
- Ví dụ:
    
    ```gherkin
    Scenario: Kiểm tra API GET danh sách thú cưng
      Given url 'https://petstore.swagger.io/v2/pet/findByStatus?status=available'
      When method get
      Then status 200
      And match response[0].name == 'doggie'
    ```
    

### 4.3. Hỗ trợ Data-Driven Testing

- Karate cho phép sử dụng dữ liệu từ file CSV, JSON, hoặc bảng trong file .feature để chạy test với nhiều bộ dữ liệu.
- Tương tự Postman khi dùng file CSV trong Collection Runner.

### 4.4. Báo cáo và gỡ lỗi

- Karate tạo báo cáo HTML chi tiết, hiển thị pass/fail và log từng bước.
- Công cụ debug tích hợp trong IDE (như IntelliJ) giúp bạn chỉnh sửa và chạy lại test dễ dàng.

### 4.5. Tích hợp CI/CD

- Karate dễ dàng tích hợp với Jenkins, Git, hoặc các công cụ CI/CD khác, giúp tự động hóa kiểm thử trong quy trình phát triển.

## 5. Hướng dẫn bắt đầu với Karate Framework

### 5.1. Cài đặt Karate Framework

1. **Yêu cầu**:
    - Cài Java JDK (phiên bản 8 trở lên).
    - Cài Maven hoặc Gradle để quản lý dự án.
    - Sử dụng IDE như IntelliJ IDEA hoặc VS Code (khuyến nghị IntelliJ).
2. **Tạo dự án Karate**:
    - Tạo một dự án Maven:
        
        ```bash
        mvn archetype:generate -DgroupId=com.mycompany -DartifactId=karate-tests -DarchetypeArtifactId=maven-archetype-quickstart
        ```
        
    - Thêm dependency Karate vào file pom.xml:
        
        ```xml
        <dependency>
            <groupId>com.intuit.karate</groupId>
            <artifactId>karate-junit5</artifactId>
            <version>1.4.0</version>
            <scope>test</scope>
        </dependency>
        ```
        
3. **Cấu trúc dự án**:
    - Tạo thư mục src/test/java và src/test/resources.
    - Đặt các file .feature (test case) trong src/test/resources.

### 5.2. Tạo test case API đơn giản

Giả sử bạn muốn kiểm tra API GET từ petstore.swagger.io, tương tự Postman:

1. **Tạo file** .feature:
    - Trong src/test/resources, tạo file petstore.feature:
        
        ```gherkin
        Feature: Kiểm tra API Petstore
          Scenario: Lấy danh sách thú cưng
            Given url 'https://petstore.swagger.io/v2/pet/findByStatus?status=available'
            When method get
            Then status 200
            And match response[0].name == 'doggie'
        ```
        
2. **Tạo Test Runner**:
    - Trong src/test/java, tạo file PetstoreTest.java:
        
        ```java
        import com.intuit.karate.junit5.Karate;
        class PetstoreTest {
            @Karate.Test
            Karate testPetstore() {
                return Karate.run("petstore").relativeTo(getClass());
            }
        }
        ```
        
3. **Chạy test**:
    - Chạy lệnh Maven: mvn test.
    - Karate sẽ chạy file .feature và tạo báo cáo trong thư mục target/karate-reports.

### 5.3. Kết hợp API và UI testing

Karate cho phép tích hợp kiểm thử API và UI trong cùng một file .feature. Ví dụ:

```gherkin
Feature: Kiểm tra đăng nhập
  Scenario: Gửi API lấy token và đăng nhập UI
    Given url 'https://example.com/api/login'
    And request { "username": "user", "password": "pass" }
    When method post
    Then status 200
    And def token = response.token
    Given driver 'https://example.com/login'
    And input('#token', token)
    When click('#submit')
    Then match driver.url == 'https://example.com/dashboard'
```

## 6. Hướng dẫn sử dụng cơ bản Karate Framework cho API Testing (tương tự Postman)

Dưới đây là hướng dẫn chi tiết cách sử dụng Karate để kiểm thử API, với các tính năng tương tự Postman như **Collection**, **biến**, và **script**.

### 6.1. Tạo và quản lý Collection (tương tự Collection trong Postman)

Trong Postman, bạn nhóm các request vào Collection. Trong Karate, bạn nhóm các **Scenario** trong file .feature hoặc nhiều file .feature trong một thư mục.

### Cách tạo Collection:

1. Tạo file .feature trong src/test/resources, ví dụ petstore.feature:
    
    ```gherkin
    Feature: Petstore API Collection
      Scenario: Lấy danh sách thú cưng
        Given url 'https://petstore.swagger.io/v2/pet/findByStatus?status=available'
        When method get
        Then status 200
    
      Scenario: Thêm thú cưng mới
        Given url 'https://petstore.swagger.io/v2/pet'
        And request { "id": 123, "name": "MyPet", "status": "available" Hawkins: Kiểm tra API trả về mã trạng thái (status code) là **201**.
    - **match responseHeaders['Content-Type'][0] contains 'application/json'**: Kiểm tra header `Content-Type` có chứa `application/json`.
    - **match responseType == 'JSON'**: Kiểm tra response là định dạng JSON.
    - **match response == { id: '#number', name: '#string', status: '#string' }**: Kiểm tra cấu trúc JSON với các trường `id` (số), `name` (chuỗi), `status` (chuỗi).
    ```
    
2. **Chạy Collection**:
    - Chạy toàn bộ file .feature bằng lệnh mvn test.
    - Hoặc chạy từng Scenario riêng lẻ trong IDE (như IntelliJ).

### 6.2. Sử dụng biến (tương tự Variables trong Postman)

Karate hỗ trợ biến để tái sử dụng dữ liệu, tương tự Global/Environment Variables trong Postman.

### Cách tạo và sử dụng biến:

1. **Khai báo biến trong file** .feature:
    
    ```gherkin
    Feature: Sử dụng biến
      Background:
        * def baseUrl = 'https://petstore.swagger.io/v2'
        * def petId = 123
    
      Scenario: Thêm thú cưng
        Given url baseUrl + '/pet'
        And request { id: '#(petId)', name: 'MyPet', status: 'available' }
        When method post
        Then status 201
    ```
    
2. **Cập nhật biến động**:
    - Lưu token từ response:
        
        ```gherkin
        Scenario: Lấy token
          Given url 'https://example.com/api/login'
          And request { username: 'user', password: 'pass' }
          When method post
          Then status 200
          * def authToken = response.token
        ```
        
3. **Sử dụng biến trong Scenario khác**:
    
    ```gherkin
    Scenario: Sử dụng token
      Given url 'https://example.com/api/protected'
      And header Authorization = 'Bearer ' + authToken
      When method get
      Then status 200
    ```
    

### So sánh với Postman:

- Postman: Dùng pm.globals.set("token", value).
- Karate: Dùng * def ten_bien = gia_tri.

### 6.3. Viết script để xử lý logic (tương tự Pre-request Script và Tests trong Postman)

Karate cho phép nhúng JavaScript hoặc sử dụng các biểu thức Karate để xử lý logic, tương tự script trong Postman.

### Ví dụ: Kiểm thử API POST

1. Tạo Scenario POST:
    
    ```gherkin
    Scenario: Thêm thú cưng
      Given url 'https://petstore.swagger.io/v2/pet'
      And request { id: 123, name: 'MyPet', status: 'available' }
      When method post
      Then status 201
      And match response == { id: 123, name: 'MyPet', status: 'available' }
    ```
    
2. Thêm logic bằng JavaScript:
    
    ```gherkin
    Scenario: Kiểm tra response phức tạp
      Given url 'https://petstore.swagger.io/v2/pet/123'
      When method get
      Then status 200
      * def expectedName = 'MyPet'
      * def responseName = response.name
      * eval if (responseName != expectedName) karate.fail('Tên không khớp')
    ```
    

### So sánh với Postman:

- Postman: Dùng JavaScript như pm.expect(jsonData.name).to.equal('MyPet').
- Karate: Dùng match hoặc JavaScript nhúng với karate.fail().

### 6.4. Tích hợp dữ liệu từ file ngoài (tương tự Data Files trong Postman)

Karate hỗ trợ đọc dữ liệu từ file CSV, JSON, hoặc YAML để chạy Data-Driven Testing.

### Cách sử dụng:

1. Tạo file CSV (pets.csv):
    
    ```
    id,name,status
    123,MyPet,available
    456,YourPet,sold
    ```
    
2. Sử dụng trong .feature:
    
    ```gherkin
    Feature: Kiểm thử Data-Driven
      Scenario Outline: Thêm nhiều thú cưng
        Given url 'https://petstore.swagger.io/v2/pet'
        And request { id: <id>, name: '<name>', status: '<status>' }
        When method post
        Then status 201
      Examples:
        | read('pets.csv') |
    ```
    

### So sánh với Postman:

- Postman: Dùng file CSV/JSON trong Collection Runner.
- Karate: Dùng read() để nhập file CSV/JSON/YAML.

### 6.5. Tạo báo cáo và lưu kết quả

- Karate tự động tạo báo cáo HTML trong thư mục target/karate-reports sau khi chạy test.
- Báo cáo hiển thị chi tiết pass/fail, thời gian chạy, và log từng request/response.
- So với Postman, báo cáo của Karate tích hợp sẵn, không cần công cụ bổ sung như Newman.

## 7. Lợi ích khi dùng Karate Framework so với chỉ dùng Postman

- **Tự động hóa mạnh mẽ**: Karate hỗ trợ kiểm thử song song, tích hợp CI/CD, và kiểm thử hiệu suất, vượt xa khả năng automation của Postman.
- **Cú pháp đơn giản**: Gherkin dễ đọc, không cần viết code Java phức tạp như Cucumber.
- **Hỗ trợ đa dạng**: Kiểm thử API, UI, mock, và hiệu suất trong một công cụ.
- **Cộng đồng và tài liệu**: Karate có cộng đồng tích cực trên Stack Overflow và tài liệu chi tiết tại karatelabs.github.io.

## 8. Mẹo học Karate Framework hiệu quả

- **Bắt đầu với API testing**: Vì bạn quen với Postman, hãy thử viết các Scenario đơn giản như GET/POST và kiểm tra response.
- **Thực hành với dự án mẫu**: Tải dự án mẫu từ GitHub của Karate (github.com/karatelabs/karate).
- **Xem video hướng dẫn**: Xem video “API Testing with Karate” của Peter Thomas trên YouTube để hiểu cách sử dụng.
- **Tham gia cộng đồng**: Tham gia Stack Overflow (tag karate) hoặc nhóm **Cộng đồng Automation Testing Việt Nam** trên Facebook để hỏi đáp.
