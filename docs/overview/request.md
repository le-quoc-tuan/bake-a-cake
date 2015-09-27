## Mô hình MVC

Mô hình MVC là viết tắt của Model-View-Controller (hay khối-dữ-liệu, khung-nhìn, và khối-điều-khiển) là một mô hình thường được sử dụng trong quá trình phát triển website. Mục đích của mô hình là giúp người phát triển phân tách mã code của họ thành 3 thành phần khác nhau, mỗi thành phần đảm nhiệm một nhiệm vụ riêng biệt

* **MODEL** - Khối dữ liệu
    - Đây là thành phần chứa tất cả các nghiệp vụ logic, phương thức xử lý, truy xuất, làm việc với database.
* **VIEW** - Khung nhìn
	- Đảm nhận việc hiển thị thông tin, tương tác với người dùng. Thành phần này bao gồm tất cả các giao diện người dùng (*user interface*) như text, hình ảnh, bảng biểu, ...
* **CONTROLLER** - Khối điều khiển
	- Khối này làm nhiệm vụ điều hướng, xử lý các logic, trung chuyển dữ liệu giữa khối dữ liệu và khung nhìn.

## Diễn biến của một truy cập web thông thường

![basic web request](/img/basic_mvc.png)

* Mọi chuyện bắt đầu khi một người dùng A truy cập vào một địa chỉ (*web address*) trên trình duyệt (*web browser*) của anh ta, chẳng hạn như `http://www.bakery.com/cakes/list` , trình duyệt của anh ta sẽ gửi một yêu cầu (*request*) tới *web server*
* Tại *web server*, bộ định tuyến (*router*) sẽ phân tách *request* thành các tham số để xác định *controller*, *action* nào sẽ xử lý *request* này. Ở đây, request sẽ được xử lý trong `function list() {}` của `CakesController`
* Trong *action*, một đoạn mã (*code*) sẽ gọi đến *model* tương ứng để lấy tất cả các loại bánh hiện đang có.
* *model* sẽ truy cập dữ liệu từ *database*, lấy ra danh sách các loại bánh rồi trả lại cho *controller*
* *controller* truyền dữ liệu nhận được từ *model* xuống *view*
* Tại *view*, dữ liệu được thể hiện dưới các đoạn mã html
* Cuối cùng, *web server* trả lại một hồi đáp (*response*) tới *web brower* của A. Tại đây các mã html được trình bày thành text, hình ảnh mà A nhìn thấy.
