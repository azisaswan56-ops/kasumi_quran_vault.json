/app/api/pinata/json/route.js
import { PinataSDK } from "pinata";
import { NextResponse } from "next/server";

const pinata = new PinataSDK({
  pinataJwt: process.env.PINATA_JWT,
});

export async function POST(req) {
  const body = await req.json();

  const upload = await pinata.upload.public.json(body);

  return NextResponse.json(upload);
}
"use client";

export default function UploadJSON() {
  const handleUpload = async () => {
    const data = {
      name: "NFT Kabutaku #1",
      description: "NFT spiritual baddie edition",
      image: "ipfs://CID_GAMBAR",
      attributes: [
        { trait_type: "Aura", value: "Hijrah tapi savage" },
        { trait_type: "Level", value: 999 }
      ]
    };

    const res = await fetch("/api/pinata/json", {
      method: "POST",
      headers: { "Content-Type": "application/json" },
      body: JSON.stringify(data)
    });

    const result = await res.json();
    console.log(result);
    alert("JSON ke-IPFS-kan 🚀");
  };

  return (
    <button
      onClick={handleUpload}
      className="px-4 py-2 bg-black text-white rounded"
    >
      Upload JSON
    </button>
  );
}
{
  "IpfsHash": "bafybeig....",
  "PinSize": 512,
  "Timestamp": "2026-02-23T..."
}
Upload Image → dapat CID
      ↓
Masukin ke JSON metadata
      ↓
Upload JSON → dapat CID metadata
      ↓
Mint NFT → pakai CID metadata