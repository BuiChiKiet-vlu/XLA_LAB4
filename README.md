# README

## Mục tiêu
Chương trình này gồm 3 bài tập nhỏ nhằm mục tiêu:
- Làm quen với thao tác **chọn vùng đối tượng** trong ảnh.
- Áp dụng các kỹ thuật xử lý ảnh như **tịnh tiến**, **xoay**, **ngưỡng hóa**, **mapping**, và **morphological closing**.
- Sử dụng thư viện xử lý ảnh nâng cao: `cv2` (OpenCV), `skimage`, `numpy`, `matplotlib`, `PIL`.

---

## Cấu trúc
```
├── exercise/
├── THLAB4.ipynb
└── README_Dalat_Objects.md
```

---

## Các bài toán cụ thể

### 🖼 Bài 1: LangBiang - Tịnh tiến + Otsu Threshold
- **Tác vụ**: Cắt vùng LangBiang từ ảnh `da_lat.jpg`, tịnh tiến sang phải 100px.
- **Ngưỡng hóa bằng Otsu** với hệ số điều chỉnh 0.3 (giảm độ sáng)
- **Công thức** (Otsu threshold tự động): chọn ngưỡng `T` sao cho:
  ```
  σ²_B(T) = w₀(T)w₁(T)[μ₀(T) - μ₁(T)]² là lớn nhất
  ```
- **Lưu kết quả**: `lang_biang.jpg`

### Bài 2: Hồ Xuân Hương - Xoay + Adaptive Threshold
- **Tác vụ**: Cắt vùng hồ, xoay 45 độ quanh tâm vùng chọn
- **Ngưỡng hóa thích nghi** (Adaptive Gaussian) với tham số C = 60
- **Công thức**:
  ```
  T(x,y) = mean_{block}(x,y) - C
  ```
- **Lưu kết quả**: `ho_xuan_huong.jpg`

### Bài 3: Quảng Trường Lâm Viên - Coordinate Mapping + Morphological Closing
- **Tác vụ**: Phóng to vùng chọn bằng phép nội suy
- Áp dụng **Binary Closing** để làm mịn chi tiết:
  ```
  Closing = Dilation(Erosion(image))
  ```
- Dùng hàm `skimage.morphology.binary_closing`
- **Lưu kết quả**: `quan_truong_lam_vien.jpg`

---

## Thư viện sử dụng
- `cv2`
- `numpy`
- `matplotlib`
- `PIL`
- `skimage`
- `scipy`
---

## Cách chạy

---
## Sinh viên thực hiện
Bùi Chí Kiệt - 2374802010255

## Giảng viên hướng dẫn
TS. ĐỖ HỮU QUÂN

## Tài liệu tham khảo
Tài liệu thực hành lab4
