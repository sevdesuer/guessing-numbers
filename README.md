# guessing-numbers
The computer tries to guess the number you keep in mind between 1-100.

import random
enkucukdeger=1
enbuyukdeger=100
benimtahmin=print("Aklınızdan 1-100 arsaından bir sayı tutun.")
denemesayısı=0
while True:
    print("{}-{}arasında bir tahmin yapmalıyım".format(enkucukdeger,enbuyukdeger))
    bilgisayarıntahmini=random.randint(enkucukdeger,enbuyukdeger)
    cevap=input("{} tuttuğun sayı olabilir mi? \n doğruysa e yi \n daha büyükse b yi \n daha küçükse k yi tuşlayınız.".format(bilgisayarıntahmini))
    denemesayısı+=1
    if cevap=="e":
         print("Bilgisayar doğru tahminde bulundu")
         print("{} deneme sonunda doğru cevaba ulaştım!".format(denemesayısı))
         break
    elif cevap=="b":
         print("Daha büyük bir sayı denemeliyim.")
         enkucukdeger=bilgisayarıntahmini+1
    elif cevap=="k":
         print("Daha küçük bir sayı denemeliyim.")
         enbuyukdeger=bilgisayarıntahmini-1
