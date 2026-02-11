# Translation-machine (Dịch chữ Trung  Quốc -> Tiếng Việt)

#Sử dụng kiến trúc Transformer và bổ sung thay thế các thành phần
+ LayerNorm --->  RMS Norm
+ Positional Embediing ---> Rotary Position Embedding
+ multi-head attention ---> Grouped-query attention
+ Feed-forward ---> FFN +SwiGLU
+ CrossENtropy ----> LabelSmoothedCrossEntropy

Bổ sung thêm thành phần Constrastive Learning theo tinh thần self-supervised để tăng cường biểu diễn embedding của token

Dùng beamsearch để giải mã thay vì tham lam

#Chiến thuật bổ sung dữ liệu. Cho mô hình dịch ngôn ngữ tiếng việt sang tiếng Trung rồi lấy các câu có  chỉ số BLEU cao nhất để bổ sung thêm vào Dataset

#Kết quả : Best valid loss: 0.9510 | Best BLEU: 42.76 và sau khi thêm phần constrastive Learning :Best valid loss (augmented): 0.7715 | Best BLEU (augmented): 54.60


