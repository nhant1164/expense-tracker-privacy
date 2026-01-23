# CHÍNH SÁCH BẢO MẬT - NTN QUẢN LÝ CHI TIÊU

**Cập nhật lần cuối: Tháng 1, 2026**

## 1. THÔNG TIN CHUNG

Ứng dụng "NTN Quản Lý Chi Tiêu" (Expense Tracker) được phát triển bởi NTN. Chúng tôi cam kết bảo vệ quyền riêng tư và thông tin cá nhân của người dùng. Chính sách này giải thích cách chúng tôi thu thập, sử dụng và bảo vệ thông tin của bạn khi sử dụng ứng dụng.

**Ứng dụng dành cho người dùng từ 13 tuổi trở lên.**

## 2. THÔNG TIN THU THẬP

### 2.1 Dữ liệu lưu trữ LOCAL (trên thiết bị)

Ứng dụng lưu trữ dữ liệu trực tiếp trên thiết bị của bạn, bao gồm:

- **Thông tin giao dịch**: Số tiền, danh mục, ngày tháng, mô tả, đường dẫn hình ảnh đính kèm
- **Danh mục chi tiêu**: Tên, icon, màu sắc, loại (thu/chi), danh mục cha
- **Ngân sách**: Danh mục, số tiền, chu kỳ, ngày bắt đầu/kết thúc
- **Dữ liệu đầu tư**: Tên, loại, số tiền, giá trị, ngày mua/bán, trạng thái
- **Cài đặt ứng dụng**: Theme (light/dark/system), ngôn ngữ (vi/en)
- **API keys** (nếu bạn tự cấu hình): Được mã hóa và lưu trong Keychain (iOS) hoặc EncryptedSharedPreferences (Android)

### 2.2 Dữ liệu KHÔNG thu thập

Chúng tôi **KHÔNG** thu thập:

- Thông tin cá nhân (tên, email, số điện thoại)
- Vị trí địa lý
- Danh bạ
- Dữ liệu analytics/tracking
- Advertising ID

## 3. DỊCH VỤ BÊN THỨ 3

Ứng dụng có tích hợp một số dịch vụ bên thứ 3 để cung cấp các tính năng:

### 3.1 Google Gemini API (OCR)

- **Mục đích**: Nhận dạng văn bản từ hình ảnh hóa đơn
- **Dữ liệu gửi**: Hình ảnh hóa đơn (chỉ xử lý, không lưu trữ vĩnh viễn)
- **Privacy Policy**: https://policies.google.com/privacy

### 3.2 Groq API (OCR dự phòng)

- **Mục đích**: Dịch vụ OCR dự phòng khi Gemini không khả dụng
- **Dữ liệu gửi**: Hình ảnh hóa đơn (chỉ xử lý, không lưu trữ)
- **Privacy Policy**: https://groq.com/privacy-policy

### 3.3 RevenueCat

- **Mục đích**: Quản lý gói đăng ký Premium
- **Dữ liệu gửi**: Trạng thái mua hàng, App User ID
- **Privacy Policy**: https://www.revenuecat.com/privacy

### 3.4 Firebase Remote Config

- **Mục đích**: Cấu hình ứng dụng từ xa
- **Dữ liệu gửi**: Không có dữ liệu người dùng
- **Privacy Policy**: https://firebase.google.com/support/privacy

### 3.5 Apple iCloud (chỉ iOS)

- **Mục đích**: Sao lưu dữ liệu
- **Dữ liệu gửi**: File backup chứa giao dịch, danh mục, ngân sách, đầu tư
- **Privacy Policy**: https://www.apple.com/legal/privacy

### 3.6 App Store / Google Play

- **Mục đích**: Xử lý mua hàng
- **Dữ liệu gửi**: Thông tin thanh toán (theo chính sách của Apple/Google)

## 4. CÁCH SỬ DỤNG THÔNG TIN

Dữ liệu được thu thập chỉ nhằm mục đích:

- Hiển thị và quản lý thông tin tài chính cá nhân của bạn
- Tạo biểu đồ và thống kê chi tiêu
- Nhận dạng hóa đơn qua OCR (khi bạn sử dụng tính năng này)
- Xuất dữ liệu CSV/JSON/PDF theo yêu cầu
- Sao lưu và khôi phục dữ liệu

## 5. CHIA SẺ THÔNG TIN

**Chúng tôi KHÔNG bán hoặc chia sẻ dữ liệu của bạn cho mục đích quảng cáo.**

Dữ liệu chỉ được chia sẻ với các dịch vụ bên thứ 3 được liệt kê ở mục 3, và chỉ khi bạn sử dụng các tính năng liên quan.

## 6. BẢO MẬT DỮ LIỆU

### 6.1 Mã hóa dữ liệu

| Platform    | Phương thức                      | Dữ liệu được bảo vệ         |
| ----------- | -------------------------------- | --------------------------- |
| **iOS**     | Keychain (hardware encryption)   | API keys, subscriber status |
| **Android** | EncryptedSharedPreferences (AES) | API keys, subscriber status |

### 6.2 Truyền tải dữ liệu

- Tất cả API calls sử dụng HTTPS
- Hình ảnh được nén trước khi gửi đến OCR API
- Không gửi dữ liệu qua kết nối không mã hóa

## 7. QUYỀN TRUY CẬP ỨNG DỤNG

| Quyền             | Mục đích                      | Bắt buộc |
| ----------------- | ----------------------------- | -------- |
| **Camera**        | Chụp ảnh hóa đơn              | Không    |
| **Photo Library** | Chọn ảnh từ thư viện          | Không    |
| **Internet**      | Gọi API OCR, quản lý đăng ký  | Có       |
| **iCloud**        | Sao lưu dữ liệu (chỉ iOS)     | Không    |

