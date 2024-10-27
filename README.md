import tkinter as tk
from tkinter import messagebox

# إنشاء نافذة التطبيق
window = tk.Tk()
window.title("واجهة مستخدم بسيطة")
window.geometry("400x200")

# دالة عند الضغط على الزر
def say_hello():
    user_name = entry_name.get()
    if user_name:
        messagebox.showinfo("مرحبًا!", f"مرحبًا، {user_name}!")
    else:
        messagebox.showwarning("تحذير", "الرجاء إدخال اسمك.")

# إضافة تسمية
label = tk.Label(window, text="الرجاء إدخال اسمك:", font=("Arial", 12))
label.pack(pady=10)

# إضافة حقل إدخال
entry_name = tk.Entry(window, font=("Arial", 12))
entry_name.pack(pady=5)

# إضافة زر
button = tk.Button(window, text="قل مرحبًا", command=say_hello, font=("Arial", 12))
button.pack(pady=10)

# بدء التطبيق
window.mainloop()
