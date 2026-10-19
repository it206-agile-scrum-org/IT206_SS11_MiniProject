# MINI PROJECT: PRODUCT BACKLOG VÀ KẾ HOẠCH SPRINT 1 – DỰ ÁN MOTOGO

**Họ tên:** [Điền họ tên] **Lớp:** [Điền lớp]
**Link Trello công khai:** [Dán link bảng "MotoGo – Họ tên – Lớp" tại đây]

> **Lưu ý quan trọng về SRS.** Đề bài tham chiếu SRS nhưng chưa kèm tài liệu này. Toàn bộ mã **FR/BR**, 5 module, 3 mục tiêu kinh doanh và danh sách "Ngoài phạm vi" dưới đây là **giả định của bản nháp** (đánh dấu ⚠). Khi có SRS thật, hãy đối chiếu và thay lại mã cho khớp.

### Giả định nền (⚠ thay bằng nội dung SRS thật)

**5 module:** M1 Tìm kiếm và đặt xe · M2 Thanh toán và cọc · M3 Quản lý cửa hàng và kho xe · M4 Giao nhận xe · M5 Báo cáo và đánh giá.

**3 mục tiêu kinh doanh (mục 1 SRS):**
- **G1** – Tăng tỷ lệ khách đặt xe thành công trực tuyến.
- **G2** – Giảm sự cố trùng lịch và sai lệch tồn kho xe của cửa hàng.
- **G3** – Giảm tranh chấp hư hại, mất mát khi giao nhận xe.

**Ngoài phạm vi (mục 6 SRS):** giao xe tận nơi, bảo hiểm tích hợp, thanh toán thẻ quốc tế, định vị GPS xe, chương trình khách hàng thân thiết. *(Không story nào bên dưới thuộc các mục này.)*

**Quy tắc nghiệp vụ giả định:**

| Mã | Nội dung |
|---|---|
| BR-01 | Xe chỉ hiển thị là "còn trống" khi không có đơn giữ chỗ, đơn đã xác nhận hoặc lịch bảo trì trùng khoảng thuê. |
| BR-05 | Xe được giữ chỗ 30 phút kể từ lúc tạo đơn. |
| BR-06 | Tiền cọc bằng 30% tổng giá thuê. |
| BR-07 | Một xe không được thuộc hai đơn có khoảng thời gian chồng nhau. |
| BR-08 | Cửa hàng phải phản hồi đơn trong 2 giờ, quá hạn đơn tự hủy. |
| BR-09 | Khách hủy trước giờ nhận xe 24 giờ được hoàn 100% tiền cọc. |
| BR-10 | Biên bản giao xe bắt buộc có tối thiểu 4 ảnh (trước, sau, trái, phải), số km và mức xăng. |
| BR-11 | Khi nhận lại xe, hệ thống đối chiếu ảnh và chỉ số với biên bản giao. |

---

## Hạng mục 1: Phân rã Epic – Feature

### Bảng Epic – Feature

| Epic | Giá trị nghiệp vụ | Feature | FR bao phủ |
|---|---|---|---|
| **E1 – Khách đặt được xe phù hợp một cách nhanh chóng, chắc chắn** | Khách tìm đúng xe trống và chốt được xe trong một lần, hỗ trợ **G1** | F1.1 Tìm xe trống theo thời gian | FR-01, FR-02, FR-03, FR-04 |
| | | F1.2 Giữ chỗ và đặt cọc | FR-10, FR-11, FR-12, FR-13 |
| **E2 – Cửa hàng vận hành kho xe chính xác, không trùng lịch** | Cửa hàng yên tâm nhận khách, không phải từ chối vì hai đơn trùng xe, hỗ trợ **G2** | F2.1 Xác nhận đơn thuê | FR-20 |
| | | F2.2 Quản lý kho xe và lịch xe | FR-21, FR-22, FR-23 |
| | | F2.3 Theo dõi hiệu quả kinh doanh | FR-40 |
| **E3 – Giao nhận xe minh bạch, có bằng chứng** | Hai bên có chứng cứ hình ảnh rõ ràng, giảm tranh chấp, hỗ trợ **G3** | F3.1 Biên bản giao xe | FR-30 |
| | | F3.2 Biên bản nhận lại xe | FR-31 |
| | | F3.3 Đánh giá sau chuyến thuê | FR-41 |

