# kasumi_quran_vault.json
A clean Next.js boilerplate for uploading files and JSON to IPFS via Pinata. Secure, fast, and scalable. Perfect for NFT minting, Web3 storage, and decentralized apps.
npx create-next-app@latest pinata-next
cd pinata-next
npm run dev
git init
git add .
git commit -m "init nextjs + pinata uploader"
git remote add origin https://github.com/USERNAME/NAMA-REPO.git
git branch -M main
git push -u origin main
pinata-next/
 ├─ app/
 │   ├─ api/pinata/json/route.js
 │   └─ upload/page.jsx
 ├─ .env.local   ❌ (JANGAN di-push)
 ├─ package.json
