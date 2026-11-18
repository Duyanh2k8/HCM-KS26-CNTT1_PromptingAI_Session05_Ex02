# [Bài thực hành 2] Xây dựng chuỗi Prompt viết bài PR sản phẩm công nghệ
## 1. Thiết kế chuỗi Prompt Chaining
### Bước 1: Nghiên cứu khách hàng mục tiêu (Research)
Mục tiêu: Xác định khách hàng tiềm năng và những vấn đề mà sản phẩm AI Chatbot có thể giải quyết.

---
**PROMPT 1 – NGHIÊN CỨU KHÁCH HÀNG**

**C - Context:** Công ty đang chuẩn bị ra mắt một giải pháp AI Chatbot dành cho doanh nghiệp, hỗ trợ tự động trả lời khách hàng, tư vấn sản phẩm và giảm tải công việc cho nhân viên chăm sóc khách hàng.

**R - Request:** Hãy nghiên cứu đối tượng khách hàng mục tiêu và xác định những nỗi đau (Pain Points) mà sản phẩm có thể giải quyết.

**E - Explanation:** Phân tích theo các nội dung:
- Nhóm khách hàng mục tiêu.
- Nhu cầu và hành vi của khách hàng.
- Những khó khăn thường gặp khi chăm sóc khách hàng.
- Các Pain Points quan trọng nhất.
- Lợi ích mà AI Chatbot có thể mang lại để giải quyết từng vấn đề.

**A - Actor:** Bạn là chuyên gia nghiên cứu thị trường trong lĩnh vực công nghệ và Marketing.

**T - Tone:** Chuyên nghiệp, rõ ràng, có tính thực tế.

**E - Extras:** Xuất kết quả dưới dạng JSON với cấu trúc:
```JSON
{
  "target_audience": [],
  "customer_needs": [],
  "pain_points": [
    {
      "problem": "",
      "impact": "",
      "solution": ""
    }
  ],
  "product_benefits": []
}
```
Không tự tạo ra số liệu thị trường nếu không có nguồn xác thực.

Đây là dữ liệu đầu vào bắt buộc cho Prompt 2.

---
**Output bước 1:** Danh sách khách hàng mục tiêu, nhu cầu, vấn đề và lợi ích sản phẩm.
### Bước 2: Xây dựng dàn ý bài PR (Outline)
**Mục tiêu:** Chuyển kết quả nghiên cứu ở bước 1 thành một dàn ý bài PR có bố cục hợp lý.

---
**PROMPT 2 – XÂY DỰNG DÀN Ý BÀI PR**

**C - Context:** Tôi đang xây dựng bài PR giới thiệu giải pháp AI Chatbot cho doanh nghiệp.

**R - Request:** Dựa trên toàn bộ dữ liệu JSON từ Prompt 1, hãy xây dựng dàn ý chi tiết cho bài PR có độ dài dự kiến 1000–1500 từ.

**E - Explanation:** Dàn ý cần có các phần:
1. Headline: Tiêu đề thu hút, có từ khóa chính.
2. Lead: Giới thiệu vấn đề và thu hút người đọc.
3. Thực trạng: Những khó khăn doanh nghiệp đang gặp phải.
4. Giải pháp: Giới thiệu AI Chatbot và cách hoạt động.
5. Lợi ích: Phân tích cách sản phẩm giải quyết từng Pain Point.
6. Ứng dụng thực tế: Các tình huống doanh nghiệp có thể sử dụng.
7. Kết luận: Khẳng định giá trị sản phẩm.
8. CTA: Kêu gọi khách hàng tìm hiểu hoặc đăng ký tư vấn.

**A - Actor:** Bạn là chuyên gia Content Marketing và SEO.

**T - Tone:** Chuyên nghiệp, tin cậy, thuyết phục nhưng không phóng đại.

**E - Extras:**
- Mỗi phần cần có tiêu đề H2, H3 phù hợp.
- Sắp xếp nội dung theo trình tự logic.
- Xác định từ khóa SEO chính và từ khóa phụ.
- Ghi rõ Pain Point nào sẽ được giải quyết trong từng phần.
- Không tự ý thêm thông tin sản phẩm chưa được cung cấp.