Tổng: 3 Epic, 8 Feature (mỗi Epic ≥ 2 Feature).

### Ảnh chụp bảng Trello

> **[Chèn ảnh chụp màn hình bảng Trello tại đây]** (4 list: Epic, Feature, Product Backlog, Sprint 1 Backlog; thẻ đã gắn nhãn).

**Cấu hình Trello cần làm:**
- Tên bảng: `MotoGo – Họ tên – Lớp`, chế độ **Public**; kiểm tra lại bằng cửa sổ ẩn danh.
- Nhãn cấp độ: `Epic`, `Feature`, `User Story`. Nhãn ưu tiên: `Must`, `Should`, `Could`, `Won't`.
- Mô tả mỗi thẻ User Story ghi: `Feature cha: F1.2 | Truy vết: FR-10, BR-05 | SP: 5`.
- Thứ tự thẻ trong list Product Backlog theo đúng thứ tự ở Hạng mục 6.

---

## Hạng mục 2: Danh sách User Story

13 story, phủ 5/5 module, 4 story cho chủ hoặc nhân viên cửa hàng (US-04, US-05, US-06, US-08, US-11 – tổng 5).

| Mã | User Story | Feature cha | Truy vết | Module |
|---|---|---|---|---|
| US-01 | Là khách thuê, tôi muốn tìm xe còn trống theo thành phố và khoảng thời gian để chọn được xe mình cần. | F1.1 | FR-01, FR-02, BR-01 | M1 |
| US-02 | Là khách thuê, tôi muốn giữ chỗ chiếc xe vừa chọn để không bị người khác đặt mất trong lúc tôi thanh toán. | F1.2 | FR-10, BR-05 | M1 |
| US-03 | Là khách thuê, tôi muốn thanh toán tiền cọc trực tuyến để chốt đơn thuê xe. | F1.2 | FR-11, BR-06 | M2 |
| US-04 | Là nhân viên cửa hàng, tôi muốn xem và xác nhận hoặc từ chối đơn mới để chủ động chuẩn bị xe. | F2.1 | FR-20, BR-08 | M3 |
| US-05 | Là chủ cửa hàng, tôi muốn hệ thống tự chặn đặt trùng lịch cho cùng một xe để không phải từ chối khách phút chót. | F2.2 | FR-21, BR-07 | M3 |
| US-06 | Là nhân viên cửa hàng, tôi muốn lập biên bản giao xe kèm ảnh để có bằng chứng tình trạng xe lúc giao. | F3.1 | FR-30, BR-10 | M4 |
| US-07 | Là khách thuê, tôi muốn lọc xe theo loại, hộp số và giá để thu hẹp lựa chọn nhanh hơn. | F1.1 | FR-03 | M1 |
| US-08 | Là nhân viên cửa hàng, tôi muốn lập biên bản nhận lại xe đối chiếu với biên bản giao để xác định hư hại phát sinh. | F3.2 | FR-31, BR-11 | M4 |
| US-09 | Là khách thuê, tôi muốn hủy đơn và nhận hoàn cọc theo chính sách để không mất tiền oan khi đổi kế hoạch. | F1.2 | FR-12, BR-09 | M2 |
| US-10 | Là khách thuê, tôi muốn xem chi tiết và hình ảnh xe để yên tâm trước khi đặt. | F1.1 | FR-04 | M1 |
| US-11 | Là chủ cửa hàng, tôi muốn xem doanh thu và số đơn theo tuần để biết hiệu quả kinh doanh. | F2.3 | FR-40 | M5 |
| US-12 | Là khách thuê, tôi muốn xem lại lịch sử các đơn đã đặt để theo dõi chuyến và đặt lại nhanh. | F1.2 | FR-13 | M1 |
| US-13 | Là khách thuê, tôi muốn đánh giá cửa hàng sau khi trả xe để chia sẻ trải nghiệm cho khách sau. | F3.3 | FR-41 | M5 |

