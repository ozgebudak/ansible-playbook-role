- Çalıştırmak için rke2-lablabs dosyasının içine girerek ansible-playbook komutu çalıştırılır.
- Burada rke2-install.yaml içerisinde yüklemek istediklerimize göre seçenekleri yorum satırından çıkarıp yükleme işlemi yapabiliriz.
```
ansible-playbook -i inventory.yaml rke2-install.yaml --extra-vars "ansible_sudo_pass=<makina şifresi>"
```