### ATM Uygulaması README

Bu doküman, ATM uygulamasının nasıl çalıştığını ve işlevlerini açıklamaktadır. Uygulama, kullanıcıların sanal bir ATM üzerinden bakiye görüntüleme, para yatırma, para çekme işlemlerini gerçekleştirmelerine olanak sağlar.

---

### Çalışma Şekli

Uygulama, bir `ATM` sınıfı ve `atm_menu()` fonksiyonu üzerinden çalışmaktadır. Kullanıcı, belirli seçenekleri seçerek ATM işlemlerini gerçekleştirebilir.

---

### Sınıf ve Fonksiyonlar

#### **ATM Sınıfı**
ATM sınıfı, bir kullanıcının bakiyesini yönetmek için aşağıdaki özelliklere sahiptir:

- **`__init__(balance=1000)`**  
  ATM nesnesi oluşturulurken varsayılan olarak 1000 TL bakiye ile başlar. İstenirse başlangıç bakiyesi değiştirilebilir.

- **`display_balance()`**  
  Kullanıcının mevcut bakiyesini ekrana yazdırır.

- **`deposit(amount)`**  
  Kullanıcının belirttiği miktarda para yatırmasını sağlar. Negatif bir miktar girilirse işlem reddedilir.

- **`withdraw(amount)`**  
  Kullanıcının belirttiği miktarda para çekmesini sağlar.  
  - Eğer bakiye yetersizse, kullanıcıya uyarı verir.  
  - Negatif bir miktar girilirse işlem reddedilir.

#### **atm_menu() Fonksiyonu**
Bu fonksiyon, kullanıcı arayüzünü sağlar ve aşağıdaki işlemleri içerir:

1. **Bakiye Görüntüle**  
   Kullanıcının mevcut bakiyesini görüntüler.

2. **Para Yatır**  
   Kullanıcının hesabına para yatırmasını sağlar.

3. **Para Çek**  
   Kullanıcının hesabından para çekmesini sağlar.

4. **Çıkış**  
   Kullanıcının işlemi sonlandırmasını sağlar.

Kullanıcı, menüde belirtilen seçeneklerden birini seçerek işlemlerini yapabilir.

---

### Kullanım Talimatları

1. **Başlatma**  
   Uygulama başlatıldığında `atm_menu()` fonksiyonu çağrılır ve bir menü görüntülenir.

2. **Seçim Yapma**  
   Kullanıcı, `1`, `2`, `3`, `4` seçeneklerinden birini seçerek işlemini yapar.

3. **Bakiye Kontrolü**  
   Seçeneklerden `1` seçildiğinde mevcut bakiye ekranda görüntülenir.

4. **Para Yatırma**  
   Seçeneklerden `2` seçildiğinde kullanıcıdan bir miktar girmesi istenir.  
   - Geçerli bir miktar girilirse bakiye güncellenir ve bilgi mesajı görüntülenir.  
   - Geçersiz bir miktar girilirse kullanıcı uyarılır.

5. **Para Çekme**  
   Seçeneklerden `3` seçildiğinde kullanıcıdan bir miktar girmesi istenir.  
   - Geçerli bir miktar ve bakiye yeterli ise para çekilir.  
   - Yetersiz bakiye durumunda veya geçersiz miktar girilirse kullanıcıya uyarı mesajı verilir.

6. **Çıkış Yapma**  
   Seçeneklerden `4` seçildiğinde program sonlandırılır.

---

### Gereksinimler

Bu uygulama herhangi bir harici kütüphane gerektirmez ve Python 3.6 veya daha üstü sürümlerde çalıştırılabilir.

---

### Örnek Kullanım

1. **Menü Görüntüleme**
   ```
   ATM İşlemleri:
   1. Bakiye Görüntüle
   2. Para Yatir
   3. Para Çek
   4. Çikiş
   ```

2. **Seçim Yapma**
   Kullanıcı örneğin `1` seçerek bakiyesini görüntüleyebilir.

3. **Sonuç**
   ```
   Mevcut Bakiye: 1000 TL
   ```

---

### Notlar

- Negatif miktarlarla yapılan işlemler geçersizdir.
- Bakiye yetersizse, para çekme işlemi gerçekleştirilemez.
- Programdan çıkış yapmak için `4` seçeneği kullanılmalıdır.
