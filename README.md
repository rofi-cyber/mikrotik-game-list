# MikroTik Game Address List 🎮

Repository ini berisi daftar IP server game populer untuk MikroTik,
digunakan bersama mangle + queue tree agar **ping game stabil**.

## 📜 Cara Pakai

1. Import script di MikroTik:

```rsc
/tool fetch url="https://raw.githubusercontent.com/YOUR_USERNAME/mikrotik-game-list/main/game-list.rsc" dst-path=game-list.rsc;
/import file-name=game-list.rsc;
```

2. Tambahkan mangle & queue sesuai kebutuhan (lihat contoh di repo ini).
3. Untuk auto-update, buat scheduler di MikroTik:

```rsc
/system script
add name=update-game-list source="\
/tool fetch url=\"https://raw.githubusercontent.com/YOUR_USERNAME/mikrotik-game-list/main/game-list.rsc\" dst-path=game-list.rsc;\r\
\n/import file-name=game-list.rsc;"

 /system scheduler
 add name="auto-update-game-list" on-event=update-game-list interval=12h
```

## 🎮 Daftar Game Support
- Mobile Legends  
- PUBG Mobile  
- Free Fire  
- Valorant  
- COD Mobile  
- Genshin Impact  
- Dota 2  
- CS:GO  
- Roblox  
- Minecraft  
- League of Legends  
- Apex Legends  

Update daftar IP bisa dilakukan dengan **pull request** atau edit langsung.
