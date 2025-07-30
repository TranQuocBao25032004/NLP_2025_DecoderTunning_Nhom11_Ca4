Đây là file được chạy bằng "kaggle" bằng cách sử dụng 2 mô hình : GPT2 và Mistral 7B 
mô hình GPT2 large với 345M tham số
mô hình Mistral 7B với 7B tham số

Các dataset được tải về bằng code : 
dataset bao gồm : Agnews,SST2,yelp, yahoo,dbpedia,rte,MNLI(m/mm),SNLI,Fewnerd,imdb 

bằng cách sử dụng việc cấu hình file gốc : 
Decoder Tuning (DecT): Efficient Language Understanding as Decoding – Ganqu Cui et al. Đề xuất phương pháp DecT cho huấn luyện nhanh các tác vụ NLP với mô hình khổng lồ chỉ qua API (MaaS). Thay vì chỉ tối ưu prompt, DecT thêm một mạng decoder trên đầu các phản hồi gợi ý của mô hình gốc, cho phép tối ưu gradient để điều chỉnh đầu ra. Nhờ vậy, DecT chỉ cần một truy vấn mô hình/phân tích trên mỗi ví dụ và huấn luyện rất nhanh (chỉ trong vài giây). Thí nghiệm trên nhiều bộ dữ liệu NLU cho thấy DecT cho hiệu suất cao hơn các phương pháp hiện tại với tốc độ huấn luyện nhanh hơn đến 200×
Hội nghị: ACL 2023. Liên kết: ACL Anthology. Mã nguồn: github.com/thunlp/DecT
. Phương pháp: Thêm mạng giải mã (decoder) vào đầu đầu ra gợi ý, cho phép tối ưu gradient thay vì chỉ prompt-tuning. Đóng góp: Cải thiện tốc độ huấn luyện NLU từ API (MaaS) – DecT đạt tốc độ nhanh gấp ~200 lần so với các phương pháp hiện có trong khi nâng cao hiệu suất
GitHub - OpenBMB/DecT: Source code for ACL 2023 paper Decoder Tuning: Efﬁcient Language Understanding as Decoding
GITHUB.COM
GitHub - OpenBMB/DecT: Source code for ACL 2023 paper Decoder Tuning: Efﬁcient Language Understanding as Decoding

được thực hiện và nghiên cứu dựa trên bài báo : https://aclanthology.org/2023.acl-long.840.pdf