*(Chi tiết sáu trường của US-01, US-02, US-03 ở Hạng mục 4; các story còn lại có chi tiết trên Trello.)*

---

## Hạng mục 3: Bảng tự đánh giá INVEST

Ba story được chọn: **US-02**, **US-04**, và **US-06 (bản đầu)**.

| Tiêu chí | US-02 (Giữ chỗ) | US-04 (Xác nhận đơn) | US-06 – bản trước khi sửa |
|---|---|---|---|
| **I**ndependent | Đạt – chỉ cần có đơn tạo từ US-01, không phụ thuộc story khác. | Đạt – chạy độc lập khi đã có đơn. | Chưa đạt – gộp giao và nhận xe, phụ thuộc lẫn nhau. |
| **N**egotiable | Đạt – thời hạn giữ chỗ và cách hiển thị còn thương lượng. | Đạt – hình thức thông báo còn linh hoạt. | Chưa đạt – ép sẵn cả hai bước vào một câu. |
| **V**aluable | Đạt – giảm mất đơn khi thanh toán (G1). | Đạt – cửa hàng chủ động chuẩn bị xe. | Đạt – giảm tranh chấp (G3). |
| **E**stimable | Đạt – nhóm đã hình dung rõ công việc. | Đạt – luồng đơn giản, rõ. | Chưa đạt – quá rộng, ước lượng lệch nhiều (≈21 điểm). |
| **S**mall | Đạt – 5 điểm, làm trọn trong một Sprint. | Đạt – 3 điểm. | Chưa đạt – ≈21 điểm, vượt 13. |
| **T**estable | Đạt – kiểm được bằng mốc 30 phút. | Đạt – kiểm được kết quả xác nhận/từ chối. | Chưa đạt – "tránh tranh chấp" không đo trực tiếp được. |

### Story được viết lại: US-06

| | Nội dung |
|---|---|
| **Bản trước** | "Là nhân viên cửa hàng, tôi muốn lập biên bản giao nhận xe có ảnh để tránh tranh chấp với khách." |
| **Bản sau** | **US-06:** "Là nhân viên cửa hàng, tôi muốn lập biên bản giao xe kèm tối thiểu 4 ảnh, số km và mức xăng để có bằng chứng tình trạng xe lúc giao." <br> **US-08:** "Là nhân viên cửa hàng, tôi muốn lập biên bản nhận lại xe đối chiếu với biên bản giao để xác định hư hại phát sinh." |
| **Đã sửa gì** | (1) Tách giao và nhận thành hai story độc lập (sửa I, S). (2) Thay "tránh tranh chấp" mơ hồ bằng đầu ra đo được: ≥4 ảnh, số km, mức xăng theo BR-10 (sửa T, E). (3) Bỏ ràng buộc về cách làm để giữ tính thương lượng (N). |

---

## Hạng mục 4: Acceptance Criteria

Ba story ưu tiên cao nhất: **US-01, US-02, US-03**.

### US-01

| Trường | Nội dung |
|---|---|
| Mã story | US-01 |
| User Story | Là khách thuê, tôi muốn tìm xe còn trống theo thành phố và khoảng thời gian để chọn được xe mình cần. |
| Truy vết | FR-01, FR-02, BR-01 |
| Mức ưu tiên | Must |
| Story Point | 3 |
| Acceptance Criteria | AC-01, AC-02, AC-03 |

**AC-01 (luồng chính)**
Given khách chọn thành phố Đà Nẵng và khoảng thời gian thuê hợp lệ, When khách bấm Tìm xe, Then hệ thống hiển thị danh sách các xe còn trống trong khoảng thời gian đó.

