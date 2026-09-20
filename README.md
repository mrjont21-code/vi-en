# RTranslator Web Mini

Phiên bản tối giản của [RTranslator](https://github.com/niedev/RTranslator) chạy trên trình duyệt web, hỗ trợ dịch thuật giọng nói thời gian thực giữa tiếng Anh và tiếng Việt.

## Tính năng

- **Giao diện chia đôi màn hình**: Bên trái hiển thị luồng Anh→Việt, bên phải hiển thị luồng Việt→Anh
- **Nhận dạng giọng nói thời gian thực**: Sử dụng Web Speech API cho cả tiếng Anh và tiếng Việt
- **Dịch thuật tự động**: Sử dụng MyMemory Translation API
- **Phát âm bản dịch**: Tự động phát bản dịch ra loa với ngôn ngữ đích tương ứng
- **3 nút điều khiển**:
  - Nút **Play/Stop** ở giữa: Bắt đầu/dừng phiên dịch liên tục
  - Nút **English Panel**: Bật/tắt khung hiển thị và nhận dạng tiếng Anh
  - Nút **Vietnamese Panel**: Bật/tắt khung hiển thị và nhận dạng tiếng Việt
- **Hỗ trợ gõ tay**: Có thể gõ trực tiếp vào ô nguồn và nhấn Enter để dịch
- **Activity log**: Ghi lại lịch sử các hoạt động dịch thuật

## Công nghệ sử dụng

- **Web Speech API (SpeechRecognition)**: Nhận dạng giọng nói
- **Web Speech API (SpeechSynthesis)**: Tổng hợp giọng nói (text-to-speech)
- **MyMemory Translation API**: Dịch thuật miễn phí, không cần API key
- **Tailwind CSS**: Styling giao diện
- **Vanilla JavaScript**: Không phụ thuộc framework

## Yêu cầu

- **Trình duyệt**: Chrome hoặc Edge (Web Speech API chỉ được hỗ trợ đầy đủ trên các trình duyệt này)
- **Kết nối HTTPS**: Nhận dạng giọng nói chỉ hoạt động trên kết nối HTTPS hoặc localhost
- **Quyền Microphone**: Cần cấp quyền microphone khi trình duyệt hỏi

## Triển khai lên GitHub Pages

### Cách 1: Upload file thủ công

1. Tạo một repository mới trên GitHub
2. Upload file `index.html` vào repository
3. Vào **Settings** → **Pages**
4. Trong phần **Build and deployment**, chọn:
   - **Source**: Deploy from a branch
   - **Branch**: `main` / `root`
5. Nhấn **Save**
6. Chờ vài phút, trang web sẽ được truy cập tại: `https://<username>.github.io/<repo-name>/`

### Cách 2: Sử dụng git command line

```bash
# Tạo repo mới trên GitHub trước, sau đó:
git init
git add index.html
git commit -m "Initial commit: RTranslator Web Mini"
git branch -M main
git remote add origin https://github.com/<username>/<repo-name>.git
git push -u origin main
```

Sau đó làm theo các bước cấu hình GitHub Pages như Cách 1.

## Sử dụng

1. Mở trang web trên trình duyệt Chrome/Edge
2. Nhấn nút **Start** ở giữa
3. Cấp quyền microphone khi được hỏi
4. Nói tiếng Anh → hệ thống sẽ dịch và phát ra tiếng Việt
5. Nói tiếng Việt → hệ thống sẽ dịch và phát ra tiếng Anh
6. Nhấn **Stop** để kết thúc phiên dịch

## Lưu ý

- Phiên bản web này sử dụng dịch thuật online (MyMemory API), không chạy offline như RTranslator gốc (sử dụng NLLB)
- Chất lượng nhận dạng giọng nói tiếng Việt phụ thuộc vào trình duyệt và hệ điều hành
- Để có kết quả tốt nhất, nói rõ ràng, không quá nhanh

## License

MIT License - tự do sử dụng, sửa đổi, phân phối
