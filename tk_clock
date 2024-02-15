import tkinter as tk
import datetime

root = tk.Tk()
root.title("時計")
root.geometry("340x200")

time_font = "DSEG14 Classic-Light" # 使用するフォント

canvas = tk.Canvas(root, width=340, height=200, bg="black")
canvas.pack()

def update_time():

    canvas.delete("time")

    time = datetime.datetime.now()
    
    hour = format(time.hour, "02")
    minute = format(time.minute, "02")
    second = format(time.second, "02")

    display_time = hour + " : " + minute + " : " + second

    canvas.create_text(165, 120, text=display_time, tag="time", fill="white", font=(time_font, 40))

    root.after(1000, update_time)

def update_date():

    canvas.delete("date")

    time = datetime.datetime.now()

    display_date = format(time, "%Y/%m/%d")

    canvas.create_text(115, 60, text=display_date, tag="date", fill="white", font=(time_font, 20))

    root.after(1000, update_date)

update_time()
update_date()

root.mainloop()
