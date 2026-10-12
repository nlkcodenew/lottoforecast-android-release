# LottoForecast Android — Releases

Kênh phát hành APK cài tay cho app LottoForecast Android
(Kotlin + Jetpack Compose, Material3 Adaptive).

## Cài đặt

1. Vào mục **Releases** bên phải, tải file `app-<version>.apk` mới nhất
   (bản thử nghiệm có chữ `beta` — chỉ cài khi được hướng dẫn).
2. Mở file APK trên điện thoại → cho phép "cài app không rõ nguồn" khi được hỏi,
   hoặc cắm cáp và chạy `adb install -r app-<version>.apk`.
3. Mở app, kết nối WiFi để kích hoạt phiên trial 7 ngày.

Không có cập nhật thầm lặng: mỗi bản mới đều phải tải + cài tay, app sẽ báo
khi có bản mới (màn Cài đặt).

## Kiểm file

Mỗi release đính kèm `.sha256`. Đối chiếu trước khi cài:

```powershell
Get-FileHash app-0.1.0.apk -Algorithm SHA256
```

## Quy ước bản

- `versionCode` tăng đơn điệu; `versionName` bám theo bản Brick khi đạt parity.
- Beta = GitHub Release **prerelease** (không `Latest`), stable mới đánh `Latest`.

## Backend

App dùng backend live `https://api.jonah.io.vn` (Worker + D1).
Trang quản trị hiển thị loại thiết bị (Brick/Android) và trạng thái online.
