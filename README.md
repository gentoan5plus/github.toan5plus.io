Trang github.toan5plus.io
# Trang thông tin Github Toan5plus
## Tài nguyên của tôi
* [Toan5plus-online](https://sites.google.com/view/toan5plus-online/home)
* [Toan5plus Wordpress](https://dttiovn.wordpress.com)
* [ ]()
## Markkdown
### Liên kết
Để tạo một liên kết, hãy đặt văn bản liên kết trong dấu ngoặc đơn (ví dụ: ) và sau đó ngay lập tức theo sau nó với URL trong ngoặc đơn (ví dụ: ).
[ ]()
* [Markdown syntax ](https://www.markdownguide.org/basic-syntax/#links)
* [Github pages](https://docs.github.com/en/pages/getting-started-with-github-pages/)
* [Bắt đầu nhanh cho GitHub Actions](https://docs.github.com/en/actions/get-started/quickstart)

## Công thức toán
$$ax^3$¢

## Tạo trang web của bạn
### Trước khi có thể tạo trang web của mình, bạn phải có kho lưu trữ cho trang web của mình trên GitHub. 
Nếu bạn không tạo trang web của mình trong kho lưu trữ hiện có, hãy xem [Tạo kho lưu trữ cho trang web của bạn](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site#creating-a-repository-for-your-site).

Cảnh báo

Các trang GitHub Pages có sẵn công khai trên internet, ngay cả khi kho lưu trữ cho trang web là riêng tư (nếu gói hoặc tổ chức của bạn cho phép). Nếu bạn có dữ liệu nhạy cảm trong kho lưu trữ của trang web, bạn có thể muốn xóa dữ liệu trước khi xuất bản. Để biết thêm thông tin, hãy xem Giới thiệu về kho lưu trữ.

### Trên GitHub, điều hướng đến kho lưu trữ trang web của bạn.

Quyết định nguồn xuất bản bạn muốn sử dụng. Xem [Đặt cấu hình nguồn phát hành cho trang GitHub Pages của bạn.](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site).

### Tạo tệp mục nhập cho trang web của bạn. Trang GitHub sẽ tìm kiếm tệp , hoặc tệp làm tệp mục cho trang web của bạn.index.html, index.md, README.md
Nếu nguồn xuất bản của bạn là một nhánh và thư mục, tệp nhập phải ở cấp cao nhất của thư mục nguồn trên nhánh nguồn. Ví dụ: nếu nguồn xuất bản của bạn là thư mục trên nhánh, tệp nhập của bạn phải nằm trong thư mục trên nhánh có tên là ./docsmain/docsmain

Nếu nguồn xuất bản của bạn là quy trình làm việc GitHub Actions, cấu phần phần mềm mà bạn triển khai phải bao gồm tệp mục nhập ở cấp cao nhất của cấu phần phần mềm. Thay vì thêm tệp mục vào kho lưu trữ, bạn có thể chọn để quy trình làm việc GitHub Actions tạo tệp mục nhập khi quy trình làm việc chạy.

### Đặt cấu hình nguồn phát hành của bạn. 
Xem [Đặt cấu hình nguồn phát hành cho trang GitHub Pages của bạn](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site).

Trang GitHub của bạn được xây dựng và triển khai với quy trình làm việc GitHub Actions. Để biết thêm thông tin, hãy xem Xem lịch sử chạy quy trình làm việc.
# Viewing workflow run history

You can view logs for each run of a workflow. Logs include the status for each job and step in a workflow.

Read access to the repository is required to perform these steps.

<div class="ghd-tool webui">

1. On GitHub, navigate to the main page of the repository.
2. Under your repository name, click **<svg version="1.1" width="16" height="16" viewBox="0 0 16 16" class="octicon octicon-play" aria-label="play" role="img"><path d="M8 0a8 8 0 1 1 0 16A8 8 0 0 1 8 0ZM1.5 8a6.5 6.5 0 1 0 13 0 6.5 6.5 0 0 0-13 0Zm4.879-2.773 4.264 2.559a.25.25 0 0 1 0 .428l-4.264 2.559A.25.25 0 0 1 6 10.559V5.442a.25.25 0 0 1 .379-.215Z"></path></svg> Actions**.

   ![Screenshot of the tabs for the "github/docs" repository. The "Actions" tab is highlighted with an orange outline.](/assets/images/help/repository/actions-tab-global-nav-update.png)
3. In the left sidebar, click the workflow you want to see.

   ![Screenshot of the left sidebar of the "Actions" tab. A workflow, "CodeQL," is outlined in dark orange.](/assets/images/help/actions/superlinter-workflow-sidebar.png)
4. From the list of workflow runs, click the name of the run to see the workflow run summary.

</div>

<div class="ghd-tool cli">

> \[!NOTE]
> To learn more about GitHub CLI, see [About GitHub CLI](/en/github-cli/github-cli/about-github-cli).

## Viewing recent workflow runs

To list the recent workflow runs, use the `run list` subcommand.

```shell
gh run list
```

To specify the maximum number of runs to return, you can use the `-L` or `--limit` flag . The default is `10`.

```shell
gh run list --limit 5
```

To only return runs for the specified workflow, you can use the `-w` or `--workflow` flag. Replace `workflow` with either the workflow name, workflow ID, or workflow file name. For example, `"Link Checker"`, `1234567`, or `"link-check-test.yml"`.

```shell
gh run list --workflow WORKFLOW
```

## Viewing details for a specific workflow run

To display details for a specific workflow run, use the `run view` subcommand. Replace `run-id` with the ID of the run that you want to view. If you don't specify a `run-id`, GitHub CLI returns an interactive menu for you to choose a recent run.

```shell
gh run view RUN_ID
```

To include job steps in the output, use the `-v` or `--verbose` flag.

```shell
gh run view RUN_ID --verbose
```

To view details for a specific job in the run, use the `-j` or `--job` flag. Replace `job-id` with the ID of the job that you want to view.

```shell
gh run view --job JOB_ID
```

To view the full log for a job, use the `--log` flag.

```shell
gh run view --job JOB_ID --log
```

Use the `--exit-status` flag to exit with a non-zero status if the run failed. For example:

```shell
gh run view 0451 --exit-status && echo "run pending or passed"
```

</div>
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
