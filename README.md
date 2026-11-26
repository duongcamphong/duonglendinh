# Đường lên đỉnh

Phần mềm thi 4 phần (Khởi động, Vượt chướng ngại vật, Tăng tốc, Về đích), có tự cập nhật.

## Cần cài trên máy build (1 lần)
Python 3 (có Tkinter) và [Inno Setup 6](https://jrsoftware.org/isinfo.php).

## Phát hành bản mới
1. Sửa code, tăng số `VERSION = "x.y.z"` trong `duong_len_dinh.pyw`.
2. Bấm đúp `build.bat` → ra:
   - `installer_output\DuongLenDinh_Setup_x.y.z.exe`: bộ cài, gửi cho người dùng cài lần đầu.
   - `dist\DuongLenDinh.exe` và `version.json`: để cập nhật.
3. Trên GitHub: tạo Release tag `vx.y.z`, đính kèm `dist\DuongLenDinh.exe`; rồi thay `version.json` ở nhánh `main` bằng file vừa tạo (repo phải Public).

Máy đã cài sẽ tự hỏi cập nhật khi mở app (hoặc menu Tệp → Kiểm tra cập nhật). Dữ liệu nằm ở `%APPDATA%\DuongLenDinh` nên không mất khi cập nhật.

Nếu repo không phải `duongcamphong/duonglendinh`, sửa `UPDATE_URL` trong `.pyw` và `REPO` trong `build.bat` cho khớp.
