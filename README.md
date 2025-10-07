# MyApplication – Feature-Based Architecture

## 📂 Cấu trúc

MyApplication/
├── app/ # Module chính, launcher
├── core/
│ └── core-ui/ # Shared resources: themes, colors, dimens, drawables
├── features/
│ ├── auth/ # Feature Auth
│ ├── ticket/ # Feature Ticket
│ └── ... # Feature khác

css
Sao chép mã

## 🎨 Quy tắc resources

- **Core-ui**: chung cho tất cả feature (themes, colors, dimens, drawable)  
- **Feature riêng**: layout, drawable, strings  

## ⚙ Dependencies

**app/build.gradle.kts**

implementation(project(":core:core-ui"))
implementation(project(":features:auth"))
implementation(project(":features:ticket"))
Feature build.gradle.kts

kotlin
Sao chép mã
implementation(project(":core:core-ui"))
➕ Thêm feature mới
Tạo folder features/myfeature/

Tạo module Android Library với namespace riêng

Thêm vào settings.gradle.kts:

kotlin
Sao chép mã
include(":features:myfeature")
Thêm dependency vào app nếu cần:

Sao chép mã
implementation(project(":features:myfeature"))
Đặt resources riêng trong features/myfeature/src/main/res/           
