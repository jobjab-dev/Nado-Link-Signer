# Nado Link Signer UI

Web UI to create and sign a Linked Signer for Nado Exchange.

## Features

- 🔐 **Generate Linked Signer**: Create a new wallet key for your bot
- ✍️ **Sign with Ledger**: Sign EIP-712 message via MetaMask/Rabby connected to Ledger
- 🚀 **Submit to Nado**: Send link request to Nado API
- 🔒 **Secure**: Private key is shown only once, then permanently hidden

## Usage

### Option 1: Open Directly

Open `index.html` in your browser:

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
1. Go to https://vercel.com/new
2. Import from GitHub or drag & drop this folder
3. Deploy!

## How to Use

### Step 1: Create Linked Signer
1. Enter your Ledger wallet address (connected to Nado)
2. Click "Generate Linked Signer"
3. **Save the Private Key!** (shown only once in the secure modal)

### Step 2: Sign with Ledger
1. Click "Connect Wallet" to connect MetaMask/Rabby
2. Make sure you select the correct account (Ledger address)
3. Click "Sign with Ledger"
4. Approve on your Ledger device

### Step 3: Submit to Nado
1. Click "Submit to Nado"
2. Wait for success
3. Add the private key you saved to your `.env` file

## Configuration

After successful setup, add to your `.env`:

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

## Security

- Private key is displayed **only once** in a secure modal
- User must explicitly copy the key before continuing
- Private key is **never stored** or displayed again after modal closes
- No data is sent to any third-party servers

## License

MIT
