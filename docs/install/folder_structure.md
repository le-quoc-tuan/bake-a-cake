### Config

Thư mục này chứa các file cấu hình của CakePHP, trong đó cần chú ý các file:

* `core.php` chứa các tham số cơ bản của project
* `database.php` chứa thông tin kết nối đến database server
* `router.php` chứa các thông tin của bộ điều tuyến. Tuy nhiên trong hầu hết các trường hợp, ta chỉ sử dụng cấu hình route mặc định của CakePHP

### Controller

Chứa các file controller của project

* `AppController.php` định nghĩa class `AppController`. AppController là class cha của tất cả các class controller trong projects. Do đó các cài đặt dùng chung cho tất cả các controller được đặt tại đây.
* `Components` chứa các file *component*. Component là các đoạn mã mở rộng cho Controller

### View

Chứa các file view của project

* `Layouts` chứa các file layout của project. File layout chứa thông tin về cấu trúc, bố trí của các view
* `Elements` chứa các file *element*. Element là các đoạn mã mở rộng cho View

### Model

Chứa các file model của project

* `AppModel.php` định nghĩa class `AppModel`. AppModel là class cha của tất cả các class model trong projects. Do đó các cài đặt dùng chung cho tất cả các model được đặt tại đây.
* `Behaviors` chứa các file *behavior*. Behavior là các đoạn mã mở rộng cho Model

### webroot

Đóng vai trò là thư mục gốc (*root directory*) của project. Trong thư mục này bao gồm các file css, javascript, image chứa trong các thư mục tương ứng.
