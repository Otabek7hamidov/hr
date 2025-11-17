# Unicon-Soft HR Boshqaruv Tizimi

Viloyat HR bo'limi uchun tuman va shahar bo'limlarini boshqarish tizimi.

## 🚀 O'rnatish va ishga tushirish

### 1. Loyihani yuklab olish
```bash
git clone https://github.com/sizning-username/unicon-soft-hr.git
cd unicon-soft-hr
```

### 2. Kerakli paketlarni o'rnatish
```bash
npm install
```

### 3. Ishga tushirish (Development)
```bash
npm run dev
```

Brauzerda ochish: `http://localhost:5173`

### 4. Production uchun build qilish
```bash
npm run build
```

Build fayllari `dist` papkasida paydo bo'ladi.

## 📦 GitHub Pages'ga deploy qilish

### Variant 1: Avtomatik deploy (GitHub Actions)

1. GitHub'da repositoriyangizni oching
2. Settings → Pages → Source → "GitHub Actions" ni tanlang
3. Quyidagi faylni yarating: `.github/workflows/deploy.yml`

```yaml
name: Deploy to GitHub Pages

on:
  push:
    branches: [ main ]

jobs:
  build-and-deploy:
    runs-on: ubuntu-latest
    
    steps:
    - name: Checkout
      uses: actions/checkout@v3
      
    - name: Setup Node.js
      uses: actions/setup-node@v3
      with:
        node-version: '18'
        
    - name: Install dependencies
      run: npm install
      
    - name: Build
      run: npm run build
      
    - name: Deploy to GitHub Pages
      uses: peaceiris/actions-gh-pages@v3
      with:
        github_token: ${{ secrets.GITHUB_TOKEN }}
        publish_dir: ./dist
```

4. Kodingizni push qiling:
```bash
git add .
git commit -m "Initial commit"
git push origin main
```

5. GitHub Actions avtomatik deploy qiladi
6. Saytingiz: `https://sizning-username.github.io/unicon-soft-hr/`

### Variant 2: Manual deploy

```bash
npm run build
cd dist
git init
git add -A
git commit -m 'deploy'
git push -f git@github.com:sizning-username/unicon-soft-hr.git main:gh-pages
```

## 🔐 Login ma'lumotlari

**Admin Panel:**
- Login: `admin`
- Parol: `admin123`

## 🛠️ Texnologiyalar

- React 18
- Vite
- Tailwind CSS
- Lucide Icons
- LocalStorage (ma'lumotlarni saqlash)

## 📱 Imkoniyatlar

✅ Tuman/Shahar bo'limlarini boshqarish  
✅ Rahbar va xodimlarni qo'shish  
✅ Rasm bilan profil  
✅ To'liq ma'lumotlar (ism, lavozim, tug'ilgan sana, telefon)  
✅ Admin panel  
✅ Responsive dizayn  

## 📞 Yordam

Savollar yoki muammolar bo'lsa:
- Email: support@uniconsoft.uz
- Telegram: @uniconsoft

## 📄 Litsenziya

© 2024 Unicon-Soft MCHJ. Barcha huquqlar himoyalangan.