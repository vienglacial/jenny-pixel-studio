# Hướng dẫn khi máy báo virus / chặn cài đặt

App **AI Image – Golden Pixel Animation** an toàn. Phần mềm diệt virus báo nhầm (false positive) vì app chưa mua chữ ký số — gần như mọi app nhỏ chưa ký số đều bị vậy. Làm theo hướng dẫn dưới để cho phép app chạy.

---

## 1. Windows Defender (mặc định trên Windows)

**Khi TẢI VỀ bị chặn / bị xóa file:**
- Bấm vào dòng cảnh báo file tải về trên trình duyệt → chọn **"Keep" / "Giữ lại"**.

**Khi MỞ FILE hiện bảng xanh "Windows protected your PC":**
- Bấm **"More info"** (Thông tin thêm) → bấm **"Run anyway"** (Vẫn chạy).

**Loại trừ hẳn (làm 1 lần, khỏi bị xóa lại):**
1. Mở **Windows Security** (gõ ở thanh tìm kiếm).
2. Vào **Virus & threat protection**.
3. Mục **Virus & threat protection settings** → bấm **Manage settings**.
4. Kéo xuống **Exclusions** → bấm **Add or remove exclusions**.
5. Bấm **Add an exclusion** → chọn:
   - **Folder** → thư mục cài app:
     `C:\Users\<tên user>\AppData\Local\Programs\AI Image - Golden Pixel Animation`
   - **hoặc File** → file `.exe` cài đặt.
6. Xong. Defender sẽ không báo/xóa app nữa.

---

## 2. Kaspersky (xóa thẳng file — cần khôi phục trước)

**Bước 1 — Khôi phục file đã bị xóa:**
1. Mở **Kaspersky**.
2. Vào **More Tools / Công cụ khác** (hoặc dấu **…** / mục **Security**).
3. Mở **Quarantine** (Cách ly / Lưu trữ).
4. Tìm file app → bấm **Restore** (Khôi phục).

**Bước 2 — Thêm vào loại trừ (để không xóa lại):**
1. Mở Kaspersky → bấm **⚙️ Settings** (góc dưới bên trái).
2. Vào **Security settings → Exclusions and actions on object detection**.
3. Bấm **Manage exclusions** → **Add**.
4. Bấm **Browse** → chọn thư mục cài app **và** file cài đặt `AI-Image-Studio-Setup-….exe`.
5. Mục **Protection components** để **All**.
6. Bấm **Add / Save**.

**Bước 3 — Cài lại app bình thường.**

> Mẹo: nếu bị chặn ngay lúc tải, chuột phải icon Kaspersky ở khay → **Pause protection** → 1 giờ, tải + cài xong rồi bật lại và thêm loại trừ như trên.

---

## 3. Diệt virus khác (Avast, AVG, Bkav, Bitdefender…)

Tìm mục **Exclusions / Loại trừ / Trusted / Tin cậy** trong phần cài đặt → thêm file `.exe` hoặc thư mục cài app vào danh sách loại trừ. Cách làm tương tự, chỉ khác tên menu.

---

## 4. Giải pháp dứt điểm (cho admin)

Whitelist từng máy chỉ là chữa cháy. Muốn hết báo nhầm trên mọi máy:

- **Gửi báo cáo false positive:**
  - Kaspersky: https://opentip.kaspersky.com/
  - Microsoft Defender: https://www.microsoft.com/en-us/wdsi/filesubmission
- **Mua chữ ký số (code signing certificate):** hết bị báo trên mọi diệt virus (tốn phí/năm).
