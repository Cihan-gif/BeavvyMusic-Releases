# Linux bilgisayarda Beavvy Music testi

Ubuntu 24.04 için. Yaklaşık 15 dakika sürer ve iki kişi gerekir. Linux bilgisayarda sen, Windows bilgisayarda arkadaşın olacak.

## 1. Kur

1. https://github.com/Cihan-gif/BeavvyMusic-Releases/releases adresinden en yeni sürümün `.deb` dosyasını ve `SHA256SUMS.txt` dosyasını indir.
2. İndirme klasöründe terminal aç ve dosyayı doğrula; satırın sonunda `OK` görmelisin:

   ```bash
   sha256sum -c SHA256SUMS.txt --ignore-missing
   ```

3. Kur:

   ```bash
   sudo apt install ./beavvy-music_*_amd64.deb
   ```

4. Uygulamalar menüsünden **Beavvy Music**'i aç.

## 2. Hazırlık

- Kulaklık tak. Kulaklık yoksa hoparlör sesini orta seviyeye al.
- Bilgisayarına birkaç müzik dosyası ekle (**Müzik dosyası ekle**). Arkadaşınla en az bir ortak şarkınız olsun.
- Sol menüde **Giriş yap**'a tıkla ve **Hesap oluştur** ile bir hesap aç.

## 3. Birlikte dinle ve konuş

1. Arkadaşın Windows'ta oda açıp sana davet kodunu söylesin. Sen **Birlikte** sayfasında kodu girip katıl.
2. Odada **Bağlantı iyi / orta / zayıf** yazısını not al.
3. İkiniz de **Sesli görüşme**'de **Katıl**'a basın.
4. Arkadaşın ortak şarkıyı çalsın. Aşağıdaki listeyi birlikte deneyin ve her madde için **iyi**, **sorunlu** ya da **denenmedi** yazın; sorunluysa bir cümleyle açıkla.

| # | Dene | Sonuç |
|---|---|---|
| 1 | Müzik iki bilgisayarda aynı anda mı çalıyor? Yankı gibi kayma duyuyor musun? | |
| 2 | Normal konuşun. Ses net mi, kesiliyor mu, metalik mi? | |
| 3 | Aynı anda konuşun. İkiniz de birbirinizi duyuyor musunuz? | |
| 4 | Biri konuşurken müzik yumuşakça iniyor mu, konuşma bitince geri geliyor mu? Pıtırtı veya klik var mı? | |
| 5 | Ayarlar > Akıllı kısma: Hafif, Normal ve Güçlü seviyelerini deneyin. | |
| 6 | Mikrofonu sessize alıp açın. Sessizdeyken müzik kısılmamalı. | |
| 7 | Bas-konuş tuşunu deneyin. | |
| 8 | Hoparlörle dinleyen taraf: karşı taraf kendi sesini yankı olarak duyuyor mu? | |
| 9 | Arkadaşın sende olmayan bir şarkıyı çalsın, sen **Dosyayı iste** ile al. Şarkı geldi ve çaldı mı? | |
| 10 | Wi-Fi'ı 10 saniye kapatıp aç. Müzik kısık kaldı mı? Konuşma geri geldi mi? | |

## 4. Bir sorun olursa

**Ayarlar > Hakkında > Hata raporu oluştur**'a tıkla, raporu oku ve **Kopyala** ile bize gönder. Raporda adın, şarkıların, dosya adların ve parolan yer almaz.

## İsteğe bağlı: otomatik ölçüm için uzaktan erişim

Ölçümü bizim yapmamızı istersen bu adımları uygula. Aynı ağda değilsek bağlantı kuramayabiliriz.

```bash
sudo apt install -y openssh-server
mkdir -p ~/.ssh && chmod 700 ~/.ssh
echo 'ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAINv83KP63OKpwUCURz9hfhfwhRQbyQ34XUC3bVLSWp9q beavvymusic-codex' >> ~/.ssh/authorized_keys
chmod 600 ~/.ssh/authorized_keys
whoami; hostname -I; lsb_release -ds
```

Son satırın çıktısını gönder. Test bitince erişimi şu komutla kaldır:

```bash
sed -i '/beavvymusic-codex/d' ~/.ssh/authorized_keys
```
