# study-area-map-vi
Study Area Map is a browser-based tool for mapping georeferenced research data. Import CSV, Excel, GPX, KML, KMZ or GeoJSON files — coordinates are detected automatically. Style points by color and shape, add a coordinate grid, north arrow and legend, then export as PNG or A4 PDF. © Thái Minh Quang

# 🗺️ Study Area Map — Bản đồ khu vực nghiên cứu

A lightweight, browser-based tool for mapping georeferenced research data. Import a spreadsheet or GIS file, and your sampling stations are plotted instantly on an interactive map — styled by color and shape, framed with a coordinate graticule, and ready to export as publication-quality figures.

Công cụ chạy trực tiếp trên trình duyệt giúp vẽ bản đồ khu vực nghiên cứu từ file dữ liệu có tọa độ. Không cần cài đặt, không cần tài khoản — chỉ cần mở file HTML và kéo thả dữ liệu vào.
Đối tượng sử dụng: Nội bộ

> **Author / Tác giả:** © Thái Minh Quang

<!-- Thêm ảnh chụp màn hình app tại đây / Add a screenshot here -->
<!-- ![Screenshot](docs/screenshot.png) -->

## ✨ Features / Tính năng

| Feature | Mô tả |
|---|---|
| 📂 Multi-format import | Nhập CSV, Excel (.xlsx/.xls), GPX, KML, KMZ, GeoJSON/JSON |
| 🔍 Auto coordinate detection | Tự nhận diện cột tọa độ, kể cả tiêu đề tiếng Việt ("Vĩ độ", "Kinh độ") và dấu phẩy thập phân |
| 🎨 Color by category | Tô màu điểm theo một cột phân nhóm, kèm chú giải |
| 🔷 Shape by category | Ký hiệu điểm (tròn, vuông, tam giác, thoi, sao, chữ thập…) theo một cột nhóm **độc lập với màu** — bản đồ 2 biến cho bài báo khoa học |
| 🏷️ Point labels | Bật/tắt hiển thị tên điểm ngay trên bản đồ |
| 🧭 Map furniture | Khung bản đồ (neatline) kèm lưới tọa độ, mũi tên hướng Bắc, thước tỷ lệ, chú giải — tất cả đều xuất ra ảnh |
| 📐 3 coordinate formats | Độ phút giây (109°21′43″Đ) · Độ, phút lẻ (109°21.72′Đ) · Độ, 5 số lẻ (109.36200°Đ) |
| 🔎 Search & filter | Tìm kiếm mọi cột, ẩn/hiện nhóm bằng cách nhấp vào chú giải |
| 📋 Linked data table | Bảng dữ liệu liên kết — nhấp một dòng để bay đến điểm tương ứng |
| ⛶ Box zoom | Phóng to theo vùng chọn bằng cách kéo chuột (hoặc giữ Shift + kéo) |
| 🖼️ Export | Xuất bản đồ ra **PNG** và **PDF khổ A4**; xuất bảng dữ liệu đã lọc ra **CSV** |

## 🚀 Getting started / Cách sử dụng

**No installation required.** Just download and open the HTML file in a modern browser (Chrome, Edge, Firefox). An internet connection is needed only to load the basemap tiles.

1. Tải file `index.html` về máy và mở bằng trình duyệt
2. Nhập mật khẩu: "camonquang"
3. Kéo thả (hoặc chọn) file dữ liệu vào **mục 1** ở thanh bên trái
4. Kiểm tra cột tọa độ ở **mục 2** — app thường tự nhận diện đúng
5. Tùy chỉnh hiển thị ở **mục 3**: màu, ký hiệu, tên điểm, khung tọa độ
6. Xuất bản đồ hoặc bảng dữ liệu ở **mục 5**

## 📄 Data format / Định dạng dữ liệu

Với file bảng tính, dòng đầu tiên là tiêu đề cột và cần có hai cột tọa độ (WGS 84, độ thập phân). Ví dụ / Example:

```csv
Tên điểm,Vĩ độ,Kinh độ,Loại mẫu,Ngày thu thập
Trạm HN-01,21.0285,105.8542,Nước mặt,2026-03-02
Trạm ĐN-01,16.0544,108.2022,Trầm tích,2026-03-10
```

Accepted coordinate column names include: `lat`, `latitude`, `Vĩ độ`, `y` / `lon`, `lng`, `longitude`, `Kinh độ`, `x`. If auto-detection fails, select the columns manually in section 2.

For GIS files (GPX, KML, KMZ, GeoJSON), point features are imported with all their attributes; lines and polygons are skipped.

## 🛠️ Built with / Công nghệ

Single self-contained HTML file — HTML, CSS, and vanilla JavaScript. Libraries loaded from CDN:

[Leaflet](https://leafletjs.com/) (interactive map) · [PapaParse](https://www.papaparse.com/) (CSV) · [SheetJS](https://sheetjs.com/) (Excel) · [JSZip](https://stuk.github.io/jszip/) (KMZ) · [html2canvas](https://html2canvas.hertzen.com/) (map capture) · [jsPDF](https://github.com/parallax/jsPDF) (PDF export) · Basemap © [OpenStreetMap](https://www.openstreetmap.org/copyright) contributors

## ⚠️ Notes / Lưu ý

- Tọa độ cần ở hệ **WGS 84** (kinh/vĩ độ thập phân hoặc theo file GIS chuẩn); app chưa hỗ trợ hệ tọa độ VN-2000/UTM
- Muốn ảnh xuất có độ phân giải cao hơn: phóng to cửa sổ trình duyệt và thu gọn bảng dữ liệu trước khi xuất
- Dữ liệu được xử lý hoàn toàn trên máy của bạn — không tải lên máy chủ nào

## 📜 License & credit

© Thái Minh Quang. Basemap data © OpenStreetMap contributors.
