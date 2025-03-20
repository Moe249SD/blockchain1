خطوات تشغيل المشروع
=====================================


---

التقنيات المستخدمة:
- **Node.js** - بيئة تشغيل JavaScript
- **Express.js** - إطار عمل لبناء السيرفر
- **MongoDB & GridFS** - قاعدة بيانات لتخزين الملفات
- **Web3.js** - للتفاعل مع عقد ذكي في البلوكشين
- **Solidity** - لكتابة العقد الذكي
- **EJS** - محرك قوالب لعرض الصفحات
- **MetaMask** - محفظة رقمية لعمليات البلوكشين

---

**خطوات تشغيل المشروع:**

**تثبيت المتطلبات:**
```sh
npm install
```

**إنشاء ملف البيئة `.env`**
قم بإنشاء ملف `.env` في جذر المشروع وأضف البيانات التالية:
```
PORT=5000
MONGO_URI=your_mongodb_connection_string
BLOCKCHAIN_RPC_URL=your_blockchain_rpc_url
CONTRACT_ADDRESS=your_contract_address
```

**تشغيل السيرفر:**
```sh
node server.js
```

**فتح المتصفح وزيارة:**
```
http://localhost:5000
```

---

**العقد الذكي (Solidity)**
```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract DocumentStorage {
    mapping(bytes32 => bool) private storedHashes;
    
    function storeDocument(bytes32 hash) public {
        storedHashes[hash] = true;
    }
    
    function verifyDocument(bytes32 hash) public view returns (bool) {
        return storedHashes[hash];
    }
}
```

---

**الميزات:**
✅ تسجيل الدخول باستخدام MetaMask
✅ رفع المستندات وتخزين بصمة التجزئة على البلوكشين
✅ التحقق من أصالة المستندات
✅ لوحة تحكم للمستخدمين



