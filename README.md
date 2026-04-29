# 🤖 Attention & Transformer in NLP

> 📚 Nghiên cứu chuyên sâu về cơ chế Attention, Transformer và ứng dụng trong mô hình học sâu (Deep Learning)

---

## 📖 Mục lục

- [Chương 1 – Attention trong Seq2Seq](#chương-1--attention-trong-seq2seq)
- [Chương 2 – Kiến trúc Transformer](#chương-2--kiến-trúc-transformer)
- [Chương 3 – Generative Pre-trained Transformer (GPT)](#chương-3--generative-pre-trained-transformer-gpt)
- [Chương 4 – Thư viện Faker](#chương-4--thư-viện-faker)

---

# CHƯƠNG 1 – ATTENTION TRONG MÔ HÌNH SEQUENCE TO SEQUENCE

## 1.1 Giới thiệu mô hình Sequence to Sequence (Seq2Seq)
Mô hình Seq2Seq được sử dụng để chuyển đổi một chuỗi đầu vào thành chuỗi đầu ra, thường dùng trong:
- Machine Translation  
- Text Summarization  
- Chatbot  

---

## 1.2 Kiến trúc của mô hình Seq2Seq

### 1.2.1 Quá trình huấn luyện
- Encoder xử lý input sequence  
- Decoder học cách sinh output sequence  

### 1.2.2 Quá trình dự đoán
- Encoder tạo context vector  
- Decoder dự đoán từng token  

---

## 1.3 Hạn chế của Seq2Seq Encoder-Decoder
- Mất thông tin với chuỗi dài  
- Context vector bị bottleneck  

---

## 1.4 Giới thiệu Attention
Attention giúp mô hình tập trung vào các phần quan trọng của input khi dự đoán output.

---

## 1.5 Bahdanau Attention & Luong Attention

### 1.5.1 Bahdanau Attention
- Additive Attention  
- Tính alignment score bằng neural network  

### 1.5.2 Luong Attention
- Multiplicative Attention  
- Nhanh hơn, ít tốn tài nguyên  

---

## 1.6 Global vs Local Attention

### 1.6.1 Global / Soft Attention
- Xét toàn bộ input sequence  

### 1.6.2 Local / Hard Attention
- Chỉ tập trung vào một phần input  

---

## 1.7 Extended Attention
Các biến thể mở rộng của Attention để cải thiện hiệu suất.

---

## 1.8 Alignment Score Function
Một số hàm phổ biến:
- Dot Product  
- General  
- Concatenation  

---

## 1.9 Cách hoạt động của Attention

### 1.9.1 Chuẩn bị Encoder Hidden State  
### 1.9.2 Tính Alignment Score  
### 1.9.3 Softmax hóa Score  
### 1.9.4 Tính Context Vector  
### 1.9.5 Tổng hợp Context  
### 1.9.6 Đưa vào Decoder  

---

## 1.10 Kết luận
Attention giải quyết hạn chế của Seq2Seq và cải thiện hiệu suất đáng kể.

---

# CHƯƠNG 2 – KIẾN TRÚC TRANSFORMER

## 2.1 Positional Encoding
Giúp mô hình hiểu thứ tự của từ trong chuỗi.

---

## 2.2 Masked Multi-Head Attention
Ngăn mô hình nhìn thấy future tokens trong quá trình training.

---

## 2.3 Add & Norm + Feed Forward
- Residual connection  
- Layer normalization  
- Fully connected layers  

---

## 2.4 Self-Attention & Multi-Head Attention

### 2.4.1 Self-Attention là gì?
Cơ chế cho phép mỗi từ “chú ý” đến các từ khác trong câu.

---

### 2.4.2 Quy trình Self-Attention

#### Bước 1: Chuẩn bị Input  
#### Bước 2: Khởi tạo Weight (Q, K, V)  
#### Bước 3: Tính Q, K, V  
#### Bước 4: Tính Attention Score  
#### Bước 5: Softmax  
#### Bước 6: Weighted Values  
#### Bước 7: Tổng hợp Output  
#### Bước 8: Lặp lại cho các token  

---

### 2.4.3 Multi-Head Self-Attention
- Chạy nhiều attention song song  
- Giúp học nhiều mối quan hệ  

---

## 2.5 So sánh Attention vs Self-Attention

| Tiêu chí | Attention | Self-Attention |
|----------|----------|---------------|
| Phạm vi  | Encoder-Decoder | Trong cùng chuỗi |
| Ứng dụng | Seq2Seq | Transformer |
| Hiệu suất | Trung bình | Cao |

---

# CHƯƠNG 3 – GENERATIVE PRE-TRAINED TRANSFORMER (GPT)

## 3.1 Giới thiệu GPT
Mô hình ngôn ngữ dựa trên Transformer, dùng để sinh văn bản.

---

## 3.2 Next Token Prediction
Dự đoán từ tiếp theo dựa trên ngữ cảnh trước đó.

---

## 3.3 Cách xây dựng
- Pre-training  
- Fine-tuning  

---

## 3.4 Query - Key - Value
Ba thành phần cốt lõi của Attention:
- Query (Q)  
- Key (K)  
- Value (V)  

---

## 3.5 Positional Encoding
Giữ thông tin vị trí của token trong chuỗi.

---

## 3.6 Ứng dụng
- Chatbot  
- Text generation  
- Code generation  

---

## 3.7 So sánh với RNN

---

# CHƯƠNG 4 – THƯ VIỆN FAKER

## 4.1 Cài đặt Faker
