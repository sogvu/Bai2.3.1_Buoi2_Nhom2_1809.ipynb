# Bai2.3.1_Buoi-2_Nhom9_CNTT1809.ipynb

# - Trong thư viện có 10 quyển sách về lịch sử và 12 quyển sách về khoa học. Nếu bạn muốn mượn một quyển sách, bạn có bao nhiêu lựa chọn?
so_sach_lich_su = 10
so_sach_khoa_hoc = 12
tong_so_lua_chon_sach = so_sach_lich_su + so_sach_khoa_hoc
print(f"Tổng số lựa chọn để mượn một quyển sách là: {tong_so_lua_chon_sach} lựa chọn.")
# Lý giải: Áp dụng quy tắc cộng. Vì  chỉ mượn MỘT quyển sách,  có thể chọn sách lịch sử HOẶC sách khoa học. Số cách chọn là tổng số sách lịch sử và sách khoa học.

# - Một quán cà phê có 3 loại cà phê (đen, sữa, bạc xỉu) và 4 loại bánh ngọt. Nếu bạn muốn chọn 1 loại cà phê và 1 loại bánh ngọt, bạn có bao nhiêu cách chọn?
so_loai_ca_phe = 3
so_loai_banh_ngot = 4
tong_so_cach_chon = so_loai_ca_phe * so_loai_banh_ngot
print(f"Tổng số cách chọn 3 loại cà phê là: {tong_so_cach_chon} cách.")
# Lý giải: Áp dụng quy tắc nhân.  cần chọn 1 loại cà phê VÀ 1 loại bánh ngọt. Số cách chọn là tích số loại cà phê và số loại bánh ngọt.

# 2.3.3 - Dãy Fibonacci

# Phương pháp 1: Lặp (Iterative)
def tinh_fibonacci_lap(n):
    """
    Hàm tính số Fibonacci thứ n bằng phương pháp lặp.
    """
    if n <= 0:
        return 0
    elif n == 1:
        return 1
    else:
        a, b = 0, 1
        for _ in range(2, n + 1):
            a, b = b, a + b
        return b

print("--- Tính Fibonacci bằng phương pháp LẶP ---")
so_can_tinh = [0, 1, 2, 3, 4, 5, 6, 10]
for n in so_can_tinh:
    print(f"Fibonacci thứ {n} là: {tinh_fibonacci_lap(n)}")


# Phương pháp 2: Đệ quy (Recursive)
def tinh_fibonacci_de_quy(n):
    """
    Hàm tính số Fibonacci thứ n bằng phương pháp đệ quy.
    """
    if n <= 0:
        return 0
    elif n == 1:
        return 1
    else:
        return tinh_fibonacci_de_quy(n-1) + tinh_fibonacci_de_quy(n-2)

print("\n--- Tính Fibonacci bằng phương pháp ĐỆ QUY ---")
for n in so_can_tinh:
    print(f"Fibonacci thứ {n} là: {tinh_fibonacci_de_quy(n)}")

print("\nDãy Fibonacci chuẩn (từ F0 đến F6): 0, 1, 1, 2, 3, 5, 8")


print("--- Bài toán 1: Câu lạc bộ thể thao ---")
tong_thanh_vien = 40
choi_bong_chuyen = 25
choi_cau_long = 18
choi_ca_hai = 10

# a) Số thành viên chơi ít nhất một trong hai môn
# Áp dụng công thức: |A hợp B| = |A| + |B| - |A giao B|
choi_it_nhat_mot_mon = choi_bong_chuyen + choi_cau_long - choi_ca_hai
print(f"Số thành viên chơi ít nhất một trong hai môn là: {choi_it_nhat_mot_mon} người.")

# b) Số thành viên không chơi môn nào
# Áp dụng công thức: Tổng số thành viên - Số thành viên chơi ít nhất một môn
khong_choi_mon_nao = tong_thanh_vien - choi_it_nhat_mot_mon
print(f"Số thành viên không chơi môn nào trong hai môn là: {khong_choi_mon_ao} người.")

# Bài toán 2: Bức ảnh
print("\n--- Bài toán 2: Bức ảnh ---")
tong_buc_anh = 50
co_nguoi = 30
co_canh_dep = 20
co_nguoi_va_canh_dep = 10

# Số bức ảnh có ít nhất một trong hai yếu tố
# Áp dụng công thức: |A hợp B| = |A| + |B| - |A giao B|
co_it_nhat_mot_yeu_to = co_nguoi + co_canh_dep - co_nguoi_va_canh_dep
print(f"Số bức ảnh có ít nhất một trong hai yếu tố (người hoặc đẹp) là: {co_it_nhat_mot_yeu_to} bức ảnh.")