**AC-02 (tham chiếu BR-01)**
Given một xe đang có đơn đã xác nhận trùng một phần khoảng thời gian tìm, When khách bấm Tìm xe, Then xe đó không xuất hiện trong danh sách kết quả.

**AC-03 (ngoại lệ)**
Given khách chọn ngày trả xe sớm hơn ngày nhận xe, When khách bấm Tìm xe, Then hệ thống hiển thị thông báo lỗi "Thời gian thuê không hợp lệ".

### US-02

| Trường | Nội dung |
|---|---|
| Mã story | US-02 |
| User Story | Là khách thuê, tôi muốn giữ chỗ chiếc xe vừa chọn để không bị người khác đặt mất trong lúc tôi thanh toán. |
| Truy vết | FR-10, BR-05 |
| Mức ưu tiên | Must |
| Story Point | 5 |
| Acceptance Criteria | AC-04, AC-05, AC-06 |

**AC-04 (luồng chính, tham chiếu BR-05)**
Given khách đã chọn xe còn trống và bấm đặt, When hệ thống tạo đơn thành công, Then xe được giữ chỗ 30 phút.

**AC-05 (luồng chính)**
Given xe đang được giữ chỗ cho một đơn, When khách khác tìm xe trong cùng khoảng thời gian, Then xe đó không hiển thị cho khách khác.

**AC-06 (ngoại lệ, tham chiếu BR-05)**
Given đơn đang ở trạng thái chờ thanh toán, When quá 30 phút mà khách chưa thanh toán cọc, Then đơn tự động hủy.

*(Việc xe được mở lại trong kết quả tìm kiếm sau khi hủy được kiểm bằng AC-05 chạy lại trên đơn đã hủy; mỗi Then chỉ giữ một kết quả.)*

### US-03

| Trường | Nội dung |
|---|---|
| Mã story | US-03 |
| User Story | Là khách thuê, tôi muốn thanh toán tiền cọc trực tuyến để chốt đơn thuê xe. |
| Truy vết | FR-11, BR-06 |
| Mức ưu tiên | Must |
| Story Point | 5 |
| Acceptance Criteria | AC-07, AC-08, AC-09 |

**AC-07 (luồng chính, tham chiếu BR-06)**
Given đơn đang chờ thanh toán với tổng giá thuê 1.000.000 đồng, When khách mở màn hình thanh toán, Then số tiền cọc hiển thị là 300.000 đồng.

**AC-08 (luồng chính)**
Given khách đã thanh toán đủ tiền cọc trước khi hết hạn giữ chỗ, When cổng thanh toán báo thành công, Then đơn chuyển sang trạng thái "Chờ cửa hàng xác nhận".

**AC-09 (ngoại lệ)**
Given khách đang thanh toán cọc, When cổng thanh toán báo giao dịch thất bại, Then hệ thống hiển thị thông báo lỗi và cho phép khách thử thanh toán lại.

---

## Hạng mục 5: Definition of Done

### Bộ DoD (áp dụng chung cho mọi story)

| # | Điều kiện | Câu hỏi kiểm chứng (Có/Không) |
|---|---|---|
| 1 | Mã nguồn đã được ít nhất 1 thành viên khác review và merge vào nhánh chính. | Đã có ít nhất 1 approval trên pull request và đã merge chưa? |
| 2 | Mọi Acceptance Criteria của story đã được chạy kiểm thử và đạt. | Tất cả AC của story đều có kết quả "Đạt" trong bảng test chưa? |
| 3 | Unit test cho logic mới đã viết và chạy đạt, độ phủ dòng mã mới ≥ 70%. | Build tự động đã chạy xanh và độ phủ mã mới ≥ 70% chưa? |
| 4 | Không còn lỗi mức Cao hoặc Nghiêm trọng đang mở thuộc story. | Danh sách lỗi mở mức Cao/Nghiêm trọng của story bằng 0 chưa? |
| 5 | Đã triển khai lên môi trường staging và Product Owner xác nhận qua demo. | PO đã xem demo trên staging và ghi chấp nhận trên thẻ Trello chưa? |

