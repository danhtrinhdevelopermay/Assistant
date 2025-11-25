# GitHub Actions Workflows

## Build APK Workflow

Workflow này tự động build APK khi có code mới được push hoặc khi được trigger thủ công.

### Cấu hình

Trước khi chạy workflow, bạn cần thêm secret `GEMINI_API_KEY` vào repository:

1. Vào **Settings** → **Secrets and variables** → **Actions**
2. Click **New repository secret**
3. Tên: `GEMINI_API_KEY`
4. Giá trị: API key của bạn từ [Google AI Studio](https://aistudio.google.com/app/apikey)

### Trigger Workflow

#### Tự động:
- Push code lên branch `main`, `master`, hoặc `develop`
- Tạo Pull Request vào `main` hoặc `master`

#### Thủ công:
1. Vào tab **Actions** trên GitHub
2. Chọn workflow **Build Android APK**
3. Click **Run workflow**
4. Chọn build type: `debug` hoặc `release`

### Download APK

Sau khi workflow chạy xong:

1. Vào tab **Actions**
2. Click vào workflow run mới nhất
3. Scroll xuống phần **Artifacts**
4. Download file APK

### Release

Khi push code lên branch `main` hoặc `master`, workflow sẽ tự động tạo release mới với APK đính kèm.
