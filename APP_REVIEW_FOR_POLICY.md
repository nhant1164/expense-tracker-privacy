# NTN Quản Lý Chi Tiêu - App Review for Policy Writing

## Tổng Quan

| Thông tin     | Chi tiết                               |
| ------------- | -------------------------------------- |
| **Tên App**   | NTN Quản Lý Chi Tiêu (Expense Tracker) |
| **Version**   | 2.0.0                                  |
| **Nền tảng**  | iOS & Android                          |
| **Ngôn ngữ**  | Tiếng Việt, English                    |
| **Đối tượng** | Người dùng từ 13 tuổi trở lên          |

---

## 1. TÍNH NĂNG HIỆN TẠI

### 1.1 Tính năng Miễn phí (Free Tier)

| Tính năng              | Mô tả                                        |
| ---------------------- | -------------------------------------------- |
| **Quản lý giao dịch**  | Thêm, sửa, xóa thu/chi không giới hạn        |
| **Danh mục tùy chỉnh** | Tạo danh mục với icon và màu sắc             |
| **Danh mục con**       | Hệ thống phân cấp 2 level                    |
| **Ngân sách**          | Thiết lập ngân sách theo ngày/tuần/tháng/năm |
| **Thống kê cơ bản**    | Biểu đồ phân tích chi tiêu                   |
| **Quản lý đầu tư**     | Theo dõi cổ phiếu, crypto, bất động sản...   |
| **Xuất CSV**           | Xuất dữ liệu ra file CSV                     |
| **Sao lưu iCloud**     | Sao lưu & khôi phục qua iCloud (iOS)         |
| **Sao lưu thủ công**   | Backup/restore file JSON                     |
| **OCR cơ bản**         | Quét hóa đơn với API mặc định                |
| **Dark/Light mode**    | Giao diện tối/sáng                           |
| **Đa ngôn ngữ**        | Tiếng Việt & English                         |
| **Tìm kiếm & Lọc**     | Tìm kiếm giao dịch theo nhiều tiêu chí       |
| **Đính kèm hình ảnh**  | Gắn hình ảnh hóa đơn vào giao dịch           |
| **Báo cáo PDF**        | Xuất báo cáo chi tiết dạng PDF               |

### 1.2 Tính năng Premium (Trả phí)

| Tính năng             | Mô tả                            | Trạng thái    |
| --------------------- | -------------------------------- | ------------- |
| **Cài đặt OCR**       | Tùy chỉnh API key Gemini/Groq    | ✅ Có sẵn     |
| **Todo & Nhắc nhở**   | Nhắc nhở thanh toán hóa đơn      | 🔜 Sắp ra mắt |
| **Chia sẻ nhóm**      | Chia sẻ chi tiêu với gia đình    | 🔜 Sắp ra mắt |
| **Giao dịch định kỳ** | Tự động thêm giao dịch lặp lại   | 🔜 Sắp ra mắt |
| **Cloud backup**      | Sao lưu không giới hạn lên cloud | 🔜 Sắp ra mắt |

---

## 2. GÓI ĐĂNG KÝ PREMIUM

| Gói          | Product ID                         | Giá         | Thời hạn                   |
| ------------ | ---------------------------------- | ----------- | -------------------------- |
| **Monthly**  | `expense_tracker_premium_monthly`  | $0.99/tháng | Tự động gia hạn hàng tháng |
| **Yearly**   | `expense_tracker_premium_yearly`   | $9.99/năm   | Tự động gia hạn hàng năm   |
| **Lifetime** | `expense_tracker_premium_lifetime` | $39.99      | Một lần, vĩnh viễn         |

### Chính sách thanh toán

- Thanh toán qua App Store (iOS) hoặc Google Play (Android)
- Tự động gia hạn trừ khi hủy trước 24 giờ khi kết thúc chu kỳ
- Quản lý đăng ký trong cài đặt thiết bị
- Hoàn tiền theo chính sách của App Store/Google Play

---

## 3. DỮ LIỆU THU THẬP & LƯU TRỮ

### 3.1 Dữ liệu lưu trữ LOCAL (trên thiết bị người dùng)

#### Database SQLite (`expense_tracker.db`)

