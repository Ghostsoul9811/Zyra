# Zyra
Web3 social networking 
zyra/
├── client/                 # React frontend
│   ├── components/
│   ├── pages/
│   ├── App.jsx
│   └── index.html
├── server/                 # FastAPI backend
│   ├── routes/
│   ├── utils/
│   ├── supabase/
│   ├── main.py
│   └── requirements.txt
├── contracts/              # Solana smart contracts (Rust)
│   ├── solana_program/
│   │   ├── Cargo.toml
│   │   └── src/lib.rs
├── .env.example
└── README.md
import React from 'react';
import WalletConnect from './components/WalletConnect';
import Feed from './components/Feed';
import TradeDashboard from './components/TradeDashboard';

export default function App() {
  return (
    <div className="p-6">
      <h1 className="text-3xl font-bold">Zyra Hybrid Platform</h1>
      <WalletConnect />
      <Feed />
      <TradeDashboard />
    </div>
  );
}
import React from 'react';

export default function WalletConnect() {
  return (
    <div className="mt-4">
      <button className="bg-blue-500 text-white px-4 py-2 rounded">
        Connect Wallet
      </button>
    </div>
  );
import React from 'react';

export default function Feed() {
  return (
    <div className="mt-6">
      <h2 className="text-xl font-semibold">Feed</h2>
      <p>Posts will appear here...</p>
    </div>
  );
}
import React from 'react';

export default function TradeDashboard() {
  return (
    <div className="mt-6">
      <h2 className="text-xl font-semibold">Trade Dashboard</h2>
      <p>Live trading and stats here...</p>
    </div>
  );
}
<!DOCTYPE html>
<html>
<head>
  <title>Zyra Platform</title>
  <meta charset="UTF-8" />
</head>
<body>
  <div id="root"></div>
</body>
</html>
module.exports = {
  content: ["./client/**/*.{js,jsx,ts,tsx,html}"],
  theme: {
    extend: {},
  },
  plugins: [],
};
