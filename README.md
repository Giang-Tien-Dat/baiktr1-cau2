# Kiểm tra số dư Token ERC20 trên Ronin Saigon

Dự án này giúp kiểm tra số dư của một token ERC20 trên mạng Ronin Saigon bằng cách tương tác trực tiếp với blockchain thông qua thư viện ethers.js.

## Yêu cầu hệ thống

- Node.js (phiên bản 14 trở lên)
- npm (Node Package Manager)

## Cài đặt

1. Cài đặt các dependencies:
```bash
npm install
```

## Cấu hình

1. Mở file `index.ts`
2. Thay đổi các giá trị sau:
   - `walletAddress`: Địa chỉ ví bạn muốn kiểm tra số dư
   - `tokenAddress`: Địa chỉ của token ERC20 bạn muốn kiểm tra

## Chạy chương trình

```bash
npm start
```

## Giải thích mã nguồn

### config.ts
- `RONIN_SAIGON_RPC`: URL của node RPC để kết nối với mạng Ronin Saigon
- `ERC20_ABI`: Định nghĩa interface của token ERC20 (chỉ bao gồm hàm balanceOf)

### index.ts
- `checkERC20Balance`: Hàm chính để kiểm tra số dư token
  - Tạo kết nối với blockchain thông qua RPC
  - Tạo interface để tương tác với smart contract
  - Gọi hàm balanceOf để lấy số dư
  - Chuyển đổi số dư sang định dạng dễ đọc

## Lưu ý

- Đảm bảo bạn có kết nối internet ổn định
- Địa chỉ ví và token phải là địa chỉ hợp lệ trên mạng Ronin Saigon
- Số dư được hiển thị với 18 số thập phân (có thể điều chỉnh tùy theo token)