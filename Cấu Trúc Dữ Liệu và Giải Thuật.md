# Cấu Trúc Dữ Liệu và Giải Thuật

## 1. 📦 Cấu Trúc Dữ Liệu Cơ Bản

### Tuyến tính (Linear)
- **Mảng (Array)** – truy cập O(1), tìm kiếm O(n)
- **Danh sách liên kết (Linked List)** – đơn, đôi, vòng
- **Ngăn xếp (Stack)** – LIFO
- **Hàng đợi (Queue)** – FIFO, Deque, Priority Queue

### Phi tuyến (Non-linear)
- **Cây (Tree)** – nhị phân, BST, AVL, B-Tree, Heap, Trie
- **Đồ thị (Graph)** – có/không có hướng, có/không có trọng số
- **Bảng băm (Hash Table)** – ánh xạ key-value

## 2. 🔍 Giải Thuật Tìm Kiếm

| Giải thuật | Độ phức tạp | Ghi chú |
| --- | --- | --- |
| Tìm tuần tự | O(n) | Mảng bất kỳ |
| Tìm nhị phân | O(log n) | Mảng đã sắp xếp |
| BFS | O(V+E) | Đồ thị/cây |
| DFS | O(V+E) | Đồ thị/cây |

## 3. 🔢 Giải Thuật Sắp Xếp

| Giải thuật | Tốt nhất | Trung bình | Xấu nhất | Ổn định |
| --- | --- | --- | --- | --- |
| Bubble Sort | O(n) | O(n²) | O(n²) | ✅ |
| Selection Sort | O(n²) | O(n²) | O(n²) | ❌ |
| Insertion Sort | O(n) | O(n²) | O(n²) | ✅ |
| Merge Sort | O(n log n) | O(n log n) | O(n log n) | ✅ |
| Quick Sort | O(n log n) | O(n log n) | O(n²) | ❌ |
| Heap Sort | O(n log n) | O(n log n) | O(n log n) | ❌ |

## 4. 🧠 Kỹ Thuật Thiết Kế Giải Thuật

- **Chia để trị (Divide & Conquer)** – Merge Sort, Quick Sort
- **Quy hoạch động (Dynamic Programming)** – Fibonacci, Knapsack, LCS, LIS
- **Tham lam (Greedy)** – Dijkstra, Huffman, Kruskal
- **Quay lui (Backtracking)** – N-Queens, Sudoku, tập con
- **Đệ quy (Recursion)** – nền tảng nhiều giải thuật

## 5. 🌐 Giải Thuật Đồ Thị

- **BFS, DFS** – duyệt đồ thị
- **Dijkstra, Bellman-Ford** – đường đi ngắn nhất
- **Floyd-Warshall** – mọi cặp đỉnh
- **Kruskal, Prim** – cây khung nhỏ nhất (MST)
- **Topological Sort** – đồ thị có hướng không chu trình (DAG)
- **Kiểm tra chu trình, liên thông**

## 6. 📊 Độ Phức Tạp Thuật Toán (Algorithm Complexity)

Độ phức tạp thuật toán đánh giá hiệu năng của một thuật toán dựa trên hai yếu tố chính: **Thời gian (Time Complexity)** và **Không gian bộ nhớ (Space Complexity)** khi kích thước dữ liệu đầu vào (n) tăng lên.

### Ký hiệu Big-O (Độ phức tạp trường hợp xấu nhất)
Dùng để mô tả *mức tăng trưởng tối đa* của thuật toán. Các độ phức tạp phổ biến từ tốt nhất đến xấu nhất:

1. **O(1) - Hằng số (Constant):** Thời gian thực thi không đổi, bất kể kích thước dữ liệu. *VD: Truy cập phần tử mảng theo mảng chỉ mục, phép toán cơ bản.*
2. **O(log n) - Logarit (Logarithmic):** Thời gian thực thi tăng theo logarit của kích thước dữ liệu. Rất hiệu quả cho dữ liệu lớn. *VD: Tìm kiếm nhị phân (Binary Search).*
3. **O(n) - Tuyến tính (Linear):** Thời gian thực thi tăng tỉ lệ thuận với kích thước dữ liệu. *VD: Duyệt qua một mảng (vòng lặp for đơn).*
4. **O(n log n) - Tuyến tính logarit (Linearithmic):** Thường gặp trong các thuật toán chia để trị tối ưu. *VD: Merge Sort, Quick Sort, Heap Sort.*
5. **O(n²) - Đa thức bậc 2 (Quadratic):** Bắt đầu chậm khi n lớn. Thường là 2 vòng lặp lồng nhau. *VD: Bubble Sort, Selection Sort, Insertion Sort.*
6. **O(2ⁿ) - Mũ (Exponential):** Rất chậm, tốc độ tăng khủng khiếp, chỉ dùng cho n rất nhỏ. *VD: Tính Fibonacci bằng đệ quy không nhớ (naive recursion), bài toán Tháp Hà Nội.*
7. **O(n!) - Giai thừa (Factorial):** Thuật toán chậm nhất. *VD: Sinh các hoán vị của một tập hợp, bài toán Người chào hàng (vét cạn).*

### Phân tích thời gian (Time Complexity)
Đánh giá **số lượng phép toán** cơ bản thuật toán phải thực hiện.
- **Cách phân tích cơ bản:**
  - Gán, in, tính toán cơ bản: `O(1)`
  - Vòng lặp `for` từ 1 đến n: `O(n)`
  - Vòng lặp lồng nhau: `O(n * m)` (nếu giới hạn là n và m) hoặc `O(n²)` (nếu cả hai là n).
  - Khối lệnh IF-ELSE: Lấy độ phức tạp của khối tốn thời gian lớn hơn lớn nhất (nhánh xấu nhất).
- *Lưu ý:* Bỏ qua hằng số và các bậc thấp hơn. VD: `O(2n² + 5n + 10)` sẽ được rút gọn thành `O(n²)`.

### Phân tích không gian (Space Complexity)
Đánh giá **lượng bộ nhớ bổ sung** mà thuật toán cần để chạy, không tính bộ nhớ lưu trữ đầu vào.
- **O(1):** Thuật toán chỉ dùng một vài biến phụ. *VD: Bubble Sort, Selection Sort (sắp xếp tại chỗ - In-place sorting).*
- **O(n):** Thuật toán cần cấp phát thêm bộ nhớ tỉ lệ với n. *VD: Cần tạo một mảng mới kích thước n, hoặc dùng đệ quy sâu n tầng (gây tốn Stack).*
- **O(n²):** Ví dụ như tạo một ma trận 2 chiều `n x n`.

## 7. 🗂️ Các Chủ Đề Nâng Cao

- **Segment Tree, Fenwick Tree (BIT)**
- **Union-Find (Disjoint Set)**
- **Suffix Array, KMP, Rabin-Karp** (xử lý chuỗi)
- **Red-Black Tree, Splay Tree**
- **A*** (tìm đường thông minh)