# Beavvy Music

Kendi müziğini internetsiz dinle; istediğinde bir arkadaşınla aynı şarkıyı aynı anda çal ve konuş.

Bu depo yalnız derlenmiş kurulum paketlerini içerir. Paketler [Releases](../../releases) sayfasındadır.

## Kurulum

- **Windows 10/11 (64 bit):** `BeavvyMusic-Setup-…-win-x64.exe` dosyasını çalıştır. Yönetici izni istemez. SmartScreen uyarısı çıkarsa "Ek bilgi" ve "Yine de çalıştır" seçeneklerini kullan; paket henüz kod imzalı değil.
- **Ubuntu 24.04:** `sudo apt install ./beavvy-music_…_amd64.deb`
- **Android 7 ve üstü (arm64):** `BeavvyMusic-…-android-arm64.apk` dosyasını indirip aç. Bilinmeyen kaynaklardan yüklemeye izin vermen istenebilir.

Her sürümde `SHA256SUMS.txt` bulunur. İndirdiğin dosyayı doğrulamak için:

- Windows: `Get-FileHash .\dosya -Algorithm SHA256`
- Linux: `sha256sum -c SHA256SUMS.txt --ignore-missing`

Üçüncü taraf bileşenlerin lisansları her sürümdeki `THIRD_PARTY_NOTICES.md` dosyasındadır.

## Test

İki kişilik Linux ve ses testi adımları: [LINUX_TEST.md](LINUX_TEST.md)