Xuất kết quả theo cấu trúc JSON gồm:
```JSON
{
  "headline": "",
  "main_keyword": "",
  "secondary_keywords": [],
  "outline": [
    {
      "heading": "",
      "subheadings": [],
      "key_points": [],
      "related_pain_points": []
    }
  ],
  "cta": ""
}
```
**Dữ liệu đầu vào:** Dán toàn bộ JSON Output của Prompt 1 vào đây.

Đây là dữ liệu bắt buộc để thực hiện Prompt 3.

---
**Output bước 2:** Dàn ý hoàn chỉnh, hệ thống tiêu đề H2/H3 và bộ từ khóa SEO.
### Bước 3: Viết bài PR hoàn chỉnh (Content Generation)
**Mục tiêu:** Triển khai nội dung theo dàn ý, đảm bảo bài viết có chiều sâu và nhất quán.

---
**PROMPT 3 – VIẾT BÀI PR VÀ TỐI ƯU SEO**

**C - Context:** Tôi cần viết bài PR chuyên sâu giới thiệu giải pháp AI Chatbot cho doanh nghiệp, độ dài từ 1000–1500 từ.

**R - Request:** Dựa hoàn toàn trên JSON Output của Prompt 2 và dữ liệu nghiên cứu từ Prompt 1, hãy triển khai thành bài PR hoàn chỉnh.

**E - Explanation:**
- Viết đầy đủ các phần theo đúng thứ tự trong dàn ý.
- Phần mở đầu phải đề cập đến vấn đề thực tế của khách hàng.
- Nội dung từng phần cần phân tích rõ ràng, tránh lặp ý.
- Lồng ghép từ khóa chính và từ khóa phụ tự nhiên.
- Sử dụng tiêu đề H2, H3 đúng cấu trúc.
- Cuối bài phải có CTA rõ ràng.

**A - Actor:** Bạn là chuyên gia Content Marketing, SEO và Copywriting trong lĩnh vực công nghệ.

**T - Tone:** Chuyên nghiệp, tin cậy, dễ hiểu và thuyết phục. Giữ nguyên giọng văn từ đầu đến cuối.

**E - Extras:**
- Không tự ý thay đổi dàn ý đã được duyệt.
- Không bịa đặt tính năng, số liệu hoặc đánh giá khách hàng.
- Độ dài bài viết từ 1000–1500 từ.
- Kiểm tra sự liên kết giữa các đoạn.
- Hạn chế nhồi nhét từ khóa SEO.

**Dữ liệu đầu vào:**
1. JSON Output của Prompt 1.
2. JSON Output của Prompt 2.

Hãy viết bài theo từng phần. Nếu nội dung quá dài, chia thành nhiều lượt nhưng phải giữ nguyên cấu trúc và giọng văn.

---
**Output bước 3:** Bài PR hoàn chỉnh gồm Headline, Lead, H2, H3, nội dung chi tiết và CTA.
## 2. Quy trình truyền dữ liệu giữa các Prompt
Để tránh mất ngữ cảnh và đảm bảo tính nhất quán, sử dụng cấu trúc truyền dữ liệu như sau:
```mermaid
flowchart TD
  A["PROMPT 1 – RESEARCH</br>Phân tích khách hàng và Pain Points</br>Output JSON 1"]
  B["PROMPT 2 – OUTLINE</br>Xây dựng dàn ý và từ khóa SEO</br>Output JSON 2"]
  C["PROMPT 3 – CONTENT</br>Viết bài PR và tối ưu SEO</br>Bài PR hoàn chỉnh"]

  A --> |"Truyền JSON 1 làm đầu vào"|B
  B --> |"Truyền JSON 2 làm đầu vào"|C

  Style A fill:#e5edfc,stroke:#e5edfc,color:#111
  Style B fill:#e1f5ef,stroke:#e1f5ef,color:#111
  Style C fill:#f1e6fa,stroke:#f1e6fa,color:#111
```
