import tkinter as tk
    # Dibuja el tallo verde
    canvas.create_line(100, 300, 100, 200, fill="green", width=5)
    for i in range(12):
        angle = i * (360 / 12)  # Ángulo entre pétalos
        x = 100 + 50 * (1 if i % 2 == 0 else 0.7) * (2 * angle)
        y = 200 - 50 * (1 if i % 2 == 0 else 0.7) * (2 * angle)
        canvas.create_oval(x - 20, y - 20, x + 20, y + 20, fill="yellow")
ventana = tk.Tk()
ventana.title("Flor Amarilla")
lienzo = tk.Canvas(ventana, width=200, height=400)
lienzo.pack()
dibujar_flor(lienzo)
ventana.mainloop()
