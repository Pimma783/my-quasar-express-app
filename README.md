# Quasar Version Control and Docker Demo

เจ้าของโปรเจกต์: Phanusak Jongaksorn

Lab 1.1 สร้าง Quasar SPA แสดงขั้นตอน Git และแนวคิด Docker

## Development

```sh
cd frontend
npm ci
npm run dev
```

## ตรวจสอบและ build

```sh
cd frontend
npm run lint
npm run build
```

## Docker Compose

จาก root ของโปรเจกต์:

```sh
docker compose up -d --build
# เปิด http://localhost:8080
docker compose down
```

## Docker

```sh
docker build -t my-quasar-frontend:latest ./frontend
docker run -d -p 8080:80 --name my-quasar-frontend-container my-quasar-frontend:latest
```

## Git workflow

```sh
git switch -c feature/quasar-version-control-page
# แก้ไขโค้ด
git add frontend/src/pages/IndexPage.vue
git commit -m "feat: update version control demo"
git push -u origin feature/quasar-version-control-page
```

เปิด Pull Request ไป main ตรวจสอบ แล้ว merge

โฟลเดอร์ backend เตรียมไว้สำหรับ Express ในบทถัดไป
