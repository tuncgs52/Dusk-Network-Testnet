# Dusk-Network-Testnet

## Sistem Gereksinimleri
| Bileşenler | Minimum Gereksinimler | 
| ------------ | ------------ |
| Ubuntu 22.04.2 |
| CPU |	2 |
| RAM	| 4 GB |
| Storage	|  GB SSD |

# Rusku İndiriyoruz.

```
curl --proto '=https' --tlsv1.2 -sSfL https://github.com/dusk-network/itn-installer/releases/download/v0.1.0/itn-installer.sh | sudo sh
```

İndirdikten Sonra Eğer Daha Önceden Dusk Cüzdanınız Varsa Şu Komutu Kullanın.

```
rusk-wallet restore
```

Eğer yoksa, [Buraya Basın](https://wallet.dusk.network/setup/)
Yeni Bir cüzdan Oluşturun Daha Sonra

```
rusk-wallet restore
```

Mnemonikleri girin. Şifrenizi Oluşturun.

# Cüzdan İçin Anahtarı Dışarı Aktarıyoruz. 
Bizden Şifre İsteyecek Girin.
Resimdeki Gibiyse sıkıntı yok.

```
rusk-wallet export -d /opt/dusk/conf -n consensus.keys
```

![Screenshot_2024-02-15-22-45-52-000-edit_com server auditor ssh client](https://github.com/tuncgs52/Dusk-Network-Testnet/assets/80161670/7d5a2823-6d64-4e30-bbec-d506f85bfca8)

Şifre Girin.

```
sh /opt/dusk/bin/setup_consensus_pwd.sh
```


# RUSKU Başlatıyoruz

Arka Planda Çalışmaya Başlayacak.

```
service rusk start
```

# Son Aşama Stake Edeceğiz.

Node Eşitlenene Kadar Bekliyoruz. Şu Komutla Kontrol edin.

```
grep "block accepted" /var/log/rusk.log
```

"Height" Explorerdakiyle Aynı ise işlemlere devam edin.
![Screenshot_2024-02-15-22-50-02-931-edit_com server auditor ssh client](https://github.com/tuncgs52/Dusk-Network-Testnet/assets/80161670/db278e2d-d332-4042-92c6-34f4a4e9c8ef)

[EXPLORER LİNK](https://explorer.dusk.network/)


