# github.toan5plus.io
Trang thông tin Github Toan5plus
# Markkdown
## Liên kết
Để tạo một liên kết, hãy đặt văn bản liên kết trong dấu ngoặc đơn (ví dụ: ) và sau đó ngay lập tức theo sau nó với URL trong ngoặc đơn (ví dụ: ).[Duck Duck Go](https://duckduckgo.com)
* [Markdown syntax ](https://www.markdownguide.org/basic-syntax/#links)
* [Github pages](https://docs.github.com/en/pages/getting-started-with-github-pages/)

# Tạo trang web của bạn
### Trước khi có thể tạo trang web của mình, bạn phải có kho lưu trữ cho trang web của mình trên GitHub. 
Nếu bạn không tạo trang web của mình trong kho lưu trữ hiện có, hãy xem [Tạo kho lưu trữ cho trang web của bạn](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site#creating-a-repository-for-your-site).

Cảnh báo

Các trang GitHub Pages có sẵn công khai trên internet, ngay cả khi kho lưu trữ cho trang web là riêng tư (nếu gói hoặc tổ chức của bạn cho phép). Nếu bạn có dữ liệu nhạy cảm trong kho lưu trữ của trang web, bạn có thể muốn xóa dữ liệu trước khi xuất bản. Để biết thêm thông tin, hãy xem Giới thiệu về kho lưu trữ.

### Trên GitHub, điều hướng đến kho lưu trữ trang web của bạn.

Quyết định nguồn xuất bản bạn muốn sử dụng. Xem Đặt cấu hình nguồn phát hành cho trang GitHub Pages của bạn.

Tạo tệp mục nhập cho trang web của bạn. Trang GitHub sẽ tìm kiếm tệp , hoặc tệp làm tệp mục cho trang web của bạn.index.html, index.md, README.md
Nếu nguồn xuất bản của bạn là một nhánh và thư mục, tệp nhập phải ở cấp cao nhất của thư mục nguồn trên nhánh nguồn. Ví dụ: nếu nguồn xuất bản của bạn là thư mục trên nhánh, tệp nhập của bạn phải nằm trong thư mục trên nhánh có tên là ./docsmain/docsmain

Nếu nguồn xuất bản của bạn là quy trình làm việc GitHub Actions, cấu phần phần mềm mà bạn triển khai phải bao gồm tệp mục nhập ở cấp cao nhất của cấu phần phần mềm. Thay vì thêm tệp mục vào kho lưu trữ, bạn có thể chọn để quy trình làm việc GitHub Actions tạo tệp mục nhập khi quy trình làm việc chạy.

### Đặt cấu hình nguồn phát hành của bạn. Xem Đặt cấu hình nguồn phát hành cho trang GitHub Pages của bạn.

Trang GitHub của bạn được xây dựng và triển khai với quy trình làm việc GitHub Actions. Để biết thêm thông tin, hãy xem Xem lịch sử chạy quy trình làm việc.

Lưu ý

GitHub Actions miễn phí cho các kho lưu trữ công cộng. Phí sử dụng áp dụng cho các kho lưu trữ riêng tư và nội bộ vượt quá mức phân bổ số phút miễn phí hàng tháng. Để biết thêm thông tin, hãy xem Thanh toán và sử dụng.

### Xem trang web đã xuất bản của bạn
Trong tên kho lưu trữ của bạn, hãy nhấp vàoCài đặt. Nếu bạn không thấy tab "Cài đặt", hãy chọnmenu thả xuống, sau đó nhấp vào Cài đặt.

Screenshot of a repository header showing the tabs. The "Settings" tab is highlighted by a dark orange outline.
Trong phần "Mã và tự động hóa" của thanh bên, hãy nhấp vàoTrang.

Để xem trang web đã xuất bản của bạn, trong phần "Trang GitHub", hãy nhấp vàoTruy cập trang web.

Lưu ý

Có thể mất đến 10 phút để các thay đổi đối với trang web của bạn xuất bản sau khi bạn đẩy các thay đổi lên GitHub. Nếu bạn không thấy các thay đổi về trang web GitHub Pages của mình được phản ánh trong trình duyệt của mình sau một giờ, hãy xem Giới thiệu về lỗi xây dựng Jekyll cho các trang web GitHub Pages.

Nếu bạn đang phát hành từ một chi nhánh và trang web của bạn chưa tự động xuất bản, hãy đảm bảo rằng ai đó có quyền quản trị viên và địa chỉ email đã xác minh đã được đẩy đến nguồn phát hành.
Các commit được đẩy bởi quy trình làm việc GitHub Actions sử dụng bản dựng không kích hoạt GitHub Pages.GITHUB_TOKEN
Trình tạo trang web tĩnh
GitHub Pages xuất bản bất kỳ tệp tĩnh nào mà bạn đẩy vào kho lưu trữ của mình. Bạn có thể tạo các tệp tĩnh của riêng mình hoặc sử dụng trình tạo trang web tĩnh để xây dựng trang web cho bạn. Bạn cũng có thể tùy chỉnh quy trình xây dựng của riêng mình cục bộ hoặc trên một máy chủ khác.

Nếu bạn sử dụng quy trình xây dựng tùy chỉnh hoặc trình tạo trang web tĩnh không phải Jekyll, bạn có thể viết quy trình làm việc GitHub Actions để xây dựng và xuất bản trang web của mình. GitHub cung cấp các mẫu quy trình làm việc cho một số trình tạo trang web tĩnh. Để biết thêm thông tin, hãy xem Đặt cấu hình nguồn phát hành cho trang GitHub của bạn.

Nếu bạn xuất bản trang web của mình từ một nhánh nguồn, GitHub Pages sẽ sử dụng Jekyll để xây dựng trang web của bạn theo mặc định. Nếu bạn muốn sử dụng trình tạo trang web tĩnh không phải Jekyll, chúng tôi khuyên bạn nên viết GitHub Actions để xây dựng và xuất bản trang web của mình. Nếu không, hãy tắt quy trình xây dựng Jekyll bằng cách tạo một tệp trống được gọi trong thư mục gốc của nguồn xuất bản của bạn, sau đó làm theo hướng dẫn của trình tạo trang web tĩnh để xây dựng trang web của bạn cục bộ..nojekyll

Lưu ý

GitHub Pages không hỗ trợ các ngôn ngữ phía máy chủ như PHP, Ruby hoặc Python.

### Các loại MIME trên Trang GitHub
Loại MIME là tiêu đề mà máy chủ gửi đến trình duyệt, cung cấp thông tin về bản chất và định dạng của các tệp mà trình duyệt yêu cầu. GitHub Pages hỗ trợ hơn 750 loại MIME trên hàng nghìn phần mở rộng tệp. Danh sách các loại MIME được hỗ trợ được tạo từ dự án mime-db.

Mặc dù bạn không thể chỉ định các loại MIME tùy chỉnh trên cơ sở mỗi tệp hoặc mỗi kho lưu trữ, nhưng bạn có thể thêm hoặc sửa đổi các loại MIME để sử dụng trên Trang GitHub. Để biết thêm thông tin, hãy xem hướng dẫn đóng góp mime-db.

### Các bước tiếp theo
Bạn có thể thêm nhiều trang hơn vào trang web của mình bằng cách tạo thêm tệp mới. Mỗi tệp sẽ có sẵn trên trang web của bạn trong cùng cấu trúc thư mục với nguồn xuất bản của bạn. Ví dụ: nếu nguồn phát hành cho site dự án của bạn là nhánh và bạn tạo một tệp mới được gọi trên nhánh, tệp sẽ có sẵn tại .gh-pages/about/contact-us.mdgh-pageshttps://<user>.github.io/<repository>/about/contact-us.html

Bạn cũng có thể thêm chủ đề để tùy chỉnh giao diện trang web của mình. Để biết thêm thông tin, hãy xem Thêm chủ đề vào trang GitHub của bạn bằng Jekyll.

## Đọc thêm
*Giới thiệu về GitHub Pages và Jekyll.
*Khắc phục lỗi bản dựng Jekyll cho các trang web GitHub Pages
*Tạo và xóa các nhánh trong kho lưu trữ của bạn
*Tạo tệp mới
*Khắc phục lỗi 404 cho các trang web GitHub Pages