| Bảng             | Dữ liệu                                               | Mục đích            |
| ---------------- | ----------------------------------------------------- | ------------------- |
| **transactions** | Số tiền, danh mục, ngày, mô tả, đường dẫn hình ảnh    | Theo dõi thu chi    |
| **categories**   | Tên, icon, màu sắc, loại (thu/chi), danh mục cha      | Phân loại giao dịch |
| **budgets**      | Danh mục, số tiền, chu kỳ, ngày bắt đầu/kết thúc      | Quản lý ngân sách   |
| **investments**  | Tên, loại, số tiền, giá trị, ngày mua/bán, trạng thái | Theo dõi đầu tư     |

#### Secure Storage (Keychain/EncryptedSharedPreferences)

- API keys Gemini (mã hóa)
- API keys Groq (mã hóa)
- Trạng thái subscriber
- Cài đặt OCR provider

#### Shared Preferences

- Theme preference (light/dark/system)
- Language preference (vi/en)

#### Local Files

- Hình ảnh hóa đơn đính kèm giao dịch
- File backup JSON

### 3.2 Dữ liệu KHÔNG thu thập

| Loại dữ liệu                        | Trạng thái        |
| ----------------------------------- | ----------------- |
| Thông tin cá nhân (tên, email, SĐT) | ❌ Không thu thập |
| Vị trí địa lý                       | ❌ Không thu thập |
| Danh bạ                             | ❌ Không thu thập |
| Dữ liệu analytics/tracking          | ❌ Không thu thập |
| Advertising ID                      | ❌ Không thu thập |

### 3.3 Dữ liệu gửi đến dịch vụ bên thứ 3

| Dịch vụ                     | Dữ liệu gửi                      | Mục đích                | Lưu trữ                       |
| --------------------------- | -------------------------------- | ----------------------- | ----------------------------- |
| **Google Gemini API**       | Hình ảnh hóa đơn                 | Nhận dạng văn bản (OCR) | Không lưu trữ                 |
| **Groq API**                | Hình ảnh hóa đơn                 | OCR dự phòng            | Không lưu trữ                 |
| **RevenueCat**              | Trạng thái mua hàng, App User ID | Quản lý subscription    | Có (theo policy RevenueCat)   |
| **Firebase Remote Config**  | Không có dữ liệu người dùng      | Cấu hình app            | Không                         |
| **App Store / Google Play** | Thông tin thanh toán             | Xử lý mua hàng          | Có (theo policy Apple/Google) |
| **iCloud (iOS)**            | File backup                      | Sao lưu dữ liệu         | Có (theo policy Apple)        |

---

## 4. DỊCH VỤ BÊN THỨ 3

### 4.1 RevenueCat

- **Mục đích**: Quản lý gói đăng ký Premium
- **SDK**: `purchases_flutter: ^9.10.7`
- **Dữ liệu**: Lịch sử mua, trạng thái subscription, App User ID
- **Privacy Policy**: https://www.revenuecat.com/privacy

### 4.2 Google Gemini API

- **Mục đích**: Nhận dạng văn bản từ hình ảnh hóa đơn (OCR)
- **Endpoint**: `https://generativelanguage.googleapis.com/v1beta/models`
- **Model**: `gemini-2.0-flash`
- **Dữ liệu**: Hình ảnh hóa đơn (chỉ xử lý, không lưu trữ vĩnh viễn)
- **Privacy Policy**: https://policies.google.com/privacy

### 4.3 Groq API

- **Mục đích**: Dịch vụ OCR dự phòng khi Gemini không khả dụng
- **Endpoint**: `https://api.groq.com/openai/v1/chat/completions`
- **Model**: `meta-llama/llama-4-scout-17b-16e-instruct`
- **Dữ liệu**: Hình ảnh hóa đơn (chỉ xử lý, không lưu trữ)
- **Privacy Policy**: https://groq.com/privacy-policy

### 4.4 Firebase (Google)

- **Mục đích**: Remote Config để cấu hình app từ xa
- **SDK**: `firebase_core: ^3.6.0`, `firebase_remote_config`
- **Dữ liệu**: Không thu thập dữ liệu người dùng
- **Privacy Policy**: https://firebase.google.com/support/privacy

### 4.5 Apple iCloud

- **Mục đích**: Sao lưu dữ liệu (chỉ iOS)
- **Dữ liệu**: File backup chứa giao dịch, danh mục, ngân sách, đầu tư
- **Privacy Policy**: https://www.apple.com/legal/privacy

---

## 5. BẢO MẬT

### 5.1 Mã hóa dữ liệu

