import qrcode
import random
import string
from datetime import date

def generator_qr():
    qr = qrcode.QRCode(version=1,
                       error_correction=qrcode.constants.ERROR_CORRECT_L,
                       box_size=50,
                       border=input("Wybierz szerokosc ramki: "))

    qr.add_data(input('Wprowadz tekst: '))

    img = qr.make_image(fill_color=input("Wybierz kolor szlaczkow: "), back_color=input("Wybierz kolor tla: "))
    id = ''.join(random.choices(string.ascii_uppercase + string.digits, k=6))
    img.save(f"qrcody/{str(date.today()) + ' ' + id}.png")

while True:
    print("Witaj w kreatorze QR kodów!\nSpersonalizuj swoja wiadomosc.\n-------------------------")
    generator_qr()
    wybor = input("Chcesz stworzyc jeszcze jeden QRcode?(n/y)")
    if wybor == 'n':
        break

