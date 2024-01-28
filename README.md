# HTTP Request Methods

1. **GET (AL):**
   - Bilgi almak için kullanılır. Tarayıcı, sunucudan veri ister.
   - *Örnek:* Bir kullanıcı "https://testsite.com/test/123" adresine gittiğinde, tarayıcı bu URL üzerinden GET isteği gönderir ve sunucu 123 numaralı ürünle ilgili bilgileri geri gönderir.

2. **POST (GÖNDER):**
   - Sunucuya veri göndermek için kullanılır. Genellikle form bilgileri gibi verileri sunucuya iletmek için kullanılır.
   - *Örnek:* Kullanıcı bir giriş formunu doldurduğunda, bu bilgileri sunucuya göndermek için POST isteği kullanılır.

3. **PUT (GÜNCELLE):**
   - Bir kaynağı güncellemek veya eğer yoksa yeni bir kaynak oluşturmak için kullanılır.
   - *Örnek:* Bir kullanıcı profili güncellendiğinde veya yeni bir kullanıcı oluşturulduğunda PUT isteği kullanılabilir.

4. **PATCH (KISMİ GÜNCELLE):**
   - Genellikle bir kaynağın sadece belirli alanlarını güncellemek için kullanılır.
   - *Örnek:* Bir makalede sadece başlık veya kategori gibi belirli alanlar güncellenecekse PATCH isteği kullanılabilir.

5. **DELETE (SİL):**
   - Bir kaynağı silmek için kullanılır.
   - *Örnek:* Bir kullanıcı hesabı silindiğinde veya bir yorum kaldırıldığında DELETE isteği kullanılır.

6. **OPTIONS (SEÇENEKLER):**
   - Hedef kaynağın hangi HTTP metodlarını desteklediğini öğrenmek için kullanılır.
   - *Örnek:* Bir API'nin hangi metodları kabul ettiğini anlamak için OPTIONS isteği gönderilebilir.

7. **HEAD (BAŞLIK):**
   - GET isteği gibi, ancak sadece başlık bilgilerini alır, gerçek veriyi almadan.
   - *Örnek:* Bir dosyanın son güncellenme tarihini öğrenmek istediğinizde HEAD isteği kullanılabilir.

8. **TRACE (İZLE):**
   - İstemci ve sunucu arasındaki iletişimdeki değişiklikleri izlemek ve hata ayıklamak için kullanılır.
   - *Örnek:* Bir isteğin sunucu tarafında nasıl işlendiğini izlemek için TRACE isteği kullanılabilir.

9. **CONNECT (BAĞLAN):**
   - Güvenli bir bağlantı (SSL/TLS) kurmak için kullanılır.
   - *Örnek:* Tarayıcı, güvenli bir bağlantı kurmak için bir web sitesine CONNECT isteği gönderebilir.

---

# HTTP Status Codes

1. **1xx (Informational):**
   - **100 Continue:** İstemci, sunucuya bir parça veri gönderiyor ve işleme devam edebilir.
     - *Örnek:* İstemci, bir büyük dosyayı parça parça gönderir ve her parça için sunucu "100 Continue" durum kodu döner.

2. **2xx (Successful):**
   - **200 OK:** İstek başarıyla işlendi ve sunucu tarafından kabul edildi.
     - *Örnek:* Bir web sayfası başarıyla yüklendiğinde, sunucu "200 OK" durum kodu döner.

   - **201 Created:** İstek başarıyla işlendi ve yeni bir kaynak oluşturuldu.
     - *Örnek:* Bir kullanıcı yeni bir hesap oluşturduğunda, sunucu "201 Created" durum kodu döner.

   - **204 No Content:** İstek başarıyla işlendi, ancak sunucu bir içerik göndermiyor.
     - *Örnek:* Bir kaynağın güncellenmesi durumunda, sadece başarı bildirimi için "204 No Content" kullanılabilir.

3. **3xx (Redirection):**
   - **301 Moved Permanently:** Kaynak kalıcı olarak başka bir konuma taşındı.
     - *Örnek:* Bir sayfanın URL'si değiştiğinde ve kalıcı olarak yeni bir konuma taşındığında "301 Moved Permanently" durum kodu döner.

   - **302 Found:** Kaynak geçici olarak başka bir konuma taşındı.
     - *Örnek:* Bir sayfa güncellendiğinde ve yeni konum hala kesin değilse "302 Found" durum kodu kullanılabilir.

4. **4xx (Client Error):**
   - **400 Bad Request:** Sunucu, isteği anlamıyor veya işleyemiyor.
     - *Örnek:* İstemci, geçersiz bir form gönderdiğinde "400 Bad Request" durum kodu döner.

   - **401 Unauthorized:** İstek için kimlik doğrulaması gerekiyor.
     - *Örnek:* Kullanıcı giriş yapmadan güvenli bir kaynağa erişmeye çalıştığında "401 Unauthorized" durum kodu döner.

   - **404 Not Found:** İstek yapılan kaynak bulunamadı.
     - *Örnek:* Bir URL yanlış yazıldığında veya var olmayan bir kaynağa erişmeye çalışıldığında "404 Not Found" durum kodu döner.

5. **5xx (Server Error):**
   - **500 Internal Server Error:** Sunucu, bir isteği işlerken bir hata oluştu.
     - *Örnek:* Sunucu tarafında bir veritabanı hatası nedeniyle "500 Internal Server Error" durum kodu döner.

   - **503 Service Unavailable:** Sunucu geçici olarak hizmet veremiyor.
     - *Örnek:* Bakım nedeniyle geçici olarak sunucu hizmet dışıysa "503 Service Unavailable" durum kodu kullanılabilir.
