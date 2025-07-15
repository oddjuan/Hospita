# Hoxpital

A decentralized application (dApp) for online medical services, built in Rust.  
Users can access medical services, book appointments with doctors, and check drug availability in nearby pharmacies.

## Project Structure

```
Hospita/
├── backend/        # Actix Web REST API server
├── frontend/       # Yew SPA client (Rust/WASM)
├── contract/       # NEAR Protocol smart contract (Rust)
├── Cargo.toml      # Cargo workspace definition
```

## Quick Start

### Prerequisites

- Rust (latest stable)
- Node.js & npm (for serving frontend)
- NEAR CLI (for deploying smart contract)

---

### 1. Backend (Actix Web API)

```bash
cd backend
cargo run
```
Server runs at `http://127.0.0.1:8080`

---

### 2. Frontend (Yew SPA)

For development:
```bash
cd frontend
# Use Trunk (recommended: cargo install trunk)
trunk serve
```
Open your browser at `http://127.0.0.1:8080`  
You may need to adjust Trunk config to serve at a different port.

---

### 3. Smart Contract (NEAR Protocol)

```bash
cd contract
# Build WASM for NEAR
cargo build --target wasm32-unknown-unknown --release
# Deploy with NEAR CLI (update account and network accordingly)
near deploy --wasmFile target/wasm32-unknown-unknown/release/contract.wasm --accountId <your-account.testnet>
```

---

## Features

- **Book Appointments:** Patients can book appointments with doctors.
- **Drug Availability:** Check drugs available in nearby pharmacies.
- **Smart Contract:** Appointments stored on blockchain for auditability.
- **Rust Full Stack:** Backend, frontend, and smart contract all in Rust.

## Customization

- Extend the smart contract for more medical records, prescriptions, or decentralized governance.
- Connect backend to real blockchain events, databases, or external APIs.
- Enhance frontend with user authentication (wallet login), search, and notifications.

## License

MIT

---

## Contributing

Pull requests and issues are welcome.  
See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.
