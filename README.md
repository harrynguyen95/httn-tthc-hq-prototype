# HTTN TTHC – Prototype

Prototype UI cho **Hệ thống Tiếp nhận Thủ tục Hành chính** – Cục Hải quan.

## Nội dung gói

| File | Mục đích |
|---|---|
| `index.html` | Toàn bộ prototype SPA (HTML + CSS + JS) trong 1 file |
| `package.json` | Metadata cho Vercel nhận diện project |
| `vercel.json` | Config deploy: bảo mật headers, cache, rewrites |

## Cách 1 – Drag & Drop vercel.com (nhanh nhất, 30 giây)

1. Truy cập https://vercel.com/new
2. Kéo thả **cả thư mục này** (3 file) vào trang
3. Vercel tự nhận là static site → click **Deploy**
4. Sau ~30 giây có URL: `https://httn-tthc-prototype-xxx.vercel.app`

## Cách 2 – Vercel CLI

```bash
npm install -g vercel
cd /path/to/this/folder
vercel login         # lần đầu
vercel --prod        # deploy production
```

## Cách 3 – GitHub Integration

1. Tạo repo GitHub mới
2. Upload 3 file lên repo
3. Vào vercel.com → **New Project** → **Import Git Repository**
4. Chọn repo → Deploy
5. Mỗi lần push mới → auto-deploy

## Các trang trong prototype

- **Dashboard** – KPI, biểu đồ, cảnh báo
- **Danh mục thủ tục** – 18 thủ tục phân 5 nhóm
- **Định nghĩa chứng từ** – Schema Builder động, JSON preview realtime
- **Hồ sơ tiếp nhận** – Tra cứu, timeline xử lý
- **Khai báo mới** – Form render động từ schema
- **API Log** – Giám sát realtime

## Bảo mật

File `vercel.json` đã bật:
- `"public": false` – yêu cầu Vercel account để xem (không hoàn toàn public)
- Security headers: X-Frame-Options, X-XSS-Protection, Referrer-Policy...

**Nếu muốn public hoàn toàn**: đổi `"public": false` → `"public": true`.

**Nếu cần password bảo vệ**: Vào Vercel Dashboard → Settings → Deployment Protection → Password.

## Lưu ý

⚠️ Đây là **prototype UI-only**, không có backend thật.
⚠️ KHÔNG dùng cho production, KHÔNG đưa dữ liệu thật vào.
⚠️ Mục đích: demo scope, workshop với nghiệp vụ, kèm HSMT.
