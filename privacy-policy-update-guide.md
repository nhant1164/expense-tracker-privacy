# Hướng dẫn cập nhật Privacy Policy cho Apple Review

## Mục đích
Bổ sung nội dung về Subscription để đáp ứng yêu cầu Apple App Store Review Guideline 3.1.2.

## URL cần cập nhật
**https://nhant1164.github.io/expense-tracker-privacy/privacy-policy.html**

---

## Nội dung cần thêm (Tiếng Việt)

Thêm section mới sau phần "Dịch vụ bên thứ ba" hoặc cuối trang:

```html
<h2>Đăng ký Premium (Subscription)</h2>

<h3>Các gói đăng ký</h3>
<ul>
  <li><strong>Gói Tháng (Monthly):</strong> Tự động gia hạn hàng tháng</li>
  <li><strong>Gói Năm (Yearly):</strong> Tự động gia hạn hàng năm</li>
  <li><strong>Gói Trọn đời (Lifetime):</strong> Thanh toán một lần, sử dụng vĩnh viễn</li>
</ul>

<h3>Thanh toán</h3>
<ul>
  <li>Thanh toán được xử lý hoàn toàn qua Apple App Store</li>
  <li>Giá được hiển thị bằng đồng tiền địa phương của bạn</li>
  <li>Chúng tôi không lưu trữ thông tin thanh toán của bạn</li>
</ul>

<h3>Tự động gia hạn</h3>
<ul>
  <li>Đăng ký tự động gia hạn trừ khi bị hủy ít nhất 24 giờ trước khi kết thúc chu kỳ hiện tại</li>
  <li>Tài khoản Apple ID của bạn sẽ bị tính phí gia hạn trong vòng 24 giờ trước khi kết thúc chu kỳ</li>
  <li>Giá gia hạn bằng với giá gói đăng ký hiện tại</li>
</ul>

<h3>Dùng thử miễn phí (Free Trial)</h3>
<ul>
  <li>Một số gói có thể bao gồm thời gian dùng thử miễn phí 7 ngày</li>
  <li>Bạn có thể hủy bất cứ lúc nào trong thời gian dùng thử mà không bị tính phí</li>
  <li>Nếu không hủy trước khi kết thúc thời gian dùng thử, đăng ký sẽ tự động chuyển sang gói trả phí</li>
</ul>

<h3>Quản lý và hủy đăng ký</h3>
<p>Để quản lý hoặc hủy đăng ký:</p>
<ol>
  <li>Mở <strong>Cài đặt</strong> trên iPhone/iPad</li>
  <li>Nhấn vào tên của bạn (Apple ID) ở đầu màn hình</li>
  <li>Chọn <strong>Đăng ký (Subscriptions)</strong></li>
  <li>Chọn "NTN Quản Lý Chi Tiêu" và nhấn <strong>Hủy đăng ký</strong></li>
</ol>
<p>Việc hủy sẽ có hiệu lực vào cuối chu kỳ thanh toán hiện tại. Bạn vẫn có thể sử dụng các tính năng Premium cho đến khi hết chu kỳ.</p>

<h3>Hoàn tiền</h3>
<ul>
  <li>Yêu cầu hoàn tiền được xử lý theo chính sách của Apple</li>
  <li>Để yêu cầu hoàn tiền, vui lòng liên hệ <a href="https://support.apple.com/">Apple Support</a> hoặc truy cập <a href="https://reportaproblem.apple.com/">reportaproblem.apple.com</a></li>
</ul>
```

---

## Nội dung cần thêm (Tiếng Anh)

Nếu có phiên bản tiếng Anh, thêm:

```html
<h2>Premium Subscription</h2>

<h3>Subscription Plans</h3>
<ul>
  <li><strong>Monthly:</strong> Auto-renews every month</li>
  <li><strong>Yearly:</strong> Auto-renews every year</li>
  <li><strong>Lifetime:</strong> One-time payment, use forever</li>
</ul>

<h3>Payment</h3>
<ul>
  <li>Payment is processed entirely through the Apple App Store</li>
  <li>Prices are displayed in your local currency</li>
  <li>We do not store your payment information</li>
</ul>

<h3>Auto-Renewal</h3>
<ul>
  <li>Subscription automatically renews unless cancelled at least 24 hours before the end of the current period</li>
  <li>Your Apple ID account will be charged for renewal within 24 hours prior to the end of the current period</li>
  <li>Renewal price equals the current subscription price</li>
</ul>

<h3>Free Trial</h3>
<ul>
  <li>Some plans may include a 7-day free trial period</li>
  <li>You can cancel anytime during the trial without being charged</li>
  <li>If not cancelled before the trial ends, the subscription will automatically convert to a paid plan</li>
</ul>

<h3>Managing and Cancelling Subscription</h3>
<p>To manage or cancel your subscription:</p>
<ol>
  <li>Open <strong>Settings</strong> on your iPhone/iPad</li>
  <li>Tap your name (Apple ID) at the top</li>
  <li>Select <strong>Subscriptions</strong></li>
  <li>Select "NTN Expense Tracker" and tap <strong>Cancel Subscription</strong></li>
</ol>
<p>Cancellation takes effect at the end of the current billing period. You can continue using Premium features until then.</p>

<h3>Refunds</h3>
<ul>
  <li>Refund requests are handled according to Apple's policies</li>
  <li>To request a refund, please contact <a href="https://support.apple.com/">Apple Support</a> or visit <a href="https://reportaproblem.apple.com/">reportaproblem.apple.com</a></li>
</ul>
```

---

## Checklist sau khi cập nhật

- [x] Thêm section "Đăng ký Premium" vào trang Privacy Policy
- [ ] Push code lên GitHub để cập nhật trang web
- [ ] Kiểm tra link hoạt động: https://nhant1164.github.io/expense-tracker-privacy/privacy-policy.html
- [ ] Đảm bảo trang load được trên mobile Safari
- [ ] Thông báo cho dev để submit lại app

---

## Thông tin bổ sung

### Tại sao cần cập nhật?
Apple yêu cầu apps có auto-renewable subscription phải:
1. Có Privacy Policy URL trong App Store Connect ✅ (đã có)
2. Hiển thị link Terms và Privacy trong app ✅ (đã sửa code)
3. Privacy Policy phải mô tả rõ về subscription terms

### Tài liệu tham khảo
- [Apple App Store Review Guidelines 3.1.2](https://developer.apple.com/app-store/review/guidelines/#subscriptions)
- [Apple's Standard EULA](https://www.apple.com/legal/internet-services/itunes/dev/stdeula/)
