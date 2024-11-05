# Born2reboot

- [Sanal Makinelerin Temel İşlevi](#sanal-makinelerin-temel-islevi)
   - [Sanal Makinelerin Faydaları](#sanal-makinelerin-faydaları)
   - [Debian](#debian)
    
    - [Genel Bilgiler](#genel-bilgiler)
    - [Sürümler](#sürümler)
    - [Paket Yönetimi](#paket-yönetimi)
    - [Özellikler](#özellikler)
    - [Kullanım Alanları](#kullanım-alanları)
    - [İlgili Projeler](#ilgili-projeler)
    - [Rocky ve Debian Arasındaki Temel Farklar](#rocky-ve-debian-arasındaki-temel-farklar)

- [Aptitude ve Apt](#aptitude-ve-apt)
   
   - [Aptitude](#aptitude)
   - [Apt](#apt)
   - [Aptitude vs Apt](#aptitude-vs-apt)
 

- [AppArmor](#apparmor)

- [UFW ve SSH](ufw-ve-ssh)

  - [UFW (Uncomplicated Firewall)](#ufw-(uncomplicated-firewall))
  - [SSH (Secure Shell)](#ssh-(secure-shell))
  - [SSH ve UFW İlişkisi](#ssh-ve-ufw-ilişkisi)
 
- [Yeni Kullanıcı ve Grup Oluşturma](#yeni-kullanıcı-ve-grup-oluşturma)

- [Güçlü Parola Oluşturma ve Politikaları](#güçlü-parola-oluşturma-ve-politikaları)

- [LVM (Logical Volume Manager)](#lvm-(logical-volume-manager))

- [SUDO (Superuser Do)](#sudo-(superuser-do))

- [CRON](#cron)

- [Lighttpd](#lighttpd)

- [MariaDB](#mariadb)

- [PHP](#php)

- [WordPress](#wordpress)


-[Debian 10 Kurulum ve Yapılandırma Rehberi](#debian-10-kurulum-ve-yapılandırma-rehberi)



  
## Sanal Makinelerin Temel Islevi

Sanal makinelerin temel işlevi, fiziksel bir bilgisayarda veya sunucuda çalışan yazılımları, işletim sistemlerini ve uygulamaları izole bir ortamda çalıştırmaktır. Bu sayede farklı işletim sistemleri ve yazılımlar, aynı fiziksel donanım üzerinde paralel olarak çalışabilir. 

Sanal makineler, kaynakları daha verimli kullanmayı, test ve geliştirme ortamları oluşturmayı, sistemleri izole etmeyi ve yedekleme/geri yükleme işlemlerini kolaylaştırmayı sağlar. Ayrıca, bulut bilişim hizmetlerinde de yaygın olarak kullanılırlar.

## Debian

### Genel Bilgiler

- **Kuruluş**: Debian projesi, 1993 yılında Ian Murdock tarafından başlatılmıştır. Proje, özgür yazılım ve açık kaynaklı yazılımlar geliştirmeyi teşvik etmek amacıyla kurulmuştur.
- **Yönetim**: Debian, bir topluluk tarafından yönetilmektedir ve yazılımlar genellikle gönüllü geliştiriciler tarafından sağlanmaktadır.

### Sürümler

Debian, üç ana sürüm sunar:

1. **Stable (Kararlı)**: En son test edilmiş ve güvenli bir şekilde kullanılabilir olan sürümdür. Genellikle sunucular ve kurumsal ortamlar için önerilir.
2. **Testing (Test)**: Stabil sürüm için bekleyen güncellemeleri içerir. Stabil sürümden daha yeni paketleri barındırır, ancak daha az test edilmiştir.
3. **Unstable (Kararsız)**: En son geliştirmeleri ve yazılım paketlerini içeren sürümdür. Genellikle geliştiriciler ve deneysel kullanıcılar tarafından kullanılır.

### Paket Yönetimi

- **APT (Advanced Package Tool)**: Debian'ın paket yönetim sistemi olup, yazılım paketlerini yüklemek, güncellemek ve kaldırmak için kullanılır. APT, kullanıcıların yazılım depolarıyla etkileşimde bulunmasını sağlar.
- **DEB Paket Formatı**: Debian, yazılımları dağıtmak için DEB formatını kullanır. Bu format, bağımlılıkları ve kurulum süreçlerini yönetmek için gerekli bilgileri içerir.

### Özellikler

- **Güvenlik**: Debian, güvenlik güncellemeleri için düzenli olarak destek sağlar. Özellikle sunucu ortamlarında güvenlik, ön planda tutulmaktadır.
- **Esneklik**: Farklı masaüstü ortamları (GNOME, KDE, Xfce, vb.) ve çeşitli uygulama setleri ile özelleştirilebilir. Kullanıcılar kendi ihtiyaçlarına uygun yapılandırmalar oluşturabilir.
- **Topluluk Desteği**: Geniş bir topluluk tarafından desteklenir. Kullanıcılar, forumlar, belgeler ve sosyal medya aracılığıyla yardım alabilirler.

### Kullanım Alanları

- **Sunucular**: Debian, kararlılığı ve güvenliği nedeniyle yaygın olarak sunucu ortamlarında tercih edilir.
- **Masaüstü**: Kullanıcı dostu masaüstü ortamları ile masaüstü bilgisayarlar için de uygundur.
- **Geliştirme**: Yazılım geliştirme için güçlü bir platform sunar ve birçok geliştirici tarafından kullanılır.

### İlgili Projeler

- **Debian GNU/Linux**: Debian'ın en yaygın dağıtımıdır ve Linux çekirdeği ile birlikte gelir.
- **Debian Med**: Tıbbi ve biyolojik yazılımlar için özel bir Debian bileşenidir.
- **Debian Edu**: Eğitim alanında kullanılmak üzere özel olarak tasarlanmış bir sürümdür.

Debian, güçlü topluluğu, esnekliği ve güvenliği ile popüler bir Linux dağıtımıdır ve hem bireysel kullanıcılar hem de kurumsal ortamlar için çeşitli kullanım senaryolarına uygundur.

## Rocky ve Debian Arasındaki Temel Farklar

| Özellik              | Rocky Linux                              | Debian                                  |
|----------------------|------------------------------------------|-----------------------------------------|
| **Temel Amaç**        | Red Hat Enterprise Linux (RHEL) ile uyumlu bir açık kaynak alternatifi sağlamak | Genel amaçlı, güvenlik ve özgür yazılım odaklı |
| **Paket Yönetimi**    | RPM (Red Hat Package Manager) ve DNF     | DEB paket formatı ve APT                |
| **Sürümler ve Destek** | Uzun vadeli destek, RHEL ile aynı yaşam döngüsü | Stable, testing ve unstable sürümleri ile sürekli güncelleme |
| **Topluluk ve Geliştirme** | Kurumsal odaklı, Rocky Enterprise Software Foundation tarafından geliştirilir | Geniş bir gönüllü topluluğu tarafından yönetilir |
| **Özelleştirme ve Kullanıcı Deneyimi** | Daha çok kurumsal yazılımlara ve hizmetlere odaklanır | Daha fazla özelleştirme seçeneği ve masaüstü ortamı sunar |

## Sanal Makinelerin Faydaları

Sanal makinelerin birçok faydası vardır, işte bazıları:

1. **Kaynak Verimliliği**: Fiziksel donanımın daha verimli kullanılmasını sağlar. Birden fazla sanal makine, tek bir fiziksel sunucuda çalışabilir.
2. **İzolasyon**: Uygulamalar ve sistemler birbirinden izole bir şekilde çalışır. Bu, bir sanal makinedeki hataların diğerlerini etkilemesini önler.
3. **Test ve Geliştirme**: Yazılım geliştirme ve test süreçlerinde, farklı işletim sistemleri ve yapılandırmalar üzerinde denemeler yapmak için ideal bir ortam sunar.
4. **Kolay Yönetim ve Yedekleme**: Sanal makineler, anlık görüntü (snapshot) alma ve yedekleme işlemlerini kolaylaştırır. Bu sayede sistem geri yüklemeleri hızlıca yapılabilir.
5. **Taşınabilirlik**: Sanal makineler, bir donanım platformundan diğerine kolayca taşınabilir. Bu, bulut ortamlarında ve veri merkezlerinde büyük bir avantajdır.
6. **Hızlı Dağıtım**: Yeni sanal makineler hızla oluşturulabilir, bu da altyapının hızlı bir şekilde ölçeklenmesine olanak tanır.
7. **Güvenlik**: İzolasyon sayesinde, sanal makineler güvenlik tehditlerine karşı daha dayanıklıdır. Ayrıca, farklı güvenlik politikaları ve yapılandırmalar uygulanabilir.
8. **Çeşitli Ortamlar**: Farklı işletim sistemleri ve yazılım kombinasyonlarını test etmek için esneklik sağlar. Örneğin, Linux ve Windows ortamlarını aynı fiziksel makinede çalıştırmak mümkündür.



# Aptitude ve Apt

## Aptitude

**Aptitude**, Debian tabanlı sistemlerde paket yönetimi için kullanılan bir araçtır. Özellikleri şunlardır:

- **Kullanıcı Arayüzü**: Hem komut satırı hem de ncurses tabanlı bir kullanıcı arayüzü sunar. Bu, kullanıcıların paketleri daha görsel bir şekilde yönetmesine olanak tanır.
- **Gelişmiş Bağımlılık Yönetimi**: Bağımlılık sorunlarını çözmek için daha karmaşık algoritmalar kullanır. Bu, paketlerin kurulum ve kaldırma işlemlerinde daha iyi bir yönetim sağlar.
- **Yardımcı Araçlar**: Kullanıcılara, hangi paketlerin kurulu olduğunu, hangi paketlerin güncellenmesi gerektiğini ve hangi bağımlılıkların bulunduğunu gösteren detaylı bilgiler sunar.
- **Profil Tabanlı Yönetim**: Uygulamalar için belirli kurallar ve profiller oluşturma yeteneği ile daha özelleştirilebilir bir yönetim deneyimi sağlar.
- **Geri Alma Özelliği**: Hatalı bir güncelleme veya kurulum durumunda geri alma seçenekleri sunar.

### Aptitude Komutları

1. **Paket Güncelleme**:
    ```bash
    sudo aptitude update
    ```

2. **Paket Yükleme**:
    ```bash
    sudo aptitude install paket_adı
    ```

3. **Paket Kaldırma**:
    ```bash
    sudo aptitude remove paket_adı
    ```

4. **Paket Güncelleme**:
    ```bash
    sudo aptitude upgrade
    ```

5. **Sistem Güncellemesi (Tüm paketleri günceller)**:
    ```bash
    sudo aptitude full-upgrade
    ```

6. **Paket Bilgisi Görüntüleme**:
    ```bash
    aptitude show paket_adı
    ```

7. **Bağımlılıkları Temizleme**:
    ```bash
    sudo aptitude purge paket_adı
    ```

8. **Tüm Yüklü Paketlerin Listesi**:
    ```bash
    aptitude search '~i'
    ```

---

## Apt

**Apt**, Debian ve Ubuntu tabanlı sistemlerde kullanılan bir paket yönetim aracıdır. Temel özellikleri şunlardır:

- **Basit Komutlar**: Temel paket yönetim görevleri için kolay anlaşılır komutlar sunar. Örneğin, `apt install`, `apt remove`, `apt update` gibi komutlar ile hızlıca işlemler gerçekleştirilebilir.
- **Paket Deposu Yönetimi**: Sistem üzerinde kurulu olan paketlerin güncellemelerini kontrol etmek ve yüklemek için kullanılır. Depolardaki paketlerle etkileşim sağlar.
- **Otomatik Bağımlılık Çözümü**: Kurulum sırasında bağımlılıkları otomatik olarak yönetir. Ancak bazı durumlarda bağımlılık sorunlarıyla karşılaşabilir.
- **Hızlı ve Etkili**: Komut satırında hızlıca işlem yapma imkanı sunar. Kullanıcıların ihtiyacına göre komutları hızlı bir şekilde çalıştırmasını sağlar.
- **Özelleştirme ve Uzantılar**: Temel işlevlerin yanı sıra, kullanıcıların ihtiyaçlarına göre daha fazla özelleştirme yapma imkanı sunar.

### Apt Komutları

1. **Paket Güncelleme**:
    ```bash
    sudo apt update
    ```

2. **Paket Yükleme**:
    ```bash
    sudo apt install paket_adı
    ```

3. **Paket Kaldırma**:
    ```bash
    sudo apt remove paket_adı
    ```

4. **Paket Güncelleme**:
    ```bash
    sudo apt upgrade
    ```

5. **Sistem Güncellemesi (Tüm paketleri günceller)**:
    ```bash
    sudo apt full-upgrade
    ```

6. **Paket Bilgisi Görüntüleme**:
    ```bash
    apt show paket_adı
    ```

7. **Bağımlılıkları Temizleme**:
    ```bash
    sudo apt purge paket_adı
    ```

8. **Tüm Yüklü Paketlerin Listesi**:
    ```bash
    apt list --installed
    ```

---

## Aptitude vs Apt

| Özellik                      | **Apt**                                     | **Aptitude**                                |
|------------------------------|---------------------------------------------|---------------------------------------------|
| **Kullanım Kolaylığı**        | Daha basit ve doğrudan bir komut satırı aracıdır. Temel paket yönetim görevleri için hızlıca kullanılır. | Daha zengin bir kullanıcı arayüzü sunar. Hem komut satırı hem de ncurses tabanlı bir arayüz sağlar. |
| **Paket Çözümleme**           | Paket bağımlılıklarını otomatik olarak çözebilir, ancak bazen bağımlılık sorunlarıyla karşılaşabilir. | Daha gelişmiş bağımlılık çözümleme algoritmalarına sahiptir ve bağımlılık çatışmalarını daha iyi yönetir. |
| **Yönetim Özellikleri**       | Temel paket yönetim işlevlerine odaklanır. | Kullanıcıya daha fazla seçenek sunar; örneğin, hangi paketlerin neden kurulu olduğunu gösterme, farklı sürümleri seçme gibi ek işlevler sağlar. |




# AppArmor

**AppArmor**, Linux tabanlı sistemlerde güvenlik sağlamak için kullanılan bir güvenlik modülüdür. Temel özellikleri şunlardır:

1. **Zorunlu Erişim Kontrolü (MAC)**: Uygulamaların sistem kaynaklarına erişimlerini kısıtlamak için kurallar oluşturur. Bu, uygulamaların yalnızca gerekli izinlere sahip olmasını sağlar.
2. **Profil Tabanlı Güvenlik**: Her uygulama için ayrı profiller oluşturularak, hangi dosyalara, dizinlere ve sistem kaynaklarına erişebileceği tanımlanır.
3. **Basit Kullanım**: Profil oluşturma ve yönetme süreci, kullanıcıların kolayca anlayabileceği bir yapıya sahiptir. Profiller, genellikle bir metin dosyası biçiminde tanımlanır.
4. **Güvenlik Olayları Kaydı**: Uygulamalar tarafından gerçekleştirilen işlemler kaydedilebilir, bu da güvenlik denetimi için önemlidir.

AppArmor, özellikle sunucu ve kritik sistemlerde uygulama güvenliğini artırmak için kullanılır.

---


# UFW ve SSH



## UFW (Uncomplicated Firewall)

**UFW**, Linux tabanlı sistemlerde kullanılan bir güvenlik duvarı yönetim aracıdır. Kullanımı kolay bir arayüz sunarak, kullanıcıların IP tabanlı ağ trafiğini yönetmelerini sağlar. İşte UFW hakkında detaylı bilgiler:

### Temel Özellikler

1. **Basit Kullanım**: UFW, karmaşık yapılandırmalar yerine basit ve anlaşılır bir komut seti sunar. Bu, hem yeni başlayanlar hem de deneyimli kullanıcılar için firewall kurallarını yönetmeyi kolaylaştırır.
2. **Öntanımlı Güvenlik**: UFW, varsayılan olarak kapalıdır. Bu, sistemin güvenliğini sağlamak için kurallar oluşturulmadığı sürece dışarıdan gelen tüm trafiği engeller.
3. **Kural Yönetimi**: Kullanıcılar, belirli portları açma veya kapama, IP adreslerine göre erişim izni verme gibi kuralları kolayca tanımlayabilir.
4. **IPv4 ve IPv6 Desteği**: UFW, hem IPv4 hem de IPv6 trafiğini yönetebilir, bu da güncel ağ yapılarına uyum sağlar.
5. **Loglama**: UFW, güvenlik duvarı olaylarını kaydedebilir, böylece kullanıcılar hangi trafiğin engellendiğini veya izin verildiğini takip edebilir.

### Temel Komutlar

- **UFW'yi Etkinleştirme**:
    ```bash
    sudo ufw enable
    ```
    
- **UFW'yi Devre Dışı Bırakma**:
    ```bash
    sudo ufw disable
    ```

- **Durumu Görüntüleme**:
    ```bash
    sudo ufw status
    ```

- **Belirli Bir Portu Açma**:
    ```bash
    sudo ufw allow 4242
    ```

- **Belirli Bir Portu Kapatma**:
    ```bash
    sudo ufw deny 4242
    ```

- **IP Adresine Göre Erişimi Engelleme**:
    ```bash
    sudo ufw deny from 127.0.0.1
    ```

- **Log Kayıtlarını Görüntüleme**:
    ```bash
    sudo ufw status verbose
    ```

### Kullanım Alanları

UFW, genellikle sunucu ortamlarında, masaüstü bilgisayarlarda veya geliştirme makinelerinde güvenlik sağlamak için kullanılır. Kullanıcıların belirli hizmetlere veya uygulamalara erişimi yönetmesine yardımcı olurken, karmaşık iptables kurallarını daha basit bir şekilde yapılandırmalarını sağlar.

UFW, Debian, Ubuntu ve diğer birçok Linux dağıtımında yerleşik olarak bulunur ve kullanıcıların güvenlik duvarı yönetimini kolaylaştırmak için tasarlanmıştır.

---

## SSH (Secure Shell)

**SSH**, ağ üzerinden güvenli bir şekilde iletişim kurmak için kullanılan bir protokoldür. Genellikle uzak sistemlere erişim sağlamak için kullanılır ve veri iletimini şifreleyerek güvenliği artırır. İşte SSH hakkında detaylı bilgiler:

### Temel Özellikler

1. **Güvenli İletişim**: SSH, tüm veri trafiğini şifreleyerek, iletişim sırasında verilerin dinlenmesini veya değiştirilmesini önler. Bu, ağ üzerinde hassas bilgilerin korunmasını sağlar.
2. **Uzak Erişim**: Kullanıcılar, SSH ile uzak sunuculara veya cihazlara güvenli bir şekilde bağlanabilir. Bu, sistem yöneticileri ve geliştiriciler için uzaktan yönetim olanağı sağlar.
3. **Kimlik Doğrulama**: SSH, kullanıcı kimlik doğrulaması için şifreler veya özel anahtarlar kullanır. Anahtar tabanlı kimlik doğrulama, şifreli oturum açma işlemlerine göre daha güvenli kabul edilir.
4. **Port Yönlendirme**: SSH, port yönlendirme ve tünelleme gibi özellikler sunarak, güvenli bağlantılar üzerinden diğer ağ hizmetlerine erişim sağlar.
5. **Dosya Transferi**: SSH, güvenli dosya transferi için SCP (Secure Copy) ve SFTP (SSH File Transfer Protocol) gibi protokollerle entegre çalışabilir.

### Temel Kullanım Komutları

- **Uzak Bir Sunucuya Bağlanma**:
    ```bash
    ssh kullanıcı_adı@sunucu_adresi
    ```

- **Belirli Bir Port ile Bağlanma**:
    ```bash
    ssh -p port_numarası kullanıcı_adı@sunucu_adresi
    ```

- **Anahtar Tabanlı Kimlik Doğrulama ile Bağlanma**:
    ```bash
    ssh -i /path/to/private_key kullanıcı_adı@sunucu_adresi
    ```

- **Uzak Sunucudan Dosya Kopyalama (SCP)**:
    ```bash
    scp /yerel/dosya kullanıcı_adı@sunucu_adresi:/uzak/dizin
    ```

- **Uzak Sunucu ile Dosya Transferi (SFTP)**:
    ```bash
    sftp kullanıcı_adı@sunucu_adresi
    ```

### Kullanım Alanları

SSH, genellikle sistem yöneticileri ve geliştiriciler tarafından sunucuların yönetimi, yazılım geliştirme, dosya transferi ve uzaktan çalışmak için kullanılır. Ayrıca, güvenli bir ağ iletişimi sağladığı için birçok ağ hizmetinin güvenli bir şekilde erişilmesine olanak tanır.

SSH, açık kaynaklıdır ve birçok işletim sisteminde yerleşik olarak bulunur; bu nedenle, geniş bir kullanıcı tabanına sahiptir. Güvenli ve esnek yapısıyla, modern bilgi teknolojileri ortamlarında yaygın olarak kullanılmaktadır.

---

## SSH ve UFW İlişkisi

**SSH (Secure Shell)** ve **UFW (Uncomplicated Firewall)**, Linux tabanlı sistemlerde güvenliği artırmak için birlikte kullanılan iki önemli bileşendir. Aralarındaki ilişki ve nasıl etkileşimde bulundukları şu şekildedir:

### SSH ve UFW İlişkisi

1. **Güvenli Uzak Erişim**:
    - SSH, uzak sunuculara güvenli bir şekilde bağlanmayı sağlar. UFW ise bu bağlantıların güvenliğini artırmak için belirli kurallar tanımlayarak yalnızca yetkili erişimleri kabul eder.
   
2. **Port Yönetimi**:
    - SSH genellikle varsayılan olarak 22 numaralı portu kullanır. UFW ile bu portun açık olduğundan emin olmak, SSH bağlantılarının sorunsuz çalışmasını sağlar. UFW ile port 22'yi açmak için aşağıdaki komut kullanılır:
        ```bash
        sudo ufw allow ssh
        ```
    - Alternatif olarak, belirli bir port üzerinden SSH bağlantısı kuruyorsanız (örneğin, 2222), o portu UFW ile açmanız gerekir:
        ```bash
        sudo ufw allow 4242
        ```

3. **Erişim Kontrolü**:
    - UFW, IP adreslerine göre erişim kuralları belirleyerek SSH bağlantılarını kontrol edebilir. Örneğin, yalnızca belirli bir IP adresinden gelen SSH bağlantılarına izin vermek için şu komut kullanılabilir:
        ```bash
        sudo ufw allow from 127.0.0.1 to any port 4242
        ```
    - Bu, yalnızca belirtilen IP adresinden gelen bağlantıların kabul edilmesini sağlar, böylece potansiyel saldırılara karşı ek bir güvenlik katmanı oluşturur.

4. **Güvenlik İyileştirmeleri**:
    - UFW'yi kullanarak SSH'yi korumak, kötü niyetli kullanıcıların sunucuya erişim sağlama olasılığını azaltır. Örneğin, tüm SSH erişimini belirli IP adresleriyle sınırlamak, "brute-force" saldırılarına karşı koruma sağlar.

5. **Loglama ve İzleme**:
    - UFW, güvenlik duvarı olaylarını kaydedebilir. SSH bağlantıları ve bu bağlantılara ilişkin kural ihlalleri, loglama aracılığıyla izlenebilir. Bu, güvenlik denetimleri ve olası tehditlerin tespit edilmesi için faydalıdır.

### Özet

SSH ve UFW, birlikte kullanıldıklarında sunucuların güvenliğini önemli ölçüde artırabilir. SSH, güvenli uzak erişim sağlarken, UFW bu erişimi kontrol eder ve sınırlar. Bu şekilde, sistem yöneticileri hem güvenli hem de yönetilebilir bir ortam oluşturabilirler.



## Yeni Kullanıcı ve Grup Oluşturma

Debian'da yeni bir kullanıcı ve kullanıcı grubu oluşturmak, güvenli bir parola politikası belirlemek için aşağıdaki adımları takip edebilirsiniz.

### Yeni Kullanıcı Oluşturma

1. **Yeni Kullanıcı Oluşturma**:  
   Kullanıcı oluşturmak için `adduser` komutunu kullanabilirsiniz. Terminalde şu komutu yazın:
    
    ```bash
    sudo adduser meke42
    ```

2. **Kullanıcı Bilgilerini Girmek**:  
   Komut çalıştırıldığında, kullanıcı bilgilerini girmeniz istenecek (şifre, ad, telefon numarası vb.). Şifre oluşturduktan sonra diğer bilgileri isteğe bağlı olarak girebilirsiniz.

### Kullanıcı Grubu Oluşturma

1. **Yeni Grup Oluşturma**:  
   Kullanıcı grubu oluşturmak için `addgroup` komutunu kullanabilirsiniz:
    
    ```bash
    sudo addgroup 42istanbul
    ```

2. **Kullanıcıyı Gruba Ekleme**:  
   Kullanıcıyı yeni oluşturduğunuz gruba eklemek için:
    
    ```bash
    sudo usermod -aG yeni_grup_adi meke42
    ```

---

## Güçlü Parola Oluşturma ve Politikaları

### Güvenli Bir Parola Politikası

Güvenli bir parola politikası belirlemek için aşağıdaki adımları uygulayabilirsiniz:

1. **Parola Uzunluğu ve Karmaşıklığı**:
    - Kullanıcı, şifresinin süresinin dolmasına 7 gün kala bir uyarı mesajı almalıdır.
    - Şifre değiştirildikten en az 2 gün sonra tekrar değiştirilebilir olmalıdır.
    - Şifre süresi her 30 günde bir dolmalıdır.
    - Şifre en az 10 karakter uzunluğunda olmalıdır. Şifre en az bir büyük karakter, bir küçük karakter ve bir sayı içermelidir. Ayrıca 3’ten fazla art arda aynı karakteri içermemelidir.
    - Şifre kullanıcının adını içermemelidir.
    - Şifre, eski şifrenin içermediği en az 7 karakter içermelidir (bu kural root kullanıcı için geçerli değildir).
    - Root kullanıcı şifresi de yukarıdaki kurallara uymalıdır.

2. **Parola Gereksinimlerini Ayarlamak**:  
    Parola gereksinimlerini belirlemek için `/etc/login.defs` dosyasındaki `PASS_MIN_LEN`, `PASS_MAX_DAYS`, `PASS_MIN_DAYS` gibi ayarları kullanabilirsiniz.

### Parola Politikasının Faydaları

1. **Güvenlik**:  
   Güçlü parolalar, yetkisiz erişimi zorlaştırarak sistemin güvenliğini artırır.

2. **Veri Koruma**:  
   Kullanıcı hesaplarına erişimin kısıtlanması, hassas verilerin korunmasına yardımcı olur.

3. **Kötü Amaçlı Saldırılara Karşı Koruma**:  
   Parola politikaları, brute-force saldırılarına karşı ek koruma sağlar.

4. **Hesap Yönetimi**:  
   Kullanıcı hesaplarının yönetimini kolaylaştırır ve şüpheli aktiviteleri tespit etmeye yardımcı olur.

5. **Yasal ve Regülasyon Uygunluğu**:  
   Birçok sektör, güçlü parola politikaları uygulamayı zorunlu kılmaktadır. Bu tür politikalar, yasal gereklilikleri karşılamaya yardımcı olur.

---



# LVM (Logical Volume Manager)

**LVM (Logical Volume Manager)**, Linux sistemlerinde depolama alanlarını daha esnek ve verimli bir şekilde yönetmek için kullanılan bir araçtır. LVM, fiziksel depolama birimlerini (örneğin, diskler veya disk bölümleri) mantıksal hacimlere dönüştürerek yönetim kolaylığı sağlar. İşte LVM'in nasıl çalıştığı ve sağladığı faydalar:

---

## LVM Nasıl Çalışır?

1. **Fiziksel Hacimler (PV)**:  
   LVM, fiziksel diskleri veya disk bölümlerini "fiziksel hacimler" olarak tanımlar. Bu hacimler, LVM yapısının temelini oluşturur.

2. **Grup Hacimler (VG)**:  
   Bir veya daha fazla fiziksel hacim bir araya getirilerek bir "grup hacim" (Volume Group) oluşturulur. Bu, fiziksel depolama kaynaklarının bir araya getirilmesini sağlar.

3. **Mantıksal Hacimler (LV)**:  
   Grup hacimden mantıksal hacimler (Logical Volume) oluşturulur. Mantıksal hacimler, işletim sistemi tarafından kullanılabilir depolama alanlarıdır ve genellikle dosya sistemleriyle biçimlendirilir.

4. **Dinamik Yönetim**:  
   LVM, hacimleri dinamik olarak boyutlandırma, ekleme veya çıkarma gibi işlemleri kolaylaştırır. Bu, disk alanı yönetimini daha esnek hale getirir.

---

## LVM'in Faydaları

1. **Esneklik**:  
   Depolama alanlarını gerektiği gibi genişletme veya daraltma imkanı sağlar. Örneğin, bir mantıksal hacmi büyütmek veya küçültmek için basit komutlar kullanabilirsiniz.

2. **Hacim Yönetimi**:  
   Birden fazla fiziksel diski bir arada kullanarak daha büyük bir mantıksal hacim oluşturulabilir. Bu, kullanıcıların daha fazla depolama alanına erişmesini sağlar.

3. **Anlık Görüntü Alma (Snapshot)**:  
   LVM, mevcut hacimlerin anlık görüntülerini alarak yedekleme veya test amaçlı kullanılmasını sağlar. Bu, veri kaybını önlemek için önemli bir özelliktir.

4. **RAID Desteği**:  
   LVM, RAID (Redundant Array of Independent Disks) yapılandırmaları ile birleştirilebilir. Bu, veri güvenliği ve performansı artırır.

5. **Kolay Yedekleme ve Geri Yükleme**:  
   LVM kullanarak, veri yedeklemesi ve geri yükleme süreçleri daha kolay ve hızlı bir şekilde gerçekleştirilebilir.

6. **Karmaşık Yapıların Basit Yönetimi**:  
   Büyük ve karmaşık sistemlerde, depolama alanlarını yönetmek daha basit hale gelir. Mantıksal hacimlerin yönetimi, fiziksel disklere göre daha az karmaşık olabilir.

---

## Özet

LVM, Linux sistemlerinde depolama alanını daha esnek ve yönetilebilir hale getiren güçlü bir araçtır. Esnekliği, hacim yönetimindeki kolaylıkları ve veri güvenliği özellikleri ile birçok sistem yöneticisi ve kullanıcı tarafından tercih edilmektedir. Özellikle büyük sunucularda ve veri merkezlerinde LVM kullanımı yaygındır.


# SUDO (Superuser Do)

**sudo (superuser do)**, Unix ve Linux tabanlı işletim sistemlerinde, kullanıcıların yönetici (root) hakları ile belirli komutları çalıştırmalarına olanak tanıyan bir programdır. Kullanıcıların sistem üzerinde daha fazla yetki gerektiren işlemleri gerçekleştirebilmesi için kullanılır. İşte sudo hakkında detaylı bilgiler:

---

## Temel Özellikler

1. **Yetkilendirme**:  
   - `sudo`, kullanıcıların yalnızca belirli komutları çalıştırmalarına izin verir. Bu, kullanıcının yetkilerini artırırken güvenliği de sağlar.

2. **Kullanıcı Yönetimi**:  
   - `sudo`, sistem yöneticilerinin hangi kullanıcıların hangi komutları çalıştırabileceğini belirlemesine olanak tanır. Bu, `/etc/sudoers` dosyası aracılığıyla yapılandırılır.

3. **Geçici Root Erişimi**:  
   - Kullanıcılar, `sudo` kullanarak geçici olarak root yetkileriyle komut çalıştırabilirler. Bu, root hesabına doğrudan giriş yapmadan gerekli işlemleri yapma imkanı sağlar.

4. **Kayıt Tutma**:  
   - `sudo`, çalıştırılan komutları kaydederek kullanıcı etkinliğini izler. Bu, güvenlik denetimleri ve sorun giderme süreçleri için faydalıdır.

5. **Parola İhtiyacı**:  
   - `sudo` komutu çalıştırıldığında, kullanıcıdan kendi parolasını girmesi istenir. Bu, yetkisiz erişimi önlemeye yardımcı olur.

---

## Temel Kullanım Komutları

- **Bir Komutu Root Olarak Çalıştırma**:  
    Bir komutu root olarak çalıştırmak için `sudo` komutunu kullanabilirsiniz:
    
    ```bash
    sudo komut
    ```
    
    Örneğin, bir dosyayı kopyalamak için:
    
    ```bash
    sudo cp /kaynak/dosya /hedef/dizin
    ```

- **Bir Shell Açma**:  
    Eğer tüm oturumda root yetkileriyle çalışmak istiyorsanız:
    
    ```bash
    sudo -i
    ```

- **Bir Komutu Farklı Bir Kullanıcı Olarak Çalıştırma**:  
    Belirli bir kullanıcı olarak komut çalıştırmak için:
    
    ```bash
    sudo -u kullanıcı_adı komut
    ```

---

## Sudoers Dosyası

- **Yapılandırma**:  
   `sudo` yetkilerini yönetmek için `/etc/sudoers` dosyası kullanılır. Bu dosya, hangi kullanıcıların hangi komutları çalıştırabileceğini belirler.
   
- **Visudo Aracı**:  
   `sudoers` dosyasını düzenlemek için `visudo` komutunu kullanmak önerilir. Bu, dosyanın hatalarını kontrol ederek yapılandırma sorunlarını önler.

---

## Faydaları

1. **Güvenlik**:  
   Kullanıcıların root hesabına doğrudan erişimini engelleyerek güvenliği artırır.

2. **Kullanıcı İzleme**:  
   Hangi kullanıcının ne tür komutlar çalıştırdığını izlemeyi kolaylaştırır.

3. **Esneklik**:  
   Sistem yöneticileri, kullanıcıların yetkilerini detaylı bir şekilde yönetebilir.

4. **Eğitim**:  
   Kullanıcıların yönetici yetkilerini öğrenmelerine ve kullanmalarına olanak tanır.

---

## Özet

`sudo`, sistem yönetimi ve güvenlik için kritik bir araçtır. Kullanıcıların yönetici haklarına sahip olmadan gerekli işlemleri gerçekleştirmelerine olanak tanırken, aynı zamanda sistemin güvenliğini artırır. Hem kullanıcılar hem de sistem yöneticileri için önemli bir araçtır.



# CRON

**Cron**, Unix ve Linux tabanlı işletim sistemlerinde zamanlanmış görevleri otomatik olarak çalıştırmak için kullanılan bir sistem aracıdır. Belirli zaman dilimlerinde veya belirli aralıklarla otomatik olarak komutlar veya betikler çalıştırmak için kullanılır. İşte Cron hakkında detaylı bilgiler:

---

## Temel Özellikler

1. **Zamanlama**:  
   - Cron, kullanıcıların ve sistem yöneticilerinin belirli zaman dilimlerinde komut veya betik çalıştırmalarına olanak tanır. Örneğin, günlük, haftalık veya belirli bir tarihte çalıştırma yapılabilir.

2. **Cron Tablosu**:  
   - Kullanıcıların zamanlanmış görevlerini tanımlamak için kullanılan dosyaya "crontab" denir. Her kullanıcının kendine ait bir crontab dosyası vardır.
   - Sistem genelindeki görevler için `/etc/crontab` dosyası ve `/etc/cron.d/` dizini kullanılır.

3. **Basit Kullanım**:  
   - Cron, kullanıcıların görevleri zamanlamasını ve yönetmesini kolaylaştırır. Herhangi bir programlama bilgisi gerektirmez.

4. **Esneklik**:  
   - Zamanlama aralıkları dakikalar, saatler, günler, aylar ve haftanın günleri olarak belirlenebilir.

---

## Crontab Dosyası Yapısı

Crontab dosyasındaki her satır, bir zamanlama ve çalıştırılacak komut içerir.

Buradaki `*` işaretleri sırasıyla şu anlamlara gelir:

1. **Dakika** (0-59)
2. **Saat** (0-23)
3. **Gün** (1-31)
4. **Ay** (1-12)
5. **Hafta Günü** (0-7) (0 ve 7 Pazar'ı temsil eder)

---

## Örnek Crontab Girişleri

1. **Her gün saat 2:30'da bir betik çalıştırma**:

    ```bash
    30 2 * * * /path/to/script.sh
    ```

2. **Her hafta Pazartesi saat 5'te yedekleme yapma**:

    ```bash
    0 5 * * 1 /path/to/backup.sh
    ```

3. **Her 15 dakikada bir belirli bir komut çalıştırma**:

    ```bash
    */15 * * * * /path/to/command
    ```

---

## Crontab ile Çalışma

- **Crontab Dosyasını Düzenleme**:

    ```bash
    crontab -e
    ```

- **Crontab Dosyasını Görüntüleme**:

    ```bash
    crontab -l
    ```

- **Crontab Dosyasını Temizleme**:

    ```bash
    crontab -r
    ```

---

## Faydaları

1. **Otomatikleştirme**:  
   Tekrar eden görevlerin otomatik olarak yapılmasını sağlar, bu da zaman kazandırır.

2. **Planlama**:  
   Sistem yönetimi ve bakım görevlerini belirli zamanlarda gerçekleştirme imkanı sunar.

3. **Kolay Yönetim**:  
   Kullanıcı dostu bir yapı ile görevlerin kolayca yönetilmesini sağlar.

4. **Verimlilik**:  
   Sistem kaynaklarını daha verimli kullanarak manuel işlemleri azaltır.

---

## Özet

Cron, zamanlanmış görevlerin otomatik olarak çalıştırılmasını sağlayarak sistem yöneticilerine ve kullanıcılarına önemli bir kolaylık sunar. Veri yedekleme, rapor oluşturma, güncellemeleri kontrol etme gibi işlemler için sıklıkla kullanılır. Bu özellikleri ile sistemlerin düzenli ve verimli bir şekilde yönetilmesine yardımcı olur.




# Lighttpd

**Lighttpd**, yüksek performanslı ve hafif bir web sunucusudur. Özellikle düşük kaynak kullanımı ve hızlı yanıt süreleri ile bilinir. Genellikle dinamik ve statik web içeriği sunmak için kullanılır. İşte Lighttpd hakkında detaylı bilgiler:

---

## Temel Özellikler

1. **Hafif Yapı**:  
   Lighttpd, düşük bellek ve CPU kullanımıyla yüksek performans sağlar. Bu özellik, onu özellikle kaynak sınırlı sunucular için ideal kılar.

2. **Asenkron I/O Desteği**:  
   Asenkron giriş/çıkış (I/O) desteği sayesinde, çok sayıda eşzamanlı bağlantıyı etkin bir şekilde yönetebilir. Bu, yüksek trafikli web siteleri için önemli bir avantajdır.

3. **Modüler Yapı**:  
   Lighttpd, çeşitli modüller aracılığıyla işlevselliğini genişletir. Örneğin, FastCGI, SCGI, CGI, WebDAV, SSL ve daha fazlasını destekler.

4. **URL Yeniden Yazma**:  
   Lighttpd, URL yeniden yazma kurallarını destekler, bu da SEO ve kullanıcı deneyimi açısından faydalıdır.

5. **Statik İçerik Performansı**:  
   Statik içerik sunma konusunda oldukça hızlıdır. Bu, resimler, CSS ve JavaScript dosyaları gibi içeriklerin hızlı bir şekilde sunulmasını sağlar.

6. **TLS/SSL Desteği**:  
   Güvenli bağlantılar için TLS/SSL desteği sunar. Bu, HTTPS protokolü ile güvenli web sunumu sağlar.

---

## Kullanım Alanları

- **Küçük ve Orta Ölçekli Web Siteleri**:  
   Lighttpd, düşük kaynak tüketimi ile küçük ve orta ölçekli web siteleri için idealdir.

- **Yüksek Trafikli Web Uygulamaları**:  
   Asenkron I/O desteği sayesinde, yüksek trafikli uygulamalar ve hizmetler için uygundur.

- **Geliştirme Ortamları**:  
   Hızlı kurulum ve düşük kaynak kullanımı ile geliştirme ve test ortamları için popüler bir seçenektir.

---

## Kurulum ve Temel Yapılandırma

Lighttpd, genellikle paket yöneticileri aracılığıyla kolayca kurulabilir.

```bash
sudo apt install lighttpd
```



## MariaDB

**MariaDB**, MySQL veritabanı yönetim sisteminin bir çatallanmasıdır (fork) ve özellikle açık kaynak kodlu, yüksek performanslı, ve güvenilir bir veritabanı çözümü olarak geliştirilmiştir.
MySQL'in kurucu geliştiricileri tarafından başlatılmıştır ve kullanıcıların veri yönetimini kolaylaştırmak için tasarlanmıştır.

---

## Temel Özellikler

1. **Açık Kaynak**:  
   MariaDB, GNU Genel Kamu Lisansı (GPL) altında dağıtılmaktadır. Bu, kullanıcıların yazılımı özgürce kullanabilmesini, değiştirebilmesini ve dağıtabilmesini sağlar.

2. **MySQL ile Uyumluluk**:  
   MariaDB, MySQL ile yüksek derecede uyumlu bir yapıya sahiptir. MySQL veritabanları genellikle MariaDB ile sorunsuz bir şekilde çalıştırılabilir.

3. **Yüksek Performans**:  
   Performans iyileştirmeleri ile büyük veri setleri üzerinde daha hızlı sorgu sonuçları sunar. Özellikle yazma ve okuma işlemlerinde optimizasyonlar içerir.

4. **Gelişmiş Özellikler**:  
   MariaDB, MySQL'e ek olarak birçok yeni özellik ve iyileştirme sunar. Örneğin, yeni depolama motorları (Aria, TokuDB), sanal kolonlar, ve daha iyi optimizasyonlar gibi özellikler içerir.

5. **Güvenlik**:  
   Kullanıcı kimlik doğrulaması ve veri şifreleme gibi güvenlik özellikleri ile donatılmıştır. Bu, veritabanının güvenliğini artırır.

6. **Veri Yedekleme ve Kurtarma**:  
   Yedekleme ve kurtarma süreçlerini kolaylaştıran araçlar ve yöntemler içerir. Bu, veri kaybı riskini azaltır.

---

## Kullanım Alanları

- **Web Uygulamaları**:  
   Çeşitli web uygulamaları ve içerik yönetim sistemlerinde (CMS) yaygın olarak kullanılır.

- **Veri Analizi**:  
   Büyük veri setlerinin analizi için güçlü bir altyapı sunar.

- **Kurumsal Uygulamalar**:  
   İşletmelerde veri yönetimi ve analiz ihtiyaçlarını karşılamak için kullanılabilir.

---

## Kurulum ve Temel Yapılandırma

MariaDB, birçok işletim sistemi için paket yöneticileri aracılığıyla kolayca kurulabilir.

```bash
sudo apt update
sudo apt install mariadb-server
```



# PHP

**PHP (Hypertext Preprocessor)**, özellikle web geliştirme için yaygın olarak kullanılan, açık kaynak kodlu bir betik dilidir. Sunucu tarafında çalışan bir dil olup, dinamik web sayfaları oluşturmak için sıklıkla tercih edilir. İşte PHP hakkında detaylı bilgiler:

---

## Temel Özellikler

1. **Sunucu Taraflı Çalışma**:  
   PHP, web sunucusunda çalışarak HTML, CSS ve JavaScript gibi diğer dillerle birlikte dinamik içerik oluşturur. Kullanıcı isteklerine göre içerik üretebilir.

2. **Kolay Öğrenim**:  
   PHP, sözdizimi açısından kullanıcı dostudur ve programlamaya yeni başlayanlar için öğrenmesi kolay bir dil olarak bilinir.

3. **Geniş Topluluk ve Destek**:  
   PHP, büyük bir topluluğa ve kapsamlı belgelerle desteklenmektedir. Sorun giderme ve kaynak bulma açısından oldukça avantajlıdır.

4. **Veritabanı Entegrasyonu**:  
   PHP, MySQL, MariaDB, PostgreSQL gibi birçok veritabanı ile kolayca entegre olabilir. Veritabanı işlemleri için birçok yerleşik fonksiyon ve kütüphane sunar.

5. **Çok Amaçlı Kullanım**:  
   PHP, yalnızca web uygulamaları değil, aynı zamanda komut satırı uygulamaları ve masaüstü uygulamaları için de kullanılabilir.

6. **Framework Desteği**:  
   Laravel, Symfony, CodeIgniter gibi birçok popüler PHP framework'ü bulunmaktadır. Bu framework'ler, geliştirme sürecini hızlandırır ve düzenli bir yapı sağlar.

---

## Kullanım Alanları

- **Dinamik Web Siteleri**:  
   PHP, kullanıcı etkileşimleri, veri tabanı etkileşimleri ve içerik yönetimi gibi dinamik web siteleri oluşturmak için idealdir.

- **İçerik Yönetim Sistemleri (CMS)**:  
   WordPress, Joomla ve Drupal gibi popüler CMS'lerin temelini oluşturur.

- **E-ticaret Uygulamaları**:  
   Magento ve WooCommerce gibi e-ticaret platformları PHP ile geliştirilmiştir.

---

## Kurulum

PHP, genellikle paket yöneticileri aracılığıyla kolayca kurulabilir. Örneğin, Debian tabanlı sistemlerde aşağıdaki komutla kurulum yapılabilir:

```bash
sudo apt update
sudo apt install php
```


# WordPress

**WordPress**, dünyada en yaygın kullanılan içerik yönetim sistemlerinden (CMS) biridir. İlk olarak 2003 yılında blog platformu olarak geliştirilen WordPress, zamanla güçlü bir web sitesi oluşturma aracı haline gelmiştir. Açık kaynaklı bir yazılım olması, kullanıcıların ve geliştiricilerin yazılımı özgürce kullanabilmesine, değiştirebilmesine ve dağıtabilmesine olanak tanır. İşte WordPress hakkında detaylı bilgiler:

---

## Temel Özellikler

1. **Kullanıcı Dostu Arayüz**:  
   WordPress, kullanıcıların kolayca içerik oluşturmasına ve yönetmesine olanak tanıyan basit ve sezgisel bir arayüze sahiptir.

2. **Esnek Tema ve Eklenti Desteği**:  
   WordPress, binlerce ücretsiz ve premium tema ile web sitenizin görünümünü özelleştirmenizi sağlar. Ayrıca, işlevselliği artırmak için çok sayıda eklenti mevcuttur.

3. **SEO Dostu**:  
   WordPress, arama motorları için optimize edilmiş yapısıyla, kullanıcıların web sitelerini SEO (Arama Motoru Optimizasyonu) açısından daha görünür hale getirmesine yardımcı olur.

4. **Responsive Tasarım**:  
   Çoğu tema, mobil cihazlarla uyumlu olacak şekilde tasarlanmıştır, böylece siteniz farklı ekran boyutlarında da iyi görünür.

5. **Topluluk ve Destek**:  
   WordPress, büyük bir topluluğa sahiptir. Sorunlarınızı çözmek için birçok kaynak ve forum bulunmaktadır.

6. **Çok Dilli Desteği**:  
   WordPress, çoklu dil desteği sunarak global kullanıcılar için uygun hale getirir.

---

## Kullanım Alanları

- **Bloglar**:  
   WordPress, başlangıçta bir blog platformu olarak ortaya çıktığı için kişisel ve profesyonel bloglar için ideal bir çözümdür.

- **Kurumsal Web Siteleri**:  
   Şirketler, WordPress'i kurumsal web siteleri oluşturmak için kullanabilirler.

- **E-Ticaret**:  
   WooCommerce gibi eklentiler sayesinde, WordPress ile güçlü e-ticaret siteleri oluşturulabilir.

- **Portföyler**:  
   Sanatçılar, tasarımcılar ve diğer profesyoneller, çalışmalarını sergilemek için portföy siteleri oluşturabilirler.

---

## Kurulum ve Başlangıç

WordPress, genellikle aşağıdaki adımlarla kurulur:

1. **Sunucu ve Domain Seçimi**:  
   Bir web sunucusu ve alan adı satın alınır.

2. **WordPress İndirme**:  
   WordPress'in resmi web sitesinden en son sürüm indirilir.

3. **Yükleme**:  
   İndirilen dosyalar, sunucuya yüklenir ve gerekli veritabanı ayarları yapılır.

4. **Kurulum**:  
   Web tarayıcısı üzerinden kurulum sihirbazı takip edilerek temel ayarlar yapılır.

---

## Faydaları

1. **Ücretsiz ve Açık Kaynak**:  
   WordPress, maliyet olmadan kullanılabilir ve geniş bir geliştirici topluluğuna sahiptir.

2. **Hızlı Geliştirme**:  
   Kullanıcı dostu arayüzü ile hızlı bir şekilde içerik oluşturulabilir.

3. **Geniş Özelleştirme Seçenekleri**:  
   Temalar ve eklentiler ile web sitesi işlevselliği ve görünümü kolayca değiştirilebilir.

4. **Gelişmiş SEO Araçları**:  
   Yoast SEO gibi eklentilerle SEO optimizasyonu yapılabilir.

---

## Özet

WordPress, esnekliği, kullanıcı dostu arayüzü ve geniş tema ve eklenti desteği ile hem bireysel kullanıcılar hem de işletmeler için ideal bir web sitesi oluşturma platformudur. Bloglardan kurumsal web sitelerine, e-ticaret platformlarından portföylere kadar çok çeşitli alanlarda kullanılmaktadır.




# Debian 10 Kurulum ve Yapılandırma Rehberi

## İçindekiler
1. [Ön Hazırlık ve Disk Bölümleme](#ön-hazırlık-ve-disk-bölümleme)
2. [Temel Sistem Kurulumu](#temel-sistem-kurulumu)
3. [Sudo Kurulumu ve Yapılandırması](#sudo-kurulumu-ve-yapılandırması)
4. [SSH Kurulumu ve Yapılandırması](#ssh-kurulumu-ve-yapılandırması)
5. [UFW Güvenlik Duvarı Kurulumu](#ufw-güvenlik-duvarı-kurulumu)
6. [Hostname Değiştirme](#hostname-değiştirme)
7. [Sudo Yapılandırması](#sudo-yapılandırması)
8. [Kullanıcı Yönetimi ve Şifre Politikası](#kullanıcı-yönetimi-ve-şifre-politikası)
9. [Crontab Yapılandırması](#crontab-yapılandırması)

## Ön Hazırlık ve Disk Bölümleme

### Disk Alanı Gereksinimleri
- Bonus bölüm için 30,80 GB alan gereklidir

### Temel Kurulum Adımları
1. "Install" seçeneğini seçin
2. Dil ve klavye seçimlerini yapın
3. Ana bilgisayar adını [kullanıcıadı42] formatında girin (örn: meke42)
4. Domain name alanını boş bırakın
5. Root kullanıcısı için şifre belirleyin
6. Yeni kullanıcının tam adını yazın
7. Kullanıcı adı kısmına intra kullanıcı adını yazın (örn: meke)
8. Yeni kullanıcı için şifre belirleyin ve tekrar girin
9. Zaman dilimini Central seçin

### Disk Yapılandırması
1. Manual seçeneğini seçin
2. Önceden oluşturulan diski seçin
3. Yes ile devam edin
4. Boş alanı seçin
5. "Create a new partition" seçin
6. İlk bölüm için:
   - 525MB alan ayırın
   - Primary seçin
   - Beginning seçin
   - Use as: Ext2 file system
   - Mount point: /boot
   - Bootable flag: on

7. Kalan alan için:
   - 32.5 GB
   - Logical
   - Şifreleme yapılandırması:
     - Configure encrypted volumes
     - Create encrypted volumes
     - /dev/sda5 seçin
     - Yes ile devam edin

8. LVM Yapılandırması:
   - Configure the Logical Volume Manager
   - Create volume group: "LVMGroup"
   - Şifrelenmiş sda5'i seçin
   - Aşağıdaki logical volume'ları oluşturun:
     - root: 10.7 GB
     - swap: 2.5 GB
     - home: 5.4 GB
     - var: 3.2 GB
     - srv: 3.2 GB
     - tmp: 3.2 GB
     - var-log: 4.3 GB

9. Bölümlerin Mount Point Yapılandırması:
   - home: Ext4, /home
   - root: Ext4, / (root)
   - srv: Ext4, /srv
   - swap: swap area
   - tmp: Ext2, /tmp
   - var: Ext4, /var
   - var-log: Ext4, /var/log

## Temel Sistem Kurulumu

1. Partitioning'i tamamlayın ve Yes ile onaylayın
2. Debian mirror ülke seçimini yapın
3. Yazılım seçimlerini kaldırın
4. GRUB boot loader için:
   - Yes seçin
   - /dev/sda seçin
5. Kurulum tamamlandığında sistem yeniden başlayacak
6. Şifrelenmiş disk için şifreyi girin
7. Kullanıcı adı ve şifre ile giriş yapın

## Sudo Kurulumu ve Yapılandırması

1. Root ortamına geçiş:
```bash
su -
```

2. Sudo kurulumu:
```bash
apt update -y
apt upgrade -y
apt install sudo
```

3. Kurulumu kontrol edin:
```bash
dpkg -l | grep sudo
```

4. Kullanıcıyı sudo grubuna ekleme:
```bash
adduser <username> sudo
# veya
usermod -aG sudo <username>
```

5. Kontrolü:
```bash
getent group sudo
```

6. Sudoers dosyasını düzenleme:
```bash
sudo visudo
```
Eklenecek satır:
```
your_username ALL=(ALL) ALL
```

7. Sistemi yeniden başlatın:
```bash
reboot
```

8. Sudo yetkisini kontrol edin:
```bash
sudo -v
```

## SSH Kurulumu ve Yapılandırması

1. SSH kurulumu:
```bash
sudo apt install openssh-server -y
# veya
sudo apt install ssh -y
```

2. Kurulumu kontrol edin:
```bash
dpkg -l | grep ssh
```

3. SSH durumunu kontrol edin:
```bash
sudo systemctl status ssh
```

4. SSH'yi yeniden başlatın:
```bash
sudo service ssh restart
```

5. Port değişikliği için config dosyasını düzenleyin:
```bash
sudo vim /etc/ssh/sshd_config
```

Yapılacak değişiklikler:
```
Port 4242
PermitRootLogin no
```

6. Değişiklikleri kontrol edin:
```bash
sudo grep Port /etc/ssh/sshd_config
```

7. SSH'yi yeniden başlatın:
```bash
sudo service ssh restart
```

## UFW Güvenlik Duvarı Kurulumu

1. UFW kurulumu:
```bash
sudo apt install ufw -y
```

2. Kurulumu kontrol edin:
```bash
dpkg -l | grep ufw
```

3. UFW'yi etkinleştirin:
```bash
sudo ufw enable
```

4. SSH ve Port 4242 için kurallar:
```bash
sudo ufw allow ssh
sudo ufw allow 4242
```

5. Kuralları görüntüleme ve silme:
```bash
sudo ufw status numbered
sudo ufw delete <rule_number>
```

## Hostname Değiştirme

1. Mevcut hostname'i kontrol edin:
```bash
hostnamectl
```

2. Yeni hostname ayarlama:
```bash
sudo hostnamectl set-hostname <new_hostname>
```

3. /etc/hosts dosyasını düzenleyin:
```bash
sudo vim /etc/hosts
```

4. Sistemi yeniden başlatın:
```bash
reboot
```

## Sudo Yapılandırması

1. Sudo log dizini oluşturma:
```bash
sudo mkdir /var/log/sudo
```

2. Sudoers dosyasını düzenleme:
```bash
sudo visudo
```

Eklenecek yapılandırmalar:
```
Defaults log_input,log_output
Defaults logfile="/var/log/sudo/sudo.log"
Defaults requiretty
Defaults secure_path="/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/snap/bin"
Defaults passwd_tries=3
Defaults badpass_message="Hatali Sifre Girdiniz! Lutfen Tekrar Giriniz"
```

## Kullanıcı Yönetimi ve Şifre Politikası

### Şifre Yaşı Ayarları

1. Login.defs dosyasını düzenleyin:
```bash
sudo vim /etc/login.defs
```

Yapılacak değişiklikler:
```
PASS_MAX_DAYS 30
PASS_MIN_DAYS 2
PASS_WARN_AGE 7
```

2. Mevcut kullanıcılar için ayarları güncelleme:
```bash
sudo chage --mindays 2 <user>
sudo chage --maxdays 30 <user>
sudo chage --warndays 7 <user>
```

3. Ayarları kontrol etme:
```bash
chage -l <user>
```

### Şifre Gücü Ayarları

1. libpam-pwquality kurulumu:
```bash
sudo apt install libpam-pwquality -y
```

2. Yapılandırma dosyasını düzenleme:
```bash
sudo vim /etc/pam.d/common-password
```

Eklenecek ayarlar:
```
password requisite pam_pwquality.so retry=3 ucredit=-1 lcredit=-1 dcredit=-1 maxrepeat=3 usercheck=1 difok=7 enforce_for_root minlen=10
```

### Kullanıcı Yönetimi Komutları

1. Yeni kullanıcı oluşturma:
```bash
sudo adduser <username>
```

2. Kullanıcı kontrolü:
```bash
sudo getent passwd <username>
id <username>
```

3. Grup üyeliği kontrolü:
```bash
groups
groups <username>
```

4. Kullanıcı silme:
```bash
sudo deluser <username>
sudo deluser --remove-home <username>
sudo deluser --remove-all-files <username>
```

## Crontab Yapılandırması

1. Net-tools kurulumu:
```bash
sudo apt update -y
sudo apt install -y net-tools
```

2. Monitoring script oluşturma (/usr/local/bin/monitoring.sh)


3. Sudoers dosyasına monitoring.sh için kural ekleme:
```bash
sudo visudo
```
Eklenecek satır:
```
your_username ALL=(ALL) NOPASSWD: /usr/local/bin/monitoring.sh
```

4. Crontab yapılandırması:
```bash
sudo crontab -u root -e
```
Eklenecek satır:
```
*/10 * * * * bash /usr/local/bin/monitoring.sh
```

5. Cron servisi yönetimi:
```bash
sudo service cron stop    # Durdurmak için
sudo service cron start   # Başlatmak için
```

##Contributors
Muhammed Maruf Güveli
Emir Ismail Genç

##Resources
Davut Uzun born2beroot kurulum notları
wiki.archlinux.org/title/Main_page


