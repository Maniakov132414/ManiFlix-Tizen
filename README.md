# ManiFlix for Samsung Tizen Smart TV

Ứng dụng Smart TV (`ManiFlixTV.ManiFlix` `v1.1.0`) dành cho Samsung Smart TV chạy **Tizen OS 4.0 – 8.0**, đóng gói chuẩn `.wgt` ký chứng chỉ bằng **Tizen Studio CLI** trên GitHub Actions.

## Tính năng chính
- **Siêu mượt 60fps trên TV**: Tối ưu GPU `translate3d`, `contain: layout paint`, cập nhật DOM cục bộ (`updateHeroInPlace`, nối thẻ trực tiếp khi tải thêm), loại bỏ hoàn toàn CSS blur/mask-image nặng, hỗ trợ bật/tắt **Chế độ Siêu Mượt TV**.
- **Điều khiển Remote Samsung đầy đủ**: Đăng ký phím Media (`MediaPlayPause`, `MediaPlay`, `MediaPause`, `MediaStop`, `MediaFastForward`, `MediaRewind`, `MediaTrackPrevious`, `MediaTrackNext`) và 4 phím Màu (`Red/Green/Yellow/Blue`), hỗ trợ phím **Return (`10009`)**, **Play/Pause (`10252`)**, **Exit (`10182`)** và **IME Done/Cancel (`65376`/`65385`)**.
- **Bàn phím ảo D-Pad & Tìm kiếm nhanh**: Tìm kiếm theo tên phim hoặc chủ đề bằng Remote TV mà không cần bàn phím ngoài.
- **Trình phát HLS TV**: Tích hợp sẵn `hls.min.js` tối ưu buffer (`24s`/`45s`), tự động cắt quảng cáo & bỏ qua mở đầu/kết thúc (TheIntroDB), chọn server/tập, chất lượng, tốc độ, tỉ lệ khung hình.
- **Giám sát Mạng & Thiết bị Samsung TV**: Hiển thị Model/Firmware TV (`webapis.productinfo` + `tizen.systeminfo`), đo Speedtest 4 luồng Cloudflare Edge và trạng thái máy chủ `phim.maniakov.bond`.

## Hướng dẫn cài đặt (Sideload `.wgt`)

### Cách 1: Dùng Apps2Samsung / TizenBrew Device Manager (Nhanh nhất)
1. Trên Samsung Smart TV, mở mục **Apps**.
2. Nhấn nhanh dãy số **`1 2 3 4 5`** trên remote để mở **Developer Mode**.
3. Bật **Developer mode -> ON**, nhập địa chỉ IP máy tính của bạn, nhấn **OK** và khởi động lại TV (giữ nút Nguồn 3 giây hoặc rút điện cắm lại).
4. Tải tệp `ManiFlix-Tizen.wgt` từ mục **Releases**.
5. Dùng **Apps2Samsung** (hoặc **Tizen Studio Device Manager** -> *Remote Device Manager* -> kết nối IP TV cổng `26101`) chọn **Install** tệp `ManiFlix-Tizen.wgt`.

### Cách 2: Cài qua Tizen Studio CLI
```bash
sdb connect <IP_CUA_TV>:26101
tizen install -n ManiFlix-Tizen.wgt -t <DEVICE_NAME>
```
