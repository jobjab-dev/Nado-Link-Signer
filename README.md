# Nado Link Signer UI

Web UI สำหรับสร้างและ Sign Linked Signer ของ Nado Exchange

## Features

- 🔐 **Generate Linked Signer**: สร้าง wallet key ใหม่สำหรับ bot
- ✍️ **Sign with Ledger**: Sign EIP-712 message ผ่าน MetaMask/Rabby ที่เชื่อมต่อกับ Ledger
- 🚀 **Submit to Nado**: ส่ง link request ไปยัง Nado API

## Usage

### Option 1: Open Directly

เปิดไฟล์ `index.html` ใน browser ได้เลย:

```bash
# Windows
start index.html

# macOS
open index.html

# Linux
xdg-open index.html
```

### Option 2: Local Server

```bash
# Python 3
python -m http.server 3000

# Then open http://localhost:3000
```

### Option 3: Deploy to Vercel

#### CLI
```bash
npm i -g vercel
vercel deploy
```

#### Web Dashboard
1. ไปที่ https://vercel.com/new
2. Import จาก GitHub หรือ Drag & Drop folder นี้
3. Deploy!

## How to Use

### Step 1: Create Linked Signer
1. กรอก Ledger wallet address ที่เชื่อมต่อกับ Nado
2. กด "Generate Linked Signer"
3. **บันทึก Private Key!** (จะใช้ใส่ใน .env)

### Step 2: Sign with Ledger
1. กด "Connect Wallet" เพื่อเชื่อมต่อ MetaMask/Rabby
2. ตรวจสอบว่าเลือก account ที่ถูกต้อง (Ledger address)
3. กด "Sign with Ledger"
4. ยืนยันบน Ledger device

### Step 3: Submit to Nado
1. กด "Submit to Nado"
2. รอจนสำเร็จ
3. Copy configuration ไปใส่ใน `.env` file

## Configuration

หลังจาก setup สำเร็จ ให้เพิ่มใน `.env`:

```env
NADO_PRIVATE_KEY=0x...your_linked_signer_private_key...
```

## Requirements

- Ledger hardware wallet
- MetaMask, Rabby, or similar browser wallet
- Nado account with deposited funds

## Technical Details

- Chain: Ink Mainnet (Chain ID: 57073)
- Endpoint: `0x05ec92D78ED421f3D3Ada77FFdE167106565974E`
- API: `https://gateway.prod.nado.xyz/v1`

## License

MIT
