<div align="center">

<img src="Docs/images/icon.png" width="128" alt="Biểu tượng OverSub">

# OverSub cho Windows

Phụ đề tiếng Việt và giọng đọc cho game trên máy Windows của bạn, dùng tay cầm, cảm ứng, bàn phím hay chuột đều được.

OverSub đọc chữ trong game trên màn hình, dịch bằng AI rồi hiện bản dịch đè lên chỗ chữ gốc và đọc to lời thoại bằng giọng Việt. App dùng được với game Windows chạy trên máy và với máy console (Switch, PlayStation, Xbox) qua capture card.

[![Tải bản mới nhất](https://img.shields.io/github/v/release/imhillxtz/oversub-windows?include_prereleases&label=T%E1%BA%A3i%20v%E1%BB%81&color=F96B3F)](https://github.com/imhillxtz/oversub-windows/releases)
![Windows 11 x64](https://img.shields.io/badge/Windows%2011-x64-555)
![Bảo lưu mọi quyền](https://img.shields.io/badge/b%E1%BA%A3n%20quy%E1%BB%81n-b%E1%BA%A3o%20l%C6%B0u%20m%E1%BB%8Di%20quy%E1%BB%81n-555)

Tiếng Việt · [English](README.en.md)

</div>

Kho này chỉ chứa bộ cài và tài liệu. Mã nguồn của OverSub cho Windows không được công khai. Bản cho Mac ở [imhillxtz/oversub-mac](https://github.com/imhillxtz/oversub-mac).

OverSub cho Windows đang ở giai đoạn thử nghiệm: các bản phát hành được gắn nhãn Pre-release và có thể còn lỗi.

## OverSub làm được gì

- Phụ đề: đọc lời thoại trong vùng bạn chọn, dịch rồi hiện bản dịch đè lên ô phụ đề của game. Có thể xem ở Phụ đề nổi, một dải phụ đề riêng nằm trên game và kéo đi đâu cũng được.
- Giọng đọc: đọc to lời thoại đã dịch bằng giọng Việt VieNeu chạy ngay trên máy. Câu thoại được đọc trước chữ trên màn hình; câu kế được chuẩn bị trong lúc câu trước đang đọc, và khi thoại dồn dập thì giọng đọc nhanh hơn một chút để theo kịp.
- Dịch màn hình: dịch chữ ngoài lời thoại như menu, bảng nhiệm vụ, mô tả vật phẩm.
- Lịch sử thoại: xem lại và đọc lại các câu đã dịch. Câu cố định trên màn hình (logo, nhãn) có thể bỏ qua để từ đó không bị dịch hay đọc nữa.
- Mỗi game nhớ riêng vùng chọn, thể loại và ngôn ngữ. Thể loại (trung cổ, kiếm hiệp, anime...) giúp AI chọn xưng hô và văn phong. OverSub nhớ cách từng nhân vật đã xưng hô để dịch các câu sau theo.
- Điều khiển trọn bằng tay cầm, cảm ứng, chỉ bàn phím, hoặc bàn phím và chuột (xem mục Khác gì bản Mac).
- Giao diện tiếng Việt và tiếng Anh. Dịch sang 12 ngôn ngữ; ngôn ngữ khác tiếng Việt dùng giọng có sẵn của Windows.

## Khác gì bản Mac

Bản Mac làm cho máy Mac với chuột và bàn phím. Máy Windows thì nhiều dạng hơn: PC để bàn, laptop, máy 2 trong 1 và máy tính bảng có màn cảm ứng, máy chơi game cầm tay. Bản Windows được thiết kế để mọi màn hình của OverSub dùng được bằng tay cầm, cảm ứng, bàn phím hoặc chuột, và bạn kết hợp các cách này tuỳ máy và tuỳ lúc: chỉ cảm ứng và phím tắt trên máy 2 trong 1, tay cầm và cảm ứng trên máy cầm tay, bàn phím và chuột trên PC. OverSub đổi gợi ý nút theo thứ bạn vừa dùng, và màn chọn cách chơi ghi đúng tên máy của bạn.

| Cách điều khiển | Trong OverSub |
|---|---|
| Tay cầm | Mọi màn hình đi được bằng D-pad, A và B; LB, RB đổi tab trong Cài đặt. Trong game, giữ View rồi bấm thêm một nút. |
| Cảm ứng | Mục bấm cao ít nhất 48 điểm. Kéo khung chọn vùng bằng ngón tay, chạm hai lần để phóng to hình, chạm màn hình để hiện thanh nút. Bàn phím ảo hiện khi cần gõ key hay tên game và tự cất khi xong. |
| Chỉ bàn phím | Tab, mũi tên và Enter đi qua các nút; Ctrl Tab đổi tab trong Cài đặt. Trong game, dùng phím tắt Ctrl Alt. |
| Bàn phím và chuột | Rê chuột hay gõ phím thì gợi ý nút tay cầm ẩn đi và bảng phím trong game đổi sang Ctrl Alt; bấm tay cầm thì đổi lại. |

### Xbox Full Screen Experience

Nếu máy của bạn dùng Xbox Full Screen Experience, Windows chỉ gửi nút tay cầm cho app đang ở phía trước, tức là game. OverSub đọc tay cầm qua GameInput của Windows nên tổ hợp giữ View vẫn tới được OverSub trong lúc chơi. Màn hình của ứng dụng Xbox, Armoury Crate, Steam, Playnite và các trình chơi game khác không bị đọc; OverSub chỉ đọc khi game ở phía trước. Nếu Steam Input đổi tay cầm thành phím (bố cục desktop), OverSub hiểu lại các phím đó là nút tay cầm trên các màn hình của mình.

## Ba cách chơi

Mỗi lần mở, OverSub hỏi "Hôm nay bạn chơi gì?" và chọn sẵn cách bạn dùng lần trước. Đổi lại lúc nào cũng được bằng nút Đổi cách chơi.

### Chơi game trên máy này

Game Windows mở từ Steam, Epic, Xbox hay trình chơi game của máy. Bấm Bắt đầu rồi mở game; chữ dịch đè lên ô phụ đề của game và giọng Việt đọc to. OverSub chỉ đọc khi game ở phía trước, không đọc màn hình Windows hay trình chơi game. Trong game, giữ View rồi bấm một nút để chọn vùng, tạm dừng hay mở lại OverSub (bảng nút ở mục Điều khiển trong game).

### Xem và chơi qua capture card

Hình và tiếng của máy console hiện ngay trên máy này, chữ dịch đè lên hình. Có thể xem toàn màn hình; chạm hai lần vào hình cũng phóng to.

### Chơi trên TV

Máy console xuất hình ra TV qua capture card, còn máy Windows đặt cạnh TV làm màn đọc: câu thoại chữ to, giọng đọc to, menu dịch kèm hình. Màn đọc có Lịch sử thoại và nút Đọc lại, dùng được bằng cảm ứng hoặc tay cầm.

## Yêu cầu

- Windows 11 trên máy x64: PC để bàn, laptop, máy 2 trong 1 hay máy chơi game cầm tay. Windows 10 bản 2004 trở lên cài được nhưng chưa được thử.
- Key API của Gemini hoặc Groq để dịch. Cả hai đều có gói miễn phí, xem mục Thêm key dịch.
- Python 3.13 hoặc 3.12 và gói `vieneu` cho giọng đọc tiếng Việt. Bộ cài không kèm phần này; cách cài ở mục Giọng đọc tiếng Việt. Chưa cài thì app vẫn dịch và hiện chữ, chỉ không đọc.
- Hai cách chơi qua capture card cần một capture card kiểu webcam (UVC) có luồng MJPEG 1080p. OverSub được thử với capture card Hagibis.
- Gói đọc chữ của Windows cho ngôn ngữ trong game. Tiếng Anh thường có sẵn; với ngôn ngữ khác, app sẽ nhắc cài ở Settings → Time & language → Language & region. Trên Windows 11, nếu máy có Snipping Tool, OverSub tự dùng bộ đọc chữ của Snipping Tool (OneOCR) để đọc chính xác hơn với chữ nhỏ.

Bộ cài đã kèm .NET, nên không cần cài .NET riêng.

## Cài đặt

1. Vào trang [Releases](https://github.com/imhillxtz/oversub-windows/releases), tải tệp `OverSub-Setup-x.y.z.exe` ở mục Assets.
2. Mở tệp vừa tải. Bộ cài chưa có chữ ký số nên Windows SmartScreen sẽ hiện "Windows protected your PC". Bấm More info, kiểm tra tên tệp là `OverSub-Setup-x.y.z.exe`, rồi bấm Run anyway. Trình duyệt cũng có thể báo tệp "không thường được tải về"; chọn Giữ lại (Keep).
3. Làm theo các bước của bộ cài. OverSub được cài cho tài khoản Windows của bạn vào `%LOCALAPPDATA%\Programs\OverSub`, không cần quyền quản trị, và có lối tắt trong Start menu.

Bạn có thể kiểm tra tệp tải về đúng là bản chính thức bằng mã SHA-256 đi kèm mỗi bản phát hành. Trong PowerShell:

```powershell
Get-FileHash .\OverSub-Setup-x.y.z.exe -Algorithm SHA256
```

So kết quả với nội dung tệp `OverSub-Setup-x.y.z.exe.sha256` trên trang Releases.

OverSub chưa tự cập nhật. Để nhận thông báo khi có bản mới, bấm Watch → Custom → Releases ở đầu trang kho này. Để cập nhật, chạy bộ cài của bản mới; cài đặt và key được giữ nguyên.

## Thêm key dịch

1. Lấy key miễn phí ở [Google AI Studio](https://aistudio.google.com/apikey) (Gemini) hoặc [Groq](https://console.groq.com/keys).
2. Mở OverSub, bấm Cài đặt, chọn tab Dịch vụ dịch.
3. Dán key vào ô Key Gemini hoặc Key Groq, bấm Thêm. App thử key trước và chỉ thêm khi key dùng được.
4. Bấm Lưu.

| Dịch vụ | Ghi chú |
|---|---|
| Gemini | Dịch hay nhất trong nhóm miễn phí. Hạn mức tính theo dự án Google Cloud, nên nhiều key cùng một dự án dùng chung hạn mức. |
| Groq | Rất nhanh. Khi Gemini lỗi hay chậm quá 2,5 giây, câu đó được Groq dịch thay. |

Nên thêm cả hai để dự phòng. Nếu bản AI chưa về sau 1,5 giây, app hiện tạm bản Google Dịch (không cần key) rồi thay bằng bản AI khi có; tắt bằng ô Hiện bản Google Dịch trong lúc chờ AI ở tab Dịch vụ dịch. Hạn mức miễn phí do từng nhà cung cấp đặt và có thể thay đổi.

## Giọng đọc tiếng Việt

Giọng Việt dùng [VieNeu-TTS](https://github.com/pnnbao97/VieNeu-TTS) (giấy phép Apache 2.0), chạy trên máy qua Python. Cài một lần như sau, cần mạng:

1. Mở Terminal (chuột phải nút Start → Terminal) và cài Python 3.13:

   ```powershell
   winget install -e --id Python.Python.3.13 --scope user
   ```

   Nếu tự tải ở [python.org](https://www.python.org/downloads/windows/), hãy chọn bản "Windows installer (64-bit)" của Python 3.13 hoặc 3.12 và cài với lựa chọn mặc định. Python cài từ Microsoft Store không dùng được.

2. Cài gói giọng đọc:

   ```powershell
   & "$env:LOCALAPPDATA\Programs\Python\Python313\python.exe" -m pip install vieneu
   ```

3. Mở lại OverSub. Lần đầu, VieNeu tải model giọng từ Hugging Face nên cần chờ lâu hơn; những lần sau giọng sẵn sàng sau vài giây.

Ở tab Giọng đọc trong Cài đặt có hai bộ giọng: Nano (nhanh, mặc định) và Turbo (hay hơn, chậm hơn), kèm nút Nghe thử. Nếu giọng không lên, dòng dưới chữ Giọng sẽ ghi lý do, và nhật ký ở tab Chung có chi tiết.

## Điều khiển trong game

Khi chơi game trên máy, nút bấm cũng tới game, nên OverSub dùng tổ hợp giữ View cộng một nút. Không có tay cầm thì dùng phím tắt Ctrl Alt. Giữ View lâu một chút trong game là bảng này hiện ở góc trên bên trái.

| Việc | Tay cầm (giữ View rồi bấm) | Bàn phím |
|---|---|---|
| Chọn vùng phụ đề và vùng dịch màn hình | X | Ctrl Alt R |
| Đọc lại câu vừa rồi | Y | Ctrl Alt Space |
| Tạm dừng hay chạy tiếp | B | Ctrl Alt P |
| Ẩn hay hiện chữ dịch | A | Ctrl Alt H |
| Bật hay tắt dịch màn hình | RB | Ctrl Alt T |
| Bật hay tắt phụ đề nổi | LT | Ctrl Alt J |
| Chỉnh chỗ, bề rộng và cỡ chữ của phụ đề nổi | RT | |
| Bỏ qua câu đang hiện, từ nay không dịch nữa | LB | |
| Mở cửa sổ OverSub | Menu | Ctrl Alt O |

## Quyền riêng tư và dữ liệu

Hình màn hình và hình từ capture card không rời khỏi máy; việc đọc chữ chạy trên máy. Giọng VieNeu cũng chạy trên máy.

Khi dịch, chỉ chữ được gửi đi. Dịch vụ bạn đã thêm key nhận câu cần dịch, vài câu trước làm ngữ cảnh và tên nhân vật. Google Dịch nhận chữ cho bản dịch tạm của câu thoại và của Dịch màn hình. Nếu không muốn gửi chữ tới Google Dịch, vào tab Dịch vụ dịch, tắt ô Hiện bản Google Dịch trong lúc chờ AI và đặt Tốc độ Dịch màn hình là Chờ bản AI.

OverSub không có máy chủ riêng, không thu thập thống kê và không có quảng cáo. Key nằm trong `%LOCALAPPDATA%\OverSub\keys.bin`, được Windows mã hoá theo tài khoản người dùng của bạn. Cài đặt, hồ sơ game và trí nhớ dịch cũng ở `%LOCALAPPDATA%\OverSub`. Nhật ký chẩn đoán ở `%LOCALAPPDATA%\OverSub\Logs`; nhật ký có chữ đọc được trong game.

## Gỡ cài đặt

Vào Settings → Apps → Installed apps, tìm OverSub, bấm Uninstall. Thư mục `%LOCALAPPDATA%\OverSub` (cài đặt, key, nhật ký) được giữ lại để lần cài sau dùng tiếp; xoá thư mục này nếu muốn xoá hết. Python và gói `vieneu` gỡ riêng.

## Giới hạn hiện tại

- Bộ cài chưa có chữ ký số, nên SmartScreen cảnh báo ở lần mở đầu.
- Chưa có bản cho máy Windows chip ARM.
- Chưa tự cập nhật.
- Giọng Việt cần cài Python riêng. Trong khoảng 7 giây đầu sau khi mở app, lúc giọng đang nạp, câu thoại có thể chỉ hiện chữ mà không được đọc.
- Bản này mới được thử kỹ trên một máy (ROG Ally) với một loại capture card. Nếu OverSub chạy chưa đúng trên máy của bạn, vui lòng báo qua Issue.

## Báo lỗi và góp ý

Vui lòng mở một [Issue](https://github.com/imhillxtz/oversub-windows/issues), ghi phiên bản OverSub, máy đang dùng, tên game và cách chơi (trên máy, xem và chơi, hay chơi trên TV). Nếu được, đính kèm tệp nhật ký mới nhất trong `%LOCALAPPDATA%\OverSub\Logs` (ở Cài đặt → Chung có nút Mở thư mục). Vui lòng đọc lại nhật ký trước khi gửi, vì nhật ký có chữ trong game.

## Ủng hộ

OverSub miễn phí cho mọi người. Nếu thấy app hữu ích, bạn có thể mời mình một ly cà phê qua [paypal.me/ngochieuit](https://paypal.me/ngochieuit) hoặc mã VietQR trong [README bản Mac](https://github.com/imhillxtz/oversub-mac#%E1%BB%A7ng-h%E1%BB%99). Gắn sao cho kho này hoặc giới thiệu OverSub với bạn bè cũng là một cách ủng hộ.

## Bản quyền

© 2026 imhillxtz. Bảo lưu mọi quyền.

OverSub được dùng miễn phí nhưng không phải phần mềm mã nguồn mở, và mã nguồn của bản Windows không được công khai. Việc phân phối lại bộ cài, sửa đổi hay dịch ngược chương trình cần có sự đồng ý bằng văn bản của tác giả. Chi tiết xem tại [LICENSE](LICENSE).

Bộ cài kèm runtime .NET và một số thư viện mã nguồn mở theo giấy phép riêng của từng thư viện, liệt kê trong `THIRD-PARTY-NOTICES.txt` ở thư mục cài. Tên game và nhãn hiệu nhắc tới thuộc về chủ sở hữu tương ứng. OverSub dùng dịch vụ của Google và Groq theo điều khoản của từng nhà cung cấp.
