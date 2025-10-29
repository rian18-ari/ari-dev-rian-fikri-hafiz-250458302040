# ari-dev-rian-fikri-hafiz-250458302040

# 🚀 Tailwind CSS Setup (Plain HTML)

Project ini pakai **Tailwind CSS** tanpa framework — cuma HTML + Tailwind CLI aja.
Cocok buat latihan atau project kecil yang butuh setup cepat tanpa ribet.

---

## 📦 Setup

### 1. Clone project

```bash
git clone https://github.com/username/nama-project.git
cd nama-project
```

### 2. Install Tailwind CSS

Pastikan Node.js udah terinstall, terus jalanin:

```bash
npm install -D tailwindcss
npx tailwindcss init
```

Ini bakal bikin file `tailwind.config.js`.

---

## ⚙️ Konfigurasi

### 1. Atur file input/output CSS

Di dalam folder project, pastikan kamu punya struktur kayak gini:

```
.
├─ src/
│  └─ input.css
├─ dist/
│  └─ output.css
├─ index.html
└─ tailwind.config.js
```

Isi `src/input.css`:

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

### 2. Update file `tailwind.config.js`

```js
module.exports = {
  content: ["./*.html"],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

---

## 💻 Build CSS

### Mode development (auto update)

```bash
npx tailwindcss -i ./src/input.css -o ./dist/output.css --watch
```

### Mode production (lebih kecil ukurannya)

```bash
npx tailwindcss -i ./src/input.css -o ./dist/output.css --minify
```

---

## 🧠 Tips

* Kalau CSS nggak muncul, cek path di HTML kamu:

  ```html
  <link rel="stylesheet" href="./dist/output.css">
  ```
* Pastikan terminal tetap jalan kalau lagi pakai `--watch`.
* Buat folder `components/` kalau mau pisah file HTML biar rapi.

---

## 📜 License

Bebas dipakai, diubah, atau dimodif. Have fun 😎