## 8. QUYỀN CỦA NGƯỜI DÙNG

Bạn có các quyền sau:

| Quyền                 | Cách thực hiện                           |
| --------------------- | ---------------------------------------- |
| **Xem dữ liệu**       | Xem tất cả trong ứng dụng                |
| **Xuất dữ liệu**      | Menu > Dữ liệu & Sao lưu > Xuất CSV/JSON |
| **Xóa dữ liệu**       | Xóa từng giao dịch hoặc xóa ứng dụng     |
| **Sao lưu dữ liệu**   | Menu > Dữ liệu & Sao lưu > Sao lưu       |
| **Khôi phục dữ liệu** | Menu > Dữ liệu & Sao lưu > Khôi phục     |
| **Hủy subscription**  | Cài đặt thiết bị > App Store/Play Store  |

## 9. ĐĂNG KÝ PREMIUM (SUBSCRIPTION)

### 9.1 Các gói đăng ký

| Gói                        | Giá         | Thời hạn                              |
| -------------------------- | ----------- | ------------------------------------- |
| **Monthly (Gói Tháng)**    | $0.99/tháng | Tự động gia hạn hàng tháng            |
| **Yearly (Gói Năm)**       | $9.99/năm   | Tự động gia hạn hàng năm              |
| **Lifetime (Trọn đời)**    | $39.99      | Thanh toán một lần, sử dụng vĩnh viễn |

### 9.2 Thanh toán

- Thanh toán được xử lý hoàn toàn qua Apple App Store (iOS) hoặc Google Play Store (Android)
- Giá được hiển thị bằng đồng tiền địa phương của bạn
- Chúng tôi không lưu trữ thông tin thanh toán của bạn

### 9.3 Tự động gia hạn

- Đăng ký tự động gia hạn trừ khi bị hủy ít nhất 24 giờ trước khi kết thúc chu kỳ hiện tại
- Tài khoản Apple ID/Google của bạn sẽ bị tính phí gia hạn trong vòng 24 giờ trước khi kết thúc chu kỳ
- Giá gia hạn bằng với giá gói đăng ký hiện tại

### 9.4 Dùng thử miễn phí (Free Trial)

- Một số gói có thể bao gồm thời gian dùng thử miễn phí 7 ngày
- Bạn có thể hủy bất cứ lúc nào trong thời gian dùng thử mà không bị tính phí
- Nếu không hủy trước khi kết thúc thời gian dùng thử, đăng ký sẽ tự động chuyển sang gói trả phí
- Phần chưa sử dụng của thời gian dùng thử miễn phí sẽ bị mất khi mua đăng ký

### 9.5 Quản lý và hủy đăng ký

**Trên iOS:**
1. Mở **Cài đặt (Settings)** trên iPhone/iPad
2. Nhấn vào tên của bạn (Apple ID) ở đầu màn hình
3. Chọn **Đăng ký (Subscriptions)**
4. Chọn "NTN Quản Lý Chi Tiêu" và nhấn **Hủy đăng ký (Cancel Subscription)**

**Trên Android:**
1. Mở **Google Play Store**
2. Nhấn vào biểu tượng tài khoản > **Payments & subscriptions** > **Subscriptions**
3. Chọn "NTN Quản Lý Chi Tiêu" và nhấn **Cancel subscription**

> **Lưu ý:** Việc hủy sẽ có hiệu lực vào cuối chu kỳ thanh toán hiện tại. Bạn vẫn có thể sử dụng các tính năng Premium cho đến khi hết chu kỳ.

### 9.6 Hoàn tiền

- Yêu cầu hoàn tiền được xử lý theo chính sách của Apple/Google
- **iOS:** Liên hệ [Apple Support](https://support.apple.com/) hoặc truy cập [reportaproblem.apple.com](https://reportaproblem.apple.com/)
- **Android:** Liên hệ [Google Play Support](https://support.google.com/googleplay)

### 9.7 Điều khoản sử dụng

Việc sử dụng ứng dụng và các gói đăng ký Premium tuân theo:
- [Điều khoản sử dụng của NTN Quản Lý Chi Tiêu](terms-of-service.html)
- [Apple's Standard EULA (Licensed Application End User License Agreement)](https://www.apple.com/legal/internet-services/itunes/dev/stdeula/)

## 10. CHÍNH SÁCH TRẺ EM

Ứng dụng không dành cho trẻ em dưới 13 tuổi. Chúng tôi không cố ý thu thập thông tin từ trẻ em dưới 13 tuổi.

## 11. LIÊN HỆ

Nếu bạn có câu hỏi về chính sách bảo mật này, vui lòng liên hệ:

- **Email**: nhant.guide@gmail.com

## 12. THAY ĐỔI CHÍNH SÁCH

Chúng tôi có thể cập nhật chính sách bảo mật này theo thời gian. Mọi thay đổi quan trọng sẽ được thông báo trong ứng dụng. Bạn nên định kỳ xem lại chính sách này để cập nhật các thay đổi.

## 13. CHẤP NHẬN CHÍNH SÁCH

Bằng cách sử dụng ứng dụng "NTN Quản Lý Chi Tiêu", bạn đồng ý với các điều khoản trong chính sách bảo mật này.

---

_Chính sách này tuân thủ theo quy định về bảo vệ dữ liệu cá nhân và các luật liên quan tại Việt Nam._
