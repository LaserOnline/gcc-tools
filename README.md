
# GCC Control Version

1. ติดตั้ง dpkg (Debian tools) ผ่าน Homebrew
```
brew install dpkg
```
2. ติดตัั้ง GCC
```
brew install gcc
```
select version
```
gcc@12
```
```
gcc@13
```
```
gcc@14
```

4. ใช้ update-alternatives ที่มากับ dpkg
```
sudo update-alternatives --install /usr/local/bin/gcc gcc /opt/homebrew/bin/gcc-14 50
sudo update-alternatives --install /usr/local/bin/gcc gcc /opt/homebrew/bin/gcc-12 40
```

5. สลับเวอร์ชัน gcc:
```
sudo update-alternatives --config gcc
```

6. update
```
gcc --version
```

---
1. ลบ Symlink เดิม
```
sudo update-alternatives --remove gcc /opt/homebrew/bin/gcc-14
```

2. สร้าง Symlink ใหม่
```
sudo ln -s /opt/homebrew/bin/gcc-12 /usr/local/bin/gcc
```

3. ตรวจสอบ
```
gcc --version
```
