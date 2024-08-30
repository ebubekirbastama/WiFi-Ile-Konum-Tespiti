# Wi-Fi ile Konum Tespiti

Bu proje, Wi-Fi sinyal gücü (RSSI) kullanarak yakındaki cihazların konumunu tahmin etmek için Python ile geliştirilmiştir. Konum belirleme, trilaterasyon yöntemiyle gerçekleştirilmektedir.

## Projenin Amacı

Yakındaki Wi-Fi cihazlarından alınan sinyal gücü (RSSI) değerleri ile bu cihazların muhtemel konumunu belirlemeyi amaçlamaktadır. Bu belirleme, trilaterasyon yöntemi kullanılarak yapılır.

## Kullanılan Teknolojiler ve Kütüphaneler

- **Python**
- **Scapy**: Wi-Fi paketlerini yakalamak için
- **SciPy**: Trilaterasyon hesaplamaları için optimize edilmiş matematiksel fonksiyonları içerir

## Nasıl Kullanılır?

### Kali Linux'ta ve Monitor Modunda Kullanım

1. Kali Linux üzerinde terminali açın.
2. Kablosuz kartınızı monitor moda alın:
    ```bash
    sudo ifconfig [interface] down
    sudo iwconfig [interface] mode monitor
    sudo ifconfig [interface] up
    ```
    Burada `[interface]` yerine kablosuz ağ adaptörünüzün adını yazmalısınız, genellikle `wlan0` veya `wlan1` şeklindedir.

3. Proje dosyasını bilgisayarınıza indirin.

4. Gerekli kütüphaneleri yüklemek için aşağıdaki komutu çalıştırın:
    ```bash
    pip install scapy scipy
    ```

5. `your_wifi_ssid` değişkenini kendi BSSID'nizle değiştirin. `apartment_x` ve `apartment_y` değişkenlerini kullanarak kendi konum bilginizi girin. `iface = "wlan1"` değişkenini kendi sistemlerinizdeki kablosuz ağ adaptörü adıyla değiştirin. Örneğin, bazı sistemlerde `wlan0` olabilir.

6. Kodu çalıştırın:
    ```bash
    sudo python dosya_adı.py
    ```
    (dosya_adı.py yerine kullandığınız dosya adını yazın)

## Trilaterasyonla Konum Tespiti

Bu proje, Wi-Fi sinyal gücü kullanarak yakındaki cihazların konumunu tahmin eder. Trilaterasyon yöntemiyle sinyal güçleri analiz edilerek cihazların muhtemel konumları belirlenir.

## İlgili Instagram Gönderisi

- [Trilaterasyonla Konum Tespiti](https://dergipark.org.tr/en/download/article-file/1133653)
- [İlgili Instagram Gönderisi](https://www.instagram.com/p/Cxgt-q4Ii-Z/?hl=tr)
## Lisans

Bu proje MIT lisansı altında yayınlanmıştır. Daha fazla detay için [LICENSE](LICENSE) dosyasına göz atabilirsiniz.

