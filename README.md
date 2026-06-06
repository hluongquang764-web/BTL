# BÀI TẬP LỚN - PHÁT TRIỂN ỨNG DỤNG TRÊN THIẾT BỊ DI ĐỘNG
**Môn học:** TEE0419  
**Họ tên:** Lương Quang Hà  
**MSSV:** K225480106010  
**Lớp:** 58KTPM (K58KTP.K01)

## MỤC LỤC
1. [Phần 1 - MIT App Inventor](#phần-1---mit-app-inventor)
2. [Phần 2 - Android Studio](#phần-2---android-studio)
3. [Kết quả chạy thử](#kết-quả-chạy-thử)

---

# PHẦN 1 - MIT APP INVENTOR

## 1.1 Thanh công cụ MIT App Inventor

MIT App Inventor có giao diện chia thành 4 vùng chính:

| Vùng | Tên | Chức năng |
|------|-----|-----------|
| Trái | Palette | Danh sách các component (Button, Label, TextBox, WebViewer...) |
| Giữa | Viewer | Màn hình preview dạng điện thoại, kéo thả component vào đây |
| Phải | Properties | Bảng thuộc tính của component đang được chọn |
| Dưới | Components | Danh sách tất cả component đã thêm vào screen |
| Trên | Thanh menu | Screens, Connect, Build, Settings |

<img width="1920" height="1077" alt="image" src="https://github.com/user-attachments/assets/9325cd4e-7cd8-4ecc-b849-05dc7a2a3094" />


---

## 1.2 Kéo thả và thay đổi thuộc tính

**Cách kéo thả:**
1. Chọn component trong Palette bên trái (ví dụ: Button)
2. Giữ chuột trái, kéo component sang vùng Viewer giữa
3. Thả ra vị trí mong muốn trên màn hình điện thoại ảo
4. Component xuất hiện trong Viewer và được thêm vào danh sách Components

**Cách thay đổi thuộc tính:**
1. Click vào component cần chỉnh (trên Viewer hoặc Components)
2. Bảng Properties bên phải tự động hiện thuộc tính của component đó
3. Click vào giá trị cần đổi → nhập giá trị mới
4. Thay đổi hiển thị ngay trên Viewer (real-time preview)

**Tại sao phải thay đổi thuộc tính:**
- **Text**: thay đổi nội dung hiển thị
- **Width/Height**: chỉnh kích thước (Fill parent / Wrap content / px cụ thể)
- **BackgroundColor**: đổi màu nền
- **FontSize, FontBold**: định dạng chữ
- **Hint** (TextBox): chữ mờ trong hộp nhập
- **HomeUrl** (WebViewer): URL trang web sẽ tải
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/6dea82b9-f679-4367-af39-a172d55cd1d6" />


---

## 1.3 Blocks — Lập trình bằng kéo thả

**Bản chất của Block:**  
Mỗi block là một lệnh lập trình được trực quan hóa bằng hình ảnh. Thay vì viết code bằng chữ, người dùng kéo các block ra và snap (gắn) chúng vào nhau. Các block gắn vào nhau sẽ thực thi theo thứ tự từ trên xuống dưới.

**Cách sử dụng Blocks:**
1. Nhấn nút **Blocks** góc trên phải để chuyển sang màn hình lập trình
2. Bên trái hiện danh sách tất cả component và nhóm lệnh (Logic, Math, Text, Control...)
3. Click vào tên component → chọn block cần dùng
4. Kéo block ra vùng trắng giữa → snap vào các block khác

**Ưu điểm so với viết code:**
- Không cần nhớ cú pháp (syntax) — không bị lỗi syntax
- Trực quan, dễ hiểu logic
- Block chỉ snap đúng kiểu — hạn chế lỗi ngữ nghĩa
- Phù hợp người mới bắt đầu lập trình

**Nhược điểm:**
- Khó làm app phức tạp, nhiều chức năng
- Không linh hoạt bằng code thực
- Khó tái sử dụng code (copy block phức tạp)
- Hiệu năng thấp hơn app native Android/iOS

**Backpack (sao chép block giữa các Screen):**
- Biểu tượng ba lô góc trên phải màn hình Blocks
- Kéo block vào Backpack để lưu tạm
- Chuyển sang Screen khác → kéo block từ Backpack ra để dùng lại
- Tương đương Copy-Paste nhưng hoạt động qua các Screen khác nhau

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/dfe40386-577b-4714-bd51-5da70b1ad887" />


---

## 1.4 Mô tả 3 Screen đã tạo

### Screen 1 — Giới thiệu

**Giao diện (Designer):**
- Label: Họ tên — "Lương Quang Hà" (FontSize 18, Bold, Center)
- Label: MSSV — "K225480106010" (FontSize 16, Center)
- Label: Lớp — "58KTPM" (FontSize 16, Center)
- Button: "Giải toán" (Width Fill parent, BackgroundColor Green)
- Button: "Xem trang web" (Width Fill parent, BackgroundColor Blue)

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/759e57f5-0073-4317-8e58-5efdacccdee2" />

**Blocks:**
```
when Button1.Click
  open another screen screenName: "Screen2"

when Button2.Click
  open another screen screenName: "Screen3"
```

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/e5f78de9-e125-4246-9b8a-9ed74d9a3ff3" />


---

### Screen 2 — Giải phương trình bậc 2

**Giao diện (Designer):**
- Label tiêu đề: "Giải phương trình bậc 2: ax² + bx + c = 0"
- TextBox3: Hint "Nhập a", NumbersOnly = true
- TextBox4: Hint "Nhập b", NumbersOnly = true
- TextBox5: Hint "Nhập c", NumbersOnly = true
- Button1: "Giải" (Width Fill parent)
- Label1: hiện kết quả (để trống ban đầu)

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/150b1704-7041-40e0-98ef-48dcbaaf4acc" />

**Blocks — Logic giải phương trình:**
```
initialize global a to 0
initialize global b to 0
initialize global c to 0
initialize global delta to 0

when Button1.Click
  set global a to TextBox3.Text
  set global b to TextBox4.Text
  set global c to TextBox5.Text
  set global delta to (b×b) - (4×a×c)

  if global delta < 0
    then  set Label1.Text to "Vô nghiệm"
  else if global delta = 0
    then  set Label1.Text to join ["Nghiệm kép: x = "] [(-b)/(2a)]
  else
    set Label1.Text to join ["x1 = "] [x1] ["  x2 = "] [x2]
```

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/113a36b0-0cc9-4ac7-a779-3fcb2982f360" />


---

### Screen 3 — WebView

**Giao diện (Designer):**
- WebViewer: Width = Fill parent, Height = Fill parent
- HomeUrl: `https://www.apple.com/vn/shop/buy-iphone`

*(Screen3 không có Blocks vì WebViewer tự động tải trang web khi mở Screen)*

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/c765e005-7d61-4920-8d37-c096f39212e2" />

## KẾT QUẢ CHẠY THỬ
MIT App Inventor
<img width="1290" height="2796" alt="image" src="https://github.com/user-attachments/assets/d12ddcb1-bd3d-42f2-8306-f937fc4c8cd1" />
<img width="1290" height="2796" alt="image" src="https://github.com/user-attachments/assets/ee00f3d9-7cf0-4467-a807-6dca7e4a67fb" />
<img width="1290" height="2796" alt="image" src="https://github.com/user-attachments/assets/8e8e8b6b-96e1-4aae-b1fc-ab834d3af164" />

---

# PHẦN 2 - ANDROID STUDIO

## 2.1 AndroidManifest.xml

**AndroidManifest.xml là gì:**  
File cấu hình trung tâm của mọi ứng dụng Android. Nó khai báo mọi thứ Android cần biết trước khi chạy app: tên app, icon, danh sách Activity, quyền truy cập, phiên bản tối thiểu...

**Các thành phần chính:**

| Thẻ XML | Ý nghĩa |
|---------|---------|
| `<manifest>` | Thẻ gốc, khai báo package name (tên duy nhất của app) |
| `<uses-permission>` | Xin quyền từ hệ điều hành (INTERNET, CAMERA, LOCATION...) |
| `<application>` | Thông tin chung: icon, label, theme |
| `<activity>` | Khai báo từng Activity có trong app |
| `<intent-filter>` | Xác định Activity nào là màn hình khởi động đầu tiên |

**File AndroidManifest.xml của dự án:**

```xml
<?xml version="1.0" encoding="utf-8"?>
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools">

    <uses-permission android:name="android.permission.INTERNET"/>

    <application
        android:allowBackup="true"
        android:icon="@mipmap/ic_launcher"
        android:label="@string/app_name"
        android:theme="@style/Theme.Luongquangha">
        <activity android:name=".WebViewActivity" android:exported="false" />
        <activity android:name=".GiaiToanActivity" android:exported="false" />
        <activity android:name=".MainActivity" android:exported="true">
            <intent-filter>
                <action android:name="android.intent.action.MAIN" />
                <category android:name="android.intent.category.LAUNCHER" />
            </intent-filter>
        </activity>
    </application>

</manifest>
```

<!--
  CHÈN ẢNH: Chụp file AndroidManifest.xml đang mở trong Android Studio
  Tên file: images/androidmanifest.png
-->
![AndroidManifest.xml](images/androidmanifest.png)

---

## 2.2 Vòng đời Activity (Activity Lifecycle)

**Vòng đời là gì:**  
Mỗi Activity Android trải qua các trạng thái từ khi tạo ra đến khi bị hủy. Hệ điều hành gọi các phương thức tương ứng khi Activity đổi trạng thái.

**Sơ đồ vòng đời:**
```
onCreate() → onStart() → onResume() → [ĐANG CHẠY]
                                            |
                          người dùng rời app
                                            |
                       onPause() → onStop() → onDestroy()
```

**Tại sao phải có onCreate():**
- `onCreate()` là phương thức chạy đầu tiên khi Activity được tạo
- Đây là nơi để: đặt layout (`setContentView`), tìm các View (`findViewById`), gắn sự kiện (`setOnClickListener`), khởi tạo dữ liệu ban đầu
- Nếu không có `onCreate()` → app không biết hiển thị gì, không biết lấy dữ liệu từ đâu

---

## 2.3 XML Layout

**Cấu trúc file layout XML:**
- Mỗi file `.xml` trong `res/layout/` mô tả giao diện của 1 Activity
- Thẻ gốc là ViewGroup (LinearLayout, ConstraintLayout...) — chứa các View con bên trong
- Mỗi View/ViewGroup có thể có thuộc tính: `id`, `layout_width`, `layout_height`, `text`, `hint`...

**ViewGroup phổ biến:**

| ViewGroup | Sắp xếp con |
|-----------|-------------|
| LinearLayout | Xếp chồng dọc (vertical) hoặc ngang (horizontal) |
| ConstraintLayout | Neo vị trí bằng ràng buộc (constraint) |
| RelativeLayout | Đặt vị trí tương đối với nhau hoặc với parent |
| FrameLayout | Xếp chồng lên nhau (layered) |

**Thuộc tính quan trọng:**
- `android:id="@+id/tenId"` — định danh để Java tìm thấy View này
- `android:layout_width` / `android:layout_height`: `match_parent` (đầy ra), `wrap_content` (vừa đủ)
- `android:text` — nội dung chữ
- `android:hint` — chữ mờ trong EditText
- `android:orientation` — hướng sắp xếp của LinearLayout

**Tham chiếu trong Java bằng `findViewById`:**
```java
// Trong XML đã khai báo: android:id="@+id/btnGiai"
// Trong Java tìm lại bằng:
Button btnGiai = findViewById(R.id.btnGiai);
```

**LOCATION (vị trí):** Dùng LinearLayout vertical giúp các View xếp chồng dọc từ trên xuống, phù hợp giao diện nhập liệu đơn giản.

**LANGUAGE:** Dự án sử dụng Java (không phải Kotlin). Java là ngôn ngữ truyền thống, đủ tài liệu tham khảo, cú pháp rõ ràng.

**THEME:** App dùng theme mặc định `Theme.Luongquangha` kế thừa `Theme.MaterialComponents` — hỗ trợ Material Design 3, Button và EditText có style hiện đại.

<!--
  CHÈN ẢNH: Chụp file activity_main.xml đang mở (xem cả XML lẫn Preview bên phải)
  Tên file: images/layout_main.png
-->
![Layout activity_main.xml](images/layout_main.png)

---

## 2.4 Xử lý sự kiện (Event Handling)

**2 cách gắn sự kiện cho Button trong Android:**

**Cách 1 — setOnClickListener trong Java (dùng trong dự án này):**
```java
Button btnGiaiToan = findViewById(R.id.btnGiaiToan);
btnGiaiToan.setOnClickListener(v -> {
    Intent intent = new Intent(this, GiaiToanActivity.class);
    startActivity(intent);
});
```

**Cách 2 — thuộc tính onClick trong XML:**
```xml
<Button
    android:id="@+id/btnGiaiToan"
    android:onClick="moGiaiToan"
    android:text="Giải toán"/>
```
Sau đó trong Java khai báo phương thức:
```java
public void moGiaiToan(View v) {
    startActivity(new Intent(this, GiaiToanActivity.class));
}
```

**So sánh:**
- Cách 1: linh hoạt hơn, viết trong Java, rõ ràng ai xử lý gì
- Cách 2: ngắn gọn hơn trong XML, nhưng khó debug hơn

---

## 2.5 Thư mục Assets

**Assets là gì:**  
Thư mục `app/src/main/assets/` dùng để chứa các file tĩnh (static) cần dùng trong app: ảnh, âm thanh, font chữ, file JSON, file HTML...

**Khác với `res/`:**

| | assets/ | res/ |
|-|---------|------|
| Truy cập | `AssetManager`, đường dẫn chuỗi | `R.drawable.xxx`, `R.raw.xxx` |
| Cấu trúc thư mục | Tự do | Phải đúng theo quy tắc |
| Loại file | Bất kỳ | Có quy định theo loại |
| Use case | File phức tạp, thư mục lồng nhau | Ảnh icon, string, layout |

**Cách sử dụng Assets trong Java:**
```java
AssetManager am = getAssets();
InputStream is = am.open("data/myfile.json");
```

---

## 2.6 App 1 — Ứng dụng chính (3 Activity)

**Cấu trúc dự án:**
```
app/
  src/main/
    java/com/example/luongquangha/
      MainActivity.java
      GiaiToanActivity.java
      WebViewActivity.java
    res/layout/
      activity_main.xml
      activity_giai_toan.xml
      activity_web_view.xml
    AndroidManifest.xml
```

### MainActivity.java (Activity 1 — About)

```java
package com.example.luongquangha;

import android.content.Intent;
import android.os.Bundle;
import android.widget.Button;
import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        Button btnGiaiToan = findViewById(R.id.btnGiaiToan);
        Button btnWebView  = findViewById(R.id.btnWebView);

        btnGiaiToan.setOnClickListener(v ->
            startActivity(new Intent(this, GiaiToanActivity.class)));

        btnWebView.setOnClickListener(v ->
            startActivity(new Intent(this, WebViewActivity.class)));
    }
}
```

<!--
  CHÈN ẢNH: Chụp Activity1 đang chạy trên emulator (hiện họ tên, MSSV, 2 nút)
  Tên file: images/app_activity1.png
-->
![Activity 1 — About](images/app_activity1.png)

---

### GiaiToanActivity.java (Activity 2 — Giải toán)

Logic giải phương trình bậc 2 ax² + bx + c = 0:
- Tính delta = b² − 4ac
- Nếu delta < 0: vô nghiệm
- Nếu delta = 0: nghiệm kép x = −b/(2a)
- Nếu delta > 0: hai nghiệm x1, x2

Sau khi tính xong, gửi kết quả lên API: `https://k58kmt.tdh.io.vn/api`

**Cấu trúc JSON gửi API:**
```json
{
  "app_by": "K225480106010",
  "input": {
    "a": 1,
    "b": -5,
    "c": 6,
    "name": "Luong Quang Ha"
  },
  "output": {
    "ketluan": "Hai nghiem phan biet",
    "abc": "x1 = 3.0  x2 = 2.0",
    "nghiem": 3.0
  }
}
```

<!--
  CHÈN ẢNH: Chụp Activity2 sau khi nhập a=1, b=-5, c=6 và bấm Giải → kết quả x1=3 x2=2
  Tên file: images/app_activity2_ketqua.png
-->
![Activity 2 — Kết quả giải toán](images/app_activity2_ketqua.png)

---

### WebViewActivity.java (Activity 3 — WebView)

Load trang web: `https://k58kmt.tdh.io.vn?masv=K225480106010`

```java
WebView webView = findViewById(R.id.webView);
webView.getSettings().setJavaScriptEnabled(true);
webView.setWebViewClient(new WebViewClient());
webView.loadUrl("https://k58kmt.tdh.io.vn?masv=K225480106010");
```

<!--
  CHÈN ẢNH: Chụp Activity3 WebView đang hiện trang web (trên điện thoại thật hoặc emulator có mạng)
  Tên file: images/app_activity3_webview.png
-->
![Activity 3 — WebView](images/app_activity3_webview.png)

---

## 2.7 App 2 — Ứng dụng dùng Assets (Mô tả ý tưởng)

**Ý tưởng app:** Ứng dụng xem danh sách câu hỏi trắc nghiệm đọc từ file JSON trong Assets

**Cấu trúc Assets:**
```
assets/
  data/
    cauhoi.json
```

**Nội dung cauhoi.json:**
```json
[
  {
    "id": 1,
    "cauhoi": "Android Studio được phát hành năm nào?",
    "dapan": ["2013", "2014", "2015", "2016"],
    "dung": 0
  }
]
```

**Đọc file từ Assets:**
```java
AssetManager am = getAssets();
InputStream is = am.open("data/cauhoi.json");
BufferedReader br = new BufferedReader(new InputStreamReader(is));
StringBuilder sb = new StringBuilder();
String line;
while ((line = br.readLine()) != null) sb.append(line);
String json = sb.toString();
```

---

# KẾT QUẢ CHẠY THỬ

## MIT App Inventor

| Screen | Chức năng | Kết quả |
|--------|-----------|---------|
| Screen1 | Hiển thị thông tin cá nhân, 2 nút chuyển màn hình | ✅ OK |
| Screen2 | Giải PT bậc 2, nhập a=1 b=−5 c=6 | ✅ x1=3, x2=2 (đúng) |
| Screen3 | WebView tải trang Apple Store VN | ✅ Load được |

## Android Studio

| Activity | Chức năng | Kết quả |
|----------|-----------|---------|
| MainActivity | Hiển thị thông tin, 2 nút chuyển Activity | ✅ OK |
| GiaiToanActivity | Giải PT bậc 2, gửi API | ✅ x1=3.0, x2=2.0 (đúng) |
| WebViewActivity | WebView tải URL | ✅ OK (trên điện thoại thật) |

<!--
  CHÈN ẢNH: Chụp toàn bộ app chạy trên emulator hoặc điện thoại thật
  Tên file: images/app_full_demo.png
-->
![Demo toàn bộ app](images/app_full_demo.png)

---

*README được tạo bởi Lương Quang Hà — K225480106010 — 58KTPM*