### DoD khác Acceptance Criteria ở đâu

- **Acceptance Criteria** là điều kiện **riêng của từng story**, mô tả hệ thống phải **hành xử thế nào** để người dùng thấy đúng. **DoD** là tiêu chuẩn **chung cho mọi story**, mô tả công việc phải **hoàn tất đến mức nào** (review, test, triển khai) mới được gọi là xong.
- **Ví dụ từ bài:** AC-06 của US-02 ("quá 30 phút chưa thanh toán thì đơn tự hủy") chỉ đúng riêng cho US-02. Còn điều kiện DoD số 1 "mã nguồn được review và merge" áp dụng như nhau cho US-02, US-03, US-04 và mọi story khác. Một story có thể đạt hết AC nhưng chưa Done nếu chưa được review.

---

## Hạng mục 6: Prioritized Product Backlog

Thứ tự trong bảng chính là thứ tự thẻ trong list Product Backlog trên Trello.

| Thứ tự | Mã | Story (tóm tắt) | MoSCoW | SP |
|---|---|---|---|---|
| 1 | US-01 | Tìm xe trống theo thời gian | Must | 3 |
| 2 | US-02 | Giữ chỗ xe 30 phút | Must | 5 |
| 3 | US-03 | Thanh toán cọc trực tuyến | Must | 5 |
| 4 | US-04 | Cửa hàng xác nhận/từ chối đơn | Must | 3 |
| 5 | US-05 | Chặn đặt trùng lịch cho cùng một xe | Must | 8 |
| 6 | US-06 | Biên bản giao xe có ảnh | Must | 8 |
| 7 | US-07 | Lọc xe theo loại, hộp số, giá | Should | 2 |
| 8 | US-08 | Biên bản nhận lại xe | Should | 5 |
| 9 | US-09 | Hủy đơn, hoàn cọc | Should | 5 |
| 10 | US-10 | Xem chi tiết và ảnh xe | Should | 2 |
| 11 | US-11 | Báo cáo doanh thu theo tuần | Could | 3 |
| 12 | US-12 | Lịch sử đơn của khách | Could | 2 |
| 13 | US-13 | Đánh giá cửa hàng | Won't | 3 |

**Thống kê:** Must 6/13 ≈ 46% (≤ 50%) · Should 4 · Could 2 · Won't 1. Mỗi story thuộc đúng một mức.

### Giải trình lý do xếp hạng

| Mã | Mức | Lý do | Mục tiêu KD |
|---|---|---|---|
| US-02 | Must | Không giữ chỗ thì hai khách có thể cùng chọn một xe, đơn bị mất hoặc xung đột ngay trong lúc thanh toán; đây là chốt chặn để chuyển từ tìm sang đặt thành công. | **G1** |
| US-05 | Must | Chặn trùng lịch ở tầng dữ liệu là điều kiện sống còn để cửa hàng tin tưởng nền tảng; thiếu nó cửa hàng sẽ phải từ chối khách phút chót. | **G2** |
| US-06 | Must | Biên bản giao có ảnh là bằng chứng gốc duy nhất để xử lý hư hại; không có thì các story nhận lại và tranh chấp sau này mất căn cứ. | **G3** |
| US-09 | Should | Hủy và hoàn cọc làm khách yên tâm đặt hơn, nhưng Sprint đầu vẫn chạy được luồng đặt thành công mà chưa cần hủy chủ động (đã có tự hủy khi hết hạn giữ chỗ). | **G1** |
| US-11 | Could | Báo cáo hữu ích cho chủ cửa hàng nhưng không cản trở luồng đặt xe và giao nhận; có thể bổ sung ở phiên bản sau. | **G2** |
| US-13 | **Won't** | Đánh giá chỉ có giá trị khi đã có lượng đơn hoàn tất; phiên bản đầu cần ưu tiên chứng minh luồng đặt – giao nhận chạy đúng, đồng thời cần thêm quy tắc kiểm duyệt đánh giá chưa được làm rõ trong SRS. Chuyển sang phiên bản sau. | **G1** |

