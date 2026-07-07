# iOS Game Booster - WebClip System

## Cấu trúc thư mục

```
ios_booster/
├── index.html                       # WebClip chính (bảng điều khiển)
├── profiles/
│   ├── gaming-dns.mobileconfig      # DNS Gaming profile
│   └── block-telemetry.mobileconfig # Chặn telemetry profile
└── shortcuts/
    └── GamingModeON.plist           # Mẫu Shortcuts (import bằng Apple Shortcuts)
```

## Cách triển khai

### 1. Host WebClip
Upload `index.html` lên hosting (GitHub Pages, Vercel, Netlify, hoặc hosting thường).

### 2. Host profiles
Upload 2 file `.mobileconfig` lên hosting, sửa URL trong `index.html`:
- `https://tendomaincua-ban.com/gaming-dns.mobileconfig`
- `https://tendomaincua-ban.com/block-telemetry.mobileconfig`

### 3. Tạo Shortcuts
- Mở Apple Shortcuts trên iPhone
- Import file `GamingModeON.plist`
- Chỉnh sửa các action cho phù hợp
- Đặt tên chính xác là `GamingModeON` và `GamingModeOFF`

### 4. Hướng dẫn khách hàng
1. Cài 2 Shortcuts (GamingModeON / GamingModeOFF)
2. Mở link WebClip bằng Safari
3. Bấm nút Chia sẻ → "Thêm vào màn hình chính"
4. Mở App từ màn hình chính → gạt công tắc

## Lưu ý
- Các thông số (RAM, nhiệt, ping) là giả, chỉ hiển thị UI
- Shortcuts cần được cài thủ công trên từng máy
- Profile .mobileconfig yêu cầu người dùng vào Cài đặt xác nhận
