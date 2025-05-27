# **Visual-Agentic-AI**
Trong phần này, chúng ta sẽ sử dụng thư viện LangGraph để xây dựng agent dựa trên kiến trúc
 Supervisor thông qua thư viện LangGraph.
 LangGraph là một framework xây dựng trên LangChain, cho phép mô hình hóa các quy trình tác vụ
 của LLM dưới dạng đồ thị trạng thái có vòng lặp (stateful graph). Một trong những cấu trúc mạnh mẽ
 mà LangGraph hỗ trợ là multi-agent supervisor architecture– nơi một agent đóng vai trò "supervisor"
 (giám sát), điều phối các agent con có chuyên môn khác nhau để hoàn thành tác vụ.
 Kiến trúc này phản ánh mô hình phân quyền trong các tổ chức thực tế: supervisor giống như người
 quản lý, còn các agents con là nhân viên chuyên môn (ví dụ: tìm kiếm thông tin, phân tích số liệu, lập
 kế hoạch).
 Trong đó:
 • Supervisor: Là agent trung tâm có mục đích điều phối hoạt động thực hiện các tác vụ và tương
 tác với các agent khác.
 • Hai agents thực hiện hành động chính: Research agent và Vision agent. Các tác nhân này tương
 tác trực tiếp với Supervisor Agent.
 • Các agent thiết kế dựa vào ReAct Agent
  Kiến trúc của agent như sau:
![Screenshot 2025-05-27 173215](https://github.com/user-attachments/assets/9630b22a-f87b-431b-bb81-756fc1eff933)

 ReAct Agent hoạt động dựa trên việc kết hợp:
 • Reasoning (Suy luận): Mô hình suy nghĩ về vấn đề, phân tích tình huống và lập kế hoạch cho
 hành động tiếp theo.
 • Acting (Hành động): Mô hình thực hiện các hành động dựa trên suy luận của mình, thu thập
 thông tin mới và tiếp tục quá trình
 ![Screenshot 2025-05-27 173359](https://github.com/user-attachments/assets/464d7f40-bb64-4ecf-a78d-743626ab0af9)
