# Hash-HashcatAdvancedUsage

## HASHING Hakkında Özet

### Hash Fonksiyonlarının Amacı
- **Hash fonksiyonları, veri bütünlüğünü doğrulamak için kullanılır.
- **Verinin değişmediğini ve bozulmadığını belirlemek için hash'ler kullanılır.

### Kullanım Alanları
- **Bütünlük Kontrolü: Dosyaların, yazıların veya resimlerin değiştirilip değiştirilmediğini belirlemek için kullanılır.
- **Parola Saklama: Veritabanlarında kullanıcı parolalarını güvenli bir şekilde saklamak için hash'ler kullanılır.
- 
### Güvenlik Önlemleri
- **Collision Attacks: Aynı hash'i üreten farklı verilerin bulunması için kullanılan saldırı türüdür.
- **Rainbow Tables: Önceden hesaplanmış hash'leri kullanarak verilen hash'in çözülmesi.
- **SALT: Parolaların hashlenirken eklenecek rastgele değerdir ve saldırganların önceden hesaplanmış hash'leri kullanmasını zorlaştırır.

### Hashing Algoritmaları
- **Hız ve Güvenlik Dengesi: Parola hash'lemek için hızlı algoritmalar uygun değildir. Yavaş algoritmalar daha güvenlidir.
- **Tavsiye Edilen Algoritmalar: bcrypt, pbkdf2, argon2 gibi yavaş algoritmalar önerilir.

### Örnekler

- **Bcrypt: Karmaşıklık seviyesini belirtmek için COST kullanılır.
- **SHA: SHA-1, SHA-256, ve SHA-512 gibi çeşitleri vardır.

### Güvenlik Önerileri
- **Parola hash'leme sürelerini artırmak, saldırganların hash cracking işlemlerini zorlaştırır.
- **Parola hash'leme sürelerini ayarlamak için bcrypt, pbkdf2, argon2 gibi yavaş algoritmalar kullanılmalıdır.
