- Çalıştırmak için rke2-lablabs dosyasının içine girerek ansible-playbook komutu çalıştırılır.
- SSH erişimini yapmamız gerekiyor.

```
ssh-copy-id erkut@192.168.1.207
ssh-copy-id erkut@192.168.1.208
 ```
- Makinalarda Hostname ayarı yapılması gerekiyor. Bunun için makinalara girip düzenlemek gerek.
```
  sudo nano /etc/hostname
   buraya girip master ve worker makinalarımıza göre isimlerini veriyoruz.
```

- Burada rke2-install.yaml içerisinde yüklemek istediklerimize göre seçenekleri yorum satırından çıkarıp yükleme işlemi yapabiliriz.
```
ansible-playbook -i inventory.yaml rke2-install.yaml --extra-vars "ansible_sudo_pass=<makina şifresi>"
```