---

## Hạng mục 7: Bảng ước lượng Story Point

Thang Fibonacci: 1, 2, 3, 5, 8, 13.

**Story chuẩn:** **US-02 – Giữ chỗ xe 30 phút = 5 điểm** (có logic khóa xe, bộ đếm giờ và tự hủy; độ phức tạp trung bình, nhóm hình dung rõ).

| Mã | SP | Căn cứ so sánh với US-02 (5 điểm) |
|---|---|---|
| US-01 | 3 | Chỉ truy vấn và hiển thị, ít logic hơn US-02 vì không có khóa tài nguyên hay bộ đếm giờ. |
| US-02 | **5** | **Story chuẩn.** |
| US-03 | 5 | Tương đương US-02: phải tích hợp cổng thanh toán và xử lý thất bại, nhưng có bên thứ ba sẵn có. |
| US-04 | 3 | Màn hình danh sách và hai thao tác đổi trạng thái, đơn giản hơn US-02. |
| US-05 | 8 | Phức tạp hơn US-02: cần kiểm tra chồng lấn thời gian an toàn khi nhiều người đặt đồng thời. |
| US-06 | 8 | Lớn hơn US-02: tải ảnh, kiểm tra tối thiểu 4 ảnh, lưu số km và mức xăng. |
| US-07 | 2 | Nhỏ hơn US-02: chỉ thêm bộ lọc trên kết quả tìm kiếm có sẵn. |
| US-08 | 5 | Tương đương US-02: tái sử dụng thành phần ảnh của US-06, thêm phần đối chiếu. |
| US-09 | 5 | Tương đương US-02: có tính hoàn cọc theo mốc 24 giờ và gọi cổng thanh toán. |
| US-10 | 2 | Nhỏ hơn US-02: màn hình chỉ đọc dữ liệu xe. |
| US-11 | 3 | Nhỏ hơn US-02: tổng hợp và hiển thị số liệu, không có logic trạng thái. |
| US-12 | 2 | Nhỏ hơn US-02: danh sách chỉ đọc theo tài khoản. |
| US-13 | 3 | Nhỏ hơn US-02: biểu mẫu chấm sao, nhưng cần ràng buộc chỉ đánh giá sau khi trả xe. |

### Story vượt 13 điểm phải tách

| Trước khi tách | Ước lượng | Sau khi tách |
|---|---|---|
| "Lập biên bản giao nhận xe có ảnh" (bản đầu của US-06) | ≈ 21 (vượt 13) | **US-06** (giao xe có ảnh) = 8 điểm; **US-08** (nhận lại, đối chiếu) = 5 điểm. Tổng 13 điểm vì thành phần chụp/tải ảnh chỉ xây một lần ở US-06 rồi dùng lại ở US-08. |

---

## Hạng mục 8: Kế hoạch Sprint 1

### Sprint Goal

> **Khách du lịch có thể tìm được một chiếc xe còn trống, giữ chỗ và chốt đơn với cửa hàng mà không lo xe bị đặt trùng.**

### Sprint Backlog

- Độ dài Sprint: 2 tuần (10 ngày làm việc). Velocity giả định: **24 điểm**.

| Mã | Story | SP |
|---|---|---|
| US-01 | Tìm xe trống theo thời gian | 3 |
| US-02 | Giữ chỗ xe 30 phút | 5 |
| US-03 | Thanh toán cọc trực tuyến | 5 |
| US-04 | Cửa hàng xác nhận/từ chối đơn | 3 |
| US-05 | Chặn đặt trùng lịch cho cùng một xe | 8 |
| | **Tổng** | **24 ≤ 24** |

### Phân rã task cho US-02

