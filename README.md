
**Slim Framework RestFull Api**

Bu restfull servisinde kullanılan teknolojiler Slim Framework ve MySQL


MySQL konfigürasyon

 

       CREATE DATABASE slimdb;
        
        CREATE TABLE `kitaplar`  (
      `id` int(11) NOT NULL AUTO_INCREMENT,
      `kit_adi` varchar(255) CHARACTER SET utf8 COLLATE utf8_general_ci NULL DEFAULT NULL,
      `kit_yazar` varchar(255) CHARACTER SET utf8 COLLATE utf8_general_ci NULL DEFAULT NULL,
      `kit_isbn` varchar(255) CHARACTER SET utf8 COLLATE utf8_general_ci NULL DEFAULT NULL,
      `kit_sayfa` int(11) NULL DEFAULT NULL,
      PRIMARY KEY (`id`) USING BTREE
    ) ENGINE = InnoDB AUTO_INCREMENT = 3 CHARACTER SET = utf8 COLLATE = utf8_general_ci ROW_FORMAT = Dynamic;
    
    
    INSERT INTO `kitaplar` VALUES (1, 'Sineklerin Tanrısı', 'William Golding', '9789754582901', 262);
    INSERT INTO `kitaplar` VALUES (2, 'Şeker Portakalı', 'Jose Mauro De Vasconcelos', '9789750738609', 200);

Lütfen veritabanını oluşturun ve `src\settings.php` dosyasını düzeltin.

Projeyi çalıştırmak için proje klasöründe

    composer update

    php -S localhost:8080 -t public

`http://localhost:8080/tumkitaplar` adresini tarayıcınızda açınız.

