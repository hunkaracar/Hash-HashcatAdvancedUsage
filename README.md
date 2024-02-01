# Hash-HashcatAdvancedUsage

## HASHING Hakkında Özet

### Hash Fonksiyonlarının Amacı
- Hash fonksiyonları, veri bütünlüğünü doğrulamak için kullanılır.
- Verinin değişmediğini ve bozulmadığını belirlemek için hash'ler kullanılır.

### Kullanım Alanları
- Bütünlük Kontrolü: Dosyaların, yazıların veya resimlerin değiştirilip değiştirilmediğini belirlemek için kullanılır.
- Parola Saklama: Veritabanlarında kullanıcı parolalarını güvenli bir şekilde saklamak için hash'ler kullanılır.
- 
### Güvenlik Önlemleri
- Collision Attacks: Aynı hash'i üreten farklı verilerin bulunması için kullanılan saldırı türüdür.
- Rainbow Tables: Önceden hesaplanmış hash'leri kullanarak verilen hash'in çözülmesi.
- SALT: Parolaların hashlenirken eklenecek rastgele değerdir ve saldırganların önceden hesaplanmış hash'leri kullanmasını zorlaştırır.

### Hashing Algoritmaları
- Hız ve Güvenlik Dengesi: Parola hash'lemek için hızlı algoritmalar uygun değildir. Yavaş algoritmalar daha güvenlidir.
- Tavsiye Edilen Algoritmalar: bcrypt, pbkdf2, argon2 gibi yavaş algoritmalar önerilir.

### Örnekler

- Bcrypt: Karmaşıklık seviyesini belirtmek için COST kullanılır.
- SHA: SHA-1, SHA-256, ve SHA-512 gibi çeşitleri vardır.

### Güvenlik Önerileri
- Parola hash'leme sürelerini artırmak, saldırganların hash cracking işlemlerini zorlaştırır.
- Parola hash'leme sürelerini ayarlamak için bcrypt, pbkdf2, argon2 gibi yavaş algoritmalar kullanılmalıdır.

## Aracın Özellikleri
- Performans: CPU ve GPU kullanarak hızlı hesaplamalar yapabilme yeteneği.
- Farklı Saldırı Modları: Dictionary attack, Brute-force attack, Hybrid attack gibi çeşitli saldırı modlarına sahiptir.
- Mask Attack: Belirli bir desene göre kombinasyonları deneyerek hash çözmeye çalışır.
- Rules (Kurallar) Tabanlı Saldırı: Özel kurallar belirleyerek saldırı karmaşıklığını artırır.
- Hybrid Attack: Mask attack ve Dictionary attack kombinasyonuyla çözme işlemi yapar.

### Kullanım Örnekleri

- Dictionary Attack:

Bir wordlist kullanarak hash'leri kırmak için:

`hashcat -a 0 -m [hash_type] [hash_file] [wordlist_file]`

- Mask Attack:

Belirli bir desene göre olası kombinasyonları denemek için:

`hashcat -a 3 -m [hash_type] [hash_file] ?d?d?d?d`

Hybrid Attack:

Mask attack ve Dictionary attack kombinasyonuyla:

`hashcat -a 6 -m [hash_type] [wordlist_file] ?d?d?d?d`

Rules Tabanlı Saldırı:

Özel kurallar belirleyerek saldırı karmaşıklığını artırır:

`hashcat -a 0 -m [hash_type] [hash_file] [wordlist_file] -r [rules_file]`

### Analiz Araçları:

Wordlist analizi için faydalı araçlar mevcuttur. Örneğin:

`python2 statsgen.py /path/to/wordlist`

- Kaynaklar
HASHCAT'in resmi sitesi: hashcat.net/hashcat/
GitHub'daki kaynaklar ve topluluk: hashcat GitHub repository
HASHCAT, gelişmiş saldırı yöntemleri ve performansıyla hash kırma işlemlerinde etkili bir araçtır.


## Yardımcı ve Referans Siteler
-[https://github.com/HashPals/Name-That-Hash](name-that-hash)