| Task | Mô tả | Giờ dự kiến |
|---|---|---|
| T1 | Thiết kế bảng dữ liệu trạng thái giữ chỗ và thời hạn | 4 |
| T2 | API tạo đơn và khóa xe | 6 |
| T3 | Tác vụ tự động hủy đơn sau 30 phút | 6 |
| T4 | Giao diện nút đặt và đồng hồ đếm ngược | 5 |
| T5 | Cập nhật tìm kiếm để ẩn xe đang được giữ | 3 |
| T6 | Viết unit test và integration test | 6 |
| T7 | Kiểm thử theo AC-04, AC-05, AC-06 và sửa lỗi | 3 |
| | **Tổng** | **33** |

### Bảng capacity cá nhân

Giả định: 4 thành viên, 6 giờ làm việc thực tế mỗi ngày (đã trừ họp, nghỉ), dự phòng 15% cho phát sinh.

| Thành viên | Giờ/ngày | Số ngày Sprint | Tổng giờ | Trừ dự phòng 15% | Capacity thực |
|---|---|---|---|---|---|
| Thành viên A | 6 | 10 | 60 | 9 | **51** |
| Thành viên B (nghỉ 1 ngày) | 6 | 9 | 54 | 8 | **46** |
| Thành viên C | 6 | 10 | 60 | 9 | **51** |
| Thành viên D | 6 | 10 | 60 | 9 | **51** |
| **Tổng** | | | 234 | 35 | **199 giờ** |

Với 24 điểm trong 199 giờ (≈ 8,3 giờ/điểm), khối lượng khớp với task của US-02 (33 giờ cho 5 điểm ≈ 6,6 giờ/điểm) kèm biên độ an toàn.

---

## Phụ lục A: Nhật ký vai trò

| # | Quyết định | Vai | Căn cứ |
|---|---|---|---|
| 1 | Đặt US-05 (chặn trùng lịch) vào nhóm Must và đưa vào Sprint 1. | Product Owner | G2 và BR-07: trùng lịch làm cửa hàng mất niềm tin; nếu để muộn, dữ liệu sai sẽ khó sửa. |
| 2 | Xếp US-13 (đánh giá) vào Won't, đưa US-09 xuống Should. | Product Owner | Giữ tỷ lệ Must 46% (≤ 50%) và dồn sức cho luồng đặt – giao nhận; đã có tự hủy khi hết hạn nên chưa cần hủy chủ động ở Sprint 1. |
| 3 | Tách "biên bản giao nhận" ≈ 21 điểm thành US-06 và US-08; chốt velocity 24 điểm, không nhận thêm story vào Sprint 1. | Development Team / Scrum Master | Quy tắc không story > 13 điểm; capacity 199 giờ chỉ đủ cho 24 điểm cộng dự phòng, tránh quá tải Sprint đầu. |

**Trở ngại (Scrum Master):** chưa có SRS đầy đủ → dùng giả định có đánh dấu ⚠ và ghi vào Phụ lục B; sẽ đối chiếu khi nhận SRS.

---

## Phụ lục B: Câu hỏi và giả định

| # | Câu hỏi đặt cho khách hàng | Câu trả lời / giả định thay thế | Ảnh hưởng nếu giả định sai |
|---|---|---|---|
| 1 | Thời gian giữ chỗ một xe là bao lâu và tiền cọc là bao nhiêu phần trăm giá thuê? | *Giả định:* giữ chỗ 30 phút (BR-05), cọc 30% (BR-06). | Nếu thời hạn hoặc tỷ lệ khác, phải sửa AC-04, AC-06, AC-07, ước lượng US-02/US-03 và lịch tự hủy; có thể làm lệch Sprint Backlog. |
| 2 | Khi khách hủy đơn thì hoàn cọc theo chính sách nào, và cửa hàng có tối đa bao lâu để phản hồi đơn? | *Giả định:* hoàn 100% nếu hủy trước giờ nhận xe 24 giờ (BR-09); cửa hàng phản hồi trong 2 giờ, quá hạn đơn tự hủy (BR-08). | Nếu chính sách hoàn cọc phức tạp hơn (hoàn theo bậc), US-09 tăng điểm và có thể phải chuyển lên Must; nếu thời hạn phản hồi khác, phải sửa US-04 và các AC liên quan. |
