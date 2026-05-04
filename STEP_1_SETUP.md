# 🚀 STEP 1 — SETUP PROJECT + FIREBASE

## 🎯 Mục tiêu
- Tạo project Flutter
- Kết nối Firebase (Firestore + FCM)
- Khởi tạo Firebase trong main.dart
- Hiển thị "Firebase OK"

---

## ✅ Lệnh chạy để setup

### 1. Clone repo
```bash
git clone https://github.com/thiepmoi29/mygroup.git
cd mygroup
```

### 2. Checkout branch Step 1
```bash
git checkout feature/step-1-setup
```

### 3. Cài dependencies
```bash
flutter pub get
```

### 4. Configure Firebase
```bash
# Cài Firebase CLI (nếu chưa có)
curl -sL https://firebase.tools | bash

# Login Firebase
firebase login

# Configure Firebase cho project
flutterfire configure
```

**Lưu ý khi chạy `flutterfire configure`:**
- Chọn hoặc tạo project Firebase mới
- Chọn Android + iOS platforms
- Lệnh sẽ tự tạo:
  - `google-services.json` (Android)
  - `GoogleService-Info.plist` (iOS)
  - `lib/firebase_options.dart` (Config file)

### 5. Chạy app
```bash
# Android
flutter run

# iOS
flutter run -d ios
```

---

## ▶️ Kết quả mong đợi

✅ App khởi động thành công  
✅ Hiển thị "✅ Firebase OK" ở giữa màn hình  
✅ Không có error Firebase  

---

## 📦 Files được tạo/sửa

| File | Mô tả |
|------|-------|
| `pubspec.yaml` | Dependencies (Firebase, SharedPreferences, etc.) |
| `lib/main.dart` | App entry point + Firebase initialization |
| `.gitignore` | Ignore Flutter/Firebase files |
| `README.md` | Project documentation |
| `STEP_1_SETUP.md` | This file |

---

## 🔧 Troubleshooting

### Error: "CocoaPods not installed"
```bash
sudo gem install cocoapods
cd ios && pod install && cd ..
```

### Error: "Could not locate google-services.json"
- Đảm bảo `flutterfire configure` đã chạy hoàn tất
- Firebase CLI phải login trước: `firebase login`

### Error: "FirebaseCore not found"
```bash
flutter clean
flutter pub get
flutter run
```

---

## 📋 Checklist hoàn tất Step 1

- ✅ Clone repo từ GitHub
- ✅ Checkout `feature/step-1-setup`
- ✅ Chạy `flutter pub get`
- ✅ Chạy `flutterfire configure`
- ✅ App chạy và hiển thị "Firebase OK"
- ✅ Không có error

---

## 👉 Next Step

Sau khi xác nhận **OK STEP 1**, tiếp theo là:

**STEP 2 — PHONE FORMATTER**
- Tạo utility để chuẩn hóa số điện thoại
- Xóa ký tự đặc biệt
- Chuyển +84/84 → 0

---

## 📝 Git Commands

```bash
# Tạo branch (nếu chưa tạo)
git checkout -b feature/step-1-setup

# Push lên remote
git push origin feature/step-1-setup

# Merge về main (sau khi xác nhận)
git checkout main
git pull origin main
git merge feature/step-1-setup
git push origin main
```

---

**Branch**: `feature/step-1-setup`  
**Date**: 2026-05-04  
**Status**: ✅ Ready to test
