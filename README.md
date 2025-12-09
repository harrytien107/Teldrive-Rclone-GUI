# TeldriveRcloneApp

Một App để chạy và cấu hình `rclone` cùng với giao diện HTA cho Teldrive. Repo này chứa file HTA để khởi chạy/điều khiển dễ dàng cho việc copy từ google drive sang teldrive. (code xấu nên là cứ đóng góp)

## Nội dung repo

- `TeldriveRclone.hta` : Giao diện HTA (HTML Application) dùng trên Windows để khởi chạy hoặc hiển thị trạng thái.

## Cách dùng
- Bấm vào file hta và try to understand on your own.

## Yêu cầu

- Windows (đã test trên Windows 11).
- `rclone` đã cài đặt và nằm trong `PATH`.
- Trình chạy HTA (Windows hỗ trợ sẵn `.hta`).
- PowerShell (mặc định: `pwsh.exe` nếu dùng PowerShell Core, hoặc `powershell.exe`).

## Logging & Hiển thị

- Xem `Teldrive HTA Visibility & Logging.md` để biết chi tiết về các thiết lập hiển thị và logging.
- Nếu cần bật `rclone` logging chi tiết, thêm tham số `-v` hoặc `--log-level DEBUG` và `--log-file "path\to\log.txt"`.

```powershell
rclone copy "C:\local\path" remote:bucket --log-level DEBUG --log-file "C:\temp\rclone-log.txt"
```