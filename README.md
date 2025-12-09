# TeldriveRcloneApp

Một App để chạy và cấu hình `rclone` cùng với giao diện HTA cho Teldrive. Repo này chứa file HTA để khởi chạy/điều khiển dễ dàng cho việc copy từ google drive sang teldrive. (code xấu nên là cứ đóng góp)

## Yêu cầu (Requirements)

- Windows.
- `rclone` đã cài đặt và nằm trong `PATH`.
- `Teldrive` đã cài đặt và nằm trong `PATH`.
- Trình chạy HTA (Windows hỗ trợ sẵn `.hta`).
- PowerShell (mặc định: `pwsh.exe` nếu dùng PowerShell Core, hoặc `powershell.exe`).

## Hướng dẫn sử dụng (User Guide)

### 1. Tab Teldrive (Home)
- **Executable**: Chọn đường dẫn đến file `teldrive.exe`.
- **Config File**: Chọn file cấu hình `config.toml` của bạn. Nếu để trống, mặc định sẽ dùng `~/.teldrive/config.toml`.
- **Port**: Cổng chạy server (mặc định 8080).
- **Controls**:
  - `Start`: Chạy Teldrive server ở chế độ ngầm (Background).
  - `Stop`: Dừng server.
  - `Open Browser`: Mở giao diện web của Teldrive.
  - Các nút lệnh nhanh: `Check Version`, `Show Help`, `Upgrade`...

### 2. Tab Rclone
- **Setup**: Chọn đường dẫn `rclone.exe` và file `rclone.conf`.
- **WebDAV Server**:
  - Chạy `rclone serve webdav` để tạo server file nội bộ (Mặc định port `8090`).
  - Hỗ trợ nút `Stop` riêng biệt để không ảnh hưởng đến các tiến trình Mount khác.
- **Mount Drive**: Mount remote thành ổ đĩa mạng trên Windows (Ví dụ ổ `Z:`).
- **Copy Tool**: Công cụ hỗ trợ copy dữ liệu giữa các remote (ví dụ từ Google Drive `pgs:` sang `teldrive:`), có sẵn các flag tối ưu (`--update`, `--ignore-existing`).

### 3. Tab Config
- **List Remotes**: Xem danh sách các remote đã cấu hình.
- **Add/Edit (Wizard)**: Mở cửa sổ dòng lệnh để thêm remote mới.
- **Edit Config**: Mở trực tiếp file `conf` bằng Notepad để chỉnh sửa thủ công.


## Tài liệu tham khảo (Tutorial)
- [Hướng dẫn sử dụng chi tiết Teldrive](https://teldrive-docs.pages.dev)