| Platform    | Phương thức                      | Dữ liệu được bảo vệ         |
| ----------- | -------------------------------- | --------------------------- |
| **iOS**     | Keychain (hardware encryption)   | API keys, subscriber status |
| **Android** | EncryptedSharedPreferences (AES) | API keys, subscriber status |

### 5.2 Truyền tải dữ liệu

- Tất cả API calls sử dụng HTTPS
- Hình ảnh được nén trước khi gửi đến OCR API
- Không gửi dữ liệu qua kết nối không mã hóa

### 5.3 Quyền ứng dụng

| Quyền             | Mục đích                  | Bắt buộc |
| ----------------- | ------------------------- | -------- |
| **Camera**        | Chụp ảnh hóa đơn          | Không    |
| **Photo Library** | Chọn ảnh từ thư viện      | Không    |
| **Internet**      | Gọi API OCR, subscription | Có       |
| **iCloud**        | Sao lưu dữ liệu (iOS)     | Không    |

---

## 6. QUYỀN CỦA NGƯỜI DÙNG

| Quyền                 | Cách thực hiện                           |
| --------------------- | ---------------------------------------- |
| **Xem dữ liệu**       | Xem tất cả trong app                     |
| **Xuất dữ liệu**      | Menu > Dữ liệu & Sao lưu > Xuất CSV/JSON |
| **Xóa dữ liệu**       | Xóa từng giao dịch hoặc xóa app          |
| **Sao lưu dữ liệu**   | Menu > Dữ liệu & Sao lưu > Sao lưu       |
| **Khôi phục dữ liệu** | Menu > Dữ liệu & Sao lưu > Khôi phục     |
| **Hủy subscription**  | Cài đặt thiết bị > App Store/Play Store  |

---

## 7. THÔNG TIN LIÊN HỆ

| Thông tin          | Chi tiết       |
| ------------------ | -------------- |
| **Nhà phát triển** | NTN            |
| **Email hỗ trợ**   | [Thêm email]   |
| **Website**        | [Thêm website] |

---

## 8. CHECKLIST CHO PRIVACY POLICY

### Bắt buộc đưa vào:

- [ ] Loại dữ liệu thu thập (chỉ local storage)
- [ ] Mục đích sử dụng dữ liệu (quản lý tài chính cá nhân)
- [ ] Dịch vụ bên thứ 3 và link privacy policy của họ
- [ ] Cách bảo mật dữ liệu (encryption)
- [ ] Quyền của người dùng (xóa, xuất dữ liệu)
- [ ] Chính sách trẻ em (không dành cho dưới 13 tuổi)
- [ ] Cách liên hệ
- [ ] Ngày cập nhật policy
- [ ] Cách thông báo thay đổi policy

### Nên đưa vào:

- [ ] Giải thích OCR gửi hình ảnh đến API
- [ ] iCloud backup (iOS)
- [ ] RevenueCat xử lý subscription
- [ ] Không bán/chia sẻ dữ liệu cho quảng cáo

---

## 9. CHECKLIST CHO TERMS OF SERVICE

### Bắt buộc đưa vào:

- [ ] Mô tả dịch vụ (app quản lý chi tiêu)
- [ ] Điều kiện sử dụng (từ 13 tuổi)
- [ ] Quy định về thanh toán và hoàn tiền
- [ ] Giới hạn trách nhiệm
- [ ] Quyền sở hữu trí tuệ
- [ ] Chấm dứt dịch vụ
- [ ] Luật áp dụng

### Nên đưa vào:

- [ ] Hành vi bị cấm
- [ ] Disclaimer về quyết định tài chính
- [ ] Thay đổi điều khoản
- [ ] Liên hệ hỗ trợ

---

## 10. TÍNH NĂNG SẮP TỚI

| Tính năng           | Mô tả                                | Tier    |
| ------------------- | ------------------------------------ | ------- |
| Todo & Nhắc nhở     | Nhắc nhở thanh toán hóa đơn          | Premium |
| Chia sẻ nhóm        | Chia sẻ chi tiêu với gia đình/bạn bè | Premium |
| Giao dịch định kỳ   | Tự động tạo giao dịch lặp lại        | Premium |
| Cloud backup        | Sao lưu không giới hạn lên cloud     | Premium |
| Đồng bộ đa thiết bị | Sync dữ liệu giữa các thiết bị       | Premium |

---

_Tài liệu này được tạo để hỗ trợ viết Privacy Policy và Terms of Service cho app NTN Quản Lý Chi Tiêu._

_Cập nhật lần cuối: Tháng 1, 2026_
