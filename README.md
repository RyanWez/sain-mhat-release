<div align="center">

# ✨ ဆိုင်မှတ် (Sain Mhat) POS ✨

### 🇲🇲 မြန်မာဆိုင်ငယ်များအတွက် Professional Offline-first POS စနစ်

<p>
  <img src="https://img.shields.io/badge/Version-1.0.3-blue?style=for-the-badge&logo=flutter&logoColor=white" alt="Version"/>
  <img src="https://img.shields.io/badge/Platform-Android-green?style=for-the-badge&logo=android&logoColor=white" alt="Platform"/>
  <img src="https://img.shields.io/badge/Flutter-3.10+-02569B?style=for-the-badge&logo=flutter&logoColor=white" alt="Flutter"/>
  <img src="https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge" alt="License"/>
</p>

<p>
  <strong>သင့်ဆိုင်အတွက် ယုံကြည်စိတ်ချရသော POS - Internet မလိုပဲ အသုံးပြုနိုင်ပါသည်</strong>
</p>

---

</div>

<!-- Main Content -->

<br/>

## 📋 မာတိကာ

<table>
<tr>
<td width="50%" valign="top">

- [🎯 App Overview](#-app-overview)
- [✨ Main Features](#-main-features)
- [💳 Point of Sale (POS)](#-point-of-sale-pos)
- [📦 Inventory Management](#-inventory-management)
- [🔄 FIFO Stock System](#-fifo-stock-system)

</td>
<td width="50%" valign="top">

- [📊 Reports & Analytics](#-reports--analytics)
- [⚙️ Settings & Customization](#️-settings--customization)
- [🔔 Alert System](#-alert-system)
- [🖨️ Printing & Export](#️-printing--export)
- [💰 Currency & Tax](#-currency--tax)

</td>
</tr>
</table>

---

<br/>

## 🎯 App Overview

<table>
<tr>
<td>

### 🏪 ဘာအတွက် သုံးသလဲ?

**ဆိုင်မှတ်** သည် မြန်မာနိုင်ငံရှိ ဆိုင်ငယ်များအတွက် အထူးပြုလုပ်ထားသော **Point of Sale (POS)** စနစ်ဖြစ်ပါသည်။

- 🌐 **Offline-first**: Internet မလိုပဲ အပြည့်အဝ အသုံးပြုနိုင်
- 🔐 **Encrypted Database**: Data များကို SQLCipher ဖြင့် လုံခြုံစွာ သိမ်းဆည်း
- ☁️ **Cloud Backup**: Supabase Cloud သို့ Sync လုပ်နိုင် (Optional)
- 🇲🇲 **Myanmar Localization**: မြန်မာဘာသာ အပြည့်အဝ Support

</td>
</tr>
</table>

<table>
<tr>
<td align="center" width="25%">
  <h3>🛒</h3>
  <strong>POS System</strong>
  <br/>
  <small>အရောင်းစာရင်း မြန်ဆန်စွာ ရိုက်ထည့်</small>
</td>
<td align="center" width="25%">
  <h3>📦</h3>
  <strong>Inventory</strong>
  <br/>
  <small>FIFO Stock Tracking</small>
</td>
<td align="center" width="25%">
  <h3>📊</h3>
  <strong>Reports</strong>
  <br/>
  <small>အသေးစိတ် အစီရင်ခံစာများ</small>
</td>
<td align="center" width="25%">
  <h3>🖨️</h3>
  <strong>Printing</strong>
  <br/>
  <small>Receipt & PDF Export</small>
</td>
</tr>
</table>

---

<br/>

## ✨ Main Features

<table>
<tr>
<td width="50%" valign="top">

### 💳 အရောင်းစနစ် (POS)

- ✅ Barcode Scanner ဖြင့် ပစ္စည်းရှာ
- ✅ Cart System
- ✅ Discount (% / Fixed Amount)
- ✅ Stock Limit Check
- ✅ Receipt Printing

### 📦 Stock Management

- ✅ FIFO Stock Tracking
- ✅ Batch-based Cost Tracking
- ✅ Stock In (ကုန်ဝယ်)
- ✅ Stock Adjustment
- ✅ Low Stock Alerts

### 📋 Item & Category

- ✅ Item CRUD
- ✅ Category Management
- ✅ Item Image Support
- ✅ Barcode Assignment

</td>
<td width="50%" valign="top">

### 📊 Reports

- ✅ Daily/Weekly/Monthly Sales
- ✅ Profit Analysis
- ✅ FIFO Cost Report
- ✅ Inventory Valuation
- ✅ Top Selling Items

### ⚙️ Settings

- ✅ Shop Info (Name, Phone, Address)
- ✅ Receipt Customization
- ✅ Tax Configuration
- ✅ Currency Settings
- ✅ Data Backup/Restore

### 🔔 Notifications

- ✅ Low Stock Alerts
- ✅ Daily Sales Summary
- ✅ Customizable Thresholds

</td>
</tr>
</table>

---

<br/>

## 💳 Point of Sale (POS)

### 🛒 အရောင်းလုပ်ငန်းစဉ် (Sales Workflow)

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                          📱 POS WORKFLOW                                     │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│   ┌──────────────┐    ┌──────────────┐    ┌──────────────┐                  │
│   │  1️⃣ Search   │───▶│  2️⃣ Add to  │───▶│  3️⃣ Apply   │                  │
│   │   Items      │    │     Cart     │    │   Discount   │                  │
│   └──────────────┘    └──────────────┘    └──────────────┘                  │
│          │                                       │                          │
│          │     ┌───────────────────────────────┐ │                          │
│          │     │  📷 Barcode Scan              │ │                          │
│          └────▶│  🔍 Name Search               │ │                          │
│                │  📂 Category Browse           │ │                          │
│                └───────────────────────────────┘ │                          │
│                                                  ▼                          │
│   ┌──────────────┐    ┌──────────────┐    ┌──────────────┐                  │
│   │  6️⃣ Print   │◀───│  5️⃣ Save    │◀───│  4️⃣ Confirm │                  │
│   │   Receipt   │    │     Sale     │    │     Sale     │                  │
│   └──────────────┘    └──────────────┘    └──────────────┘                  │
│                              │                                              │
│                              ▼                                              │
│                    ┌─────────────────┐                                      │
│                    │ FIFO Stock      │                                      │
│                    │ Auto Deducted   │                                      │
│                    └─────────────────┘                                      │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

### 🔍 ပစ္စည်းရှာဖွေနည်းများ

<table>
<tr>
<td align="center" width="33%">
<h3>📷</h3>
<strong>Barcode Scanner</strong>
<br/><br/>
ကင်မရာဖြင့် Barcode Scan လုပ်၍ ပစ္စည်းကို ချက်ချင်း ထည့်နိုင်
</td>
<td align="center" width="33%">
<h3>🔍</h3>
<strong>Name Search</strong>
<br/><br/>
ပစ္စည်းအမည် ရိုက်ထည့်၍ ရှာဖွေနိုင်
</td>
<td align="center" width="33%">
<h3>📂</h3>
<strong>Category Browse</strong>
<br/><br/>
Category အလိုက် Browse လုပ်၍ ရွေးချယ်နိုင်
</td>
</tr>
</table>

### 💰 Discount System

<table>
<tr>
<th>Discount Type</th>
<th>Description</th>
<th>Example</th>
</tr>
<tr>
<td><strong>Percentage (%)</strong></td>
<td>စုစုပေါင်း၏ ရာခိုင်နှုန်းအလိုက် လျှော့</td>
<td>10% လျှော့ → 10,000 Ks မှ 9,000 Ks</td>
</tr>
<tr>
<td><strong>Fixed Amount</strong></td>
<td>ပမာဏအတိအကျ လျှော့</td>
<td>500 Ks လျှော့ → 10,000 Ks မှ 9,500 Ks</td>
</tr>
</table>

---

<br/>

## 📦 Inventory Management

### 📋 Item Management

<table>
<tr>
<td width="60%">

#### 📝 Item Information

- **အမည်** - ပစ္စည်းအမည်
- **Barcode** - Barcode နံပါတ် (Optional)
- **ရောင်းဈေး** - Selling Price
- **ကုန်ဈေး** - Cost Price (Stock In မှ Auto Track)
- **Category** - ပစ္စည်းအမျိုးအစား
- **Stock** - လက်ကျန် (FIFO Batches မှ Auto Calculate)
- **ပုံ** - Item Image (Optional)

</td>
<td width="40%">

```
┌────────────────────┐
│   🍜 ကြာဇံ         │
├────────────────────┤
│ Barcode: 123456789 │
│ Price: 2,500 Ks    │
│ Stock: 45 pcs      │
│ Category: အစားအစာ   │
└────────────────────┘
```

</td>
</tr>
</table>

### 📥 Stock In (ကုန်ဝယ်ထည့်ခြင်း)

```
┌─────────────────────────────────────────────────────────────────┐
│                      📥 STOCK IN PROCESS                         │
├─────────────────────────────────────────────────────────────────┤
│                                                                  │
│   📦 ပစ္စည်း ရွေးချယ်ပါ                                          │
│        ↓                                                         │
│   🔢 အရေအတွက် ထည့်ပါ (Quantity: 100)                            │
│        ↓                                                         │
│   💵 တစ်ခုချင်း ကုန်ဈေး ထည့်ပါ (Cost: 1,200 Ks)                  │
│        ↓                                                         │
│   ✅ Stock In Confirm                                            │
│        ↓                                                         │
│   ┌─────────────────────────────────────────────┐               │
│   │  🆕 NEW FIFO BATCH CREATED                  │               │
│   │  Date: 2026-01-25                           │               │
│   │  Qty: 100 pcs                               │               │
│   │  Cost: 1,200 Ks/pc                          │               │
│   │  Remaining: 100 pcs                         │               │
│   └─────────────────────────────────────────────┘               │
│                                                                  │
└─────────────────────────────────────────────────────────────────┘
```

### 🔧 Stock Adjustment

Stock Adjustment ဖြင့် Stock အတိုး/အလျှော့ ပြုလုပ်နိုင်ပါသည်:

| Type            | Description  | Use Case                         |
| --------------- | ------------ | -------------------------------- |
| ➕ **Increase** | Stock တိုး   | ကုန်ပစ္စည်းပြန်တွေ့, Gift/Sample |
| ➖ **Decrease** | Stock လျှော့ | ပျက်စီး, ပြုတ်ကျ, Expiry         |

---

<br/>

## 🔄 FIFO Stock System

### 📖 FIFO ဆိုတာ ဘာလဲ?

**FIFO (First-In, First-Out)** ဆိုသည်မှာ **အရင်ဝယ်ထားတဲ့ ပစ္စည်းကို အရင်ရောင်း** ဆိုသည့် Stock Tracking Method ဖြစ်ပါသည်။

<table>
<tr>
<td>

### ✅ FIFO ရဲ့ အားသာချက်များ

1. **Accurate COGS** - Cost of Goods Sold ကို တိကျစွာ တွက်ချက်နိုင်
2. **Profit Tracking** - အမြတ်/အရှုံးကို batch အလိုက် သိနိုင်
3. **Expiry Management** - အဟောင်းကို အရင်ရောင်းသည့်အတွက် Expiry ပြဿနာ နည်း
4. **Inventory Valuation** - Stock တန်ဖိုးကို တိကျစွာ သိနိုင်

</td>
</tr>
</table>

### 🔄 FIFO အလုပ်လုပ်ပုံ

```
══════════════════════════════════════════════════════════════════════════════
                           🔄 FIFO WORKFLOW EXAMPLE
══════════════════════════════════════════════════════════════════════════════

📥 STOCK IN (ကုန်ဝယ်ထည့်)
──────────────────────────────────────────────────────────────────────────────
   Jan 10: Batch #1 → 10 items @ 500 Ks/pc    (Total: 5,000 Ks)
   Jan 15: Batch #2 → 10 items @ 600 Ks/pc    (Total: 6,000 Ks)
   Jan 20: Batch #3 → 10 items @ 550 Ks/pc    (Total: 5,500 Ks)

   📦 Total Stock: 30 items
   💰 Total Cost: 16,500 Ks

══════════════════════════════════════════════════════════════════════════════

🛒 SALE: 15 items @ 800 Ks/pc  (Total: 12,000 Ks)
──────────────────────────────────────────────────────────────────────────────

   FIFO Consumption:
   ├── Batch #1: 10 items × 500 Ks = 5,000 Ks (FULLY CONSUMED ✓)
   └── Batch #2:  5 items × 600 Ks = 3,000 Ks (5 remaining)

   📊 COGS (Cost of Goods Sold): 8,000 Ks
   📈 Profit: 12,000 - 8,000 = 4,000 Ks

══════════════════════════════════════════════════════════════════════════════

📦 REMAINING STOCK
──────────────────────────────────────────────────────────────────────────────
   ├── Batch #2: 5 items @ 600 Ks/pc  (3,000 Ks)
   └── Batch #3: 10 items @ 550 Ks/pc (5,500 Ks)

   📦 Total Remaining: 15 items
   💰 Total Value: 8,500 Ks

══════════════════════════════════════════════════════════════════════════════
```

### 🔙 Void Sale (ရောင်းချမှု ပယ်ဖျက်)

Sale တစ်ခုကို Void လုပ်သောအခါ FIFO Stock ကို အလိုအလျောက် ပြန်ထည့်ပေးပါသည်:

```
┌────────────────────────────────────────────────────────────────┐
│                   🔙 VOID SALE PROCESS                          │
├────────────────────────────────────────────────────────────────┤
│                                                                 │
│  Before Void:                                                   │
│  └── Batch #2: 5 items remaining                               │
│                                                                 │
│  Void Sale (15 items):                                         │
│  ├── Restore to Batch #1: 10 items                             │
│  └── Restore to Batch #2: 5 items                              │
│                                                                 │
│  After Void:                                                    │
│  ├── Batch #1: 10 items ✓                                      │
│  ├── Batch #2: 10 items ✓                                      │
│  └── Batch #3: 10 items ✓                                      │
│                                                                 │
│  📦 Total Stock Restored: 30 items                             │
│                                                                 │
└────────────────────────────────────────────────────────────────┘
```

---

<br/>

## 📊 Reports & Analytics

### 📈 Available Reports

<table>
<tr>
<td align="center" width="25%">
<h3>📅</h3>
<strong>Sales Report</strong>
<br/><br/>
Daily, Weekly, Monthly ရောင်းရငွေ
</td>
<td align="center" width="25%">
<h3>💹</h3>
<strong>Profit Analysis</strong>
<br/><br/>
အမြတ်/အရှုံး ခွဲခြမ်းစိတ်ဖြာ
</td>
<td align="center" width="25%">
<h3>📦</h3>
<strong>FIFO Report</strong>
<br/><br/>
Batch အလိုက် Stock တန်ဖိုး
</td>
<td align="center" width="25%">
<h3>🏆</h3>
<strong>Top Items</strong>
<br/><br/>
အရောင်းရဆုံး ပစ္စည်းများ
</td>
</tr>
</table>

### 📊 Sales Report

```
┌──────────────────────────────────────────────────────────────────┐
│                     📊 DAILY SALES SUMMARY                        │
│                       2026-01-25                                  │
├──────────────────────────────────────────────────────────────────┤
│                                                                   │
│   💰 Total Sales:           150,000 Ks                           │
│   📦 Total Items Sold:      45 items                             │
│   🧾 Number of Transactions: 12                                   │
│   💳 Average Transaction:    12,500 Ks                           │
│                                                                   │
├──────────────────────────────────────────────────────────────────┤
│   📈 Cost of Goods Sold:    95,000 Ks                            │
│   💹 Gross Profit:          55,000 Ks                            │
│   📊 Profit Margin:         36.7%                                │
│                                                                   │
└──────────────────────────────────────────────────────────────────┘
```

### 📦 FIFO Inventory Report

```
┌──────────────────────────────────────────────────────────────────┐
│                   📦 FIFO INVENTORY VALUATION                     │
├──────────────────────────────────────────────────────────────────┤
│                                                                   │
│  Item: ကြာဇံ                                                      │
│  ├── Batch 1: 2026-01-10 │ 20 pcs @ 1,200 Ks │ Value: 24,000 Ks │
│  ├── Batch 2: 2026-01-18 │ 15 pcs @ 1,300 Ks │ Value: 19,500 Ks │
│  └── Batch 3: 2026-01-22 │ 30 pcs @ 1,250 Ks │ Value: 37,500 Ks │
│                                                                   │
│  📊 Total Stock: 65 pcs                                          │
│  💰 Total Value: 81,000 Ks                                       │
│  📈 Avg Cost: 1,246 Ks/pc                                        │
│                                                                   │
└──────────────────────────────────────────────────────────────────┘
```

---

<br/>

## ⚙️ Settings & Customization

### 🏪 Shop Information

<table>
<tr>
<td width="50%">

| Setting          | Description                   |
| ---------------- | ----------------------------- |
| 🏪 **Shop Name** | Receipt တွင် ပြမည့် ဆိုင်အမည် |
| 📞 **Phone**     | ဆက်သွယ်ရန် ဖုန်းနံပါတ်        |
| 📍 **Address**   | ဆိုင်လိပ်စာ                   |
| 🖼️ **Logo**      | Receipt Header Logo           |

</td>
<td width="50%">

```
┌─────────────────────────┐
│    🏪 SHOP INFO         │
├─────────────────────────┤
│ Name: ABC ကုန်စုံဆိုင်   │
│ Phone: 09-123456789     │
│ Address: ရန်ကုန်မြို့    │
└─────────────────────────┘
```

</td>
</tr>
</table>

### 🧾 Receipt Settings

<table>
<tr>
<th>Setting</th>
<th>Options</th>
<th>Description</th>
</tr>
<tr>
<td>📏 Paper Size</td>
<td>58mm / 80mm</td>
<td>Thermal Receipt Paper အရွယ်အစား</td>
</tr>
<tr>
<td>🖼️ Show Logo</td>
<td>ON / OFF</td>
<td>Receipt Header တွင် Logo ပြ/မပြ</td>
</tr>
<tr>
<td>📝 Footer Message</td>
<td>Custom Text</td>
<td>Receipt အောက်ခြေ မက်ဆေ့</td>
</tr>
<tr>
<td>🔢 Show Item Code</td>
<td>ON / OFF</td>
<td>Barcode/Item Code ပြ/မပြ</td>
</tr>
</table>

### 💼 Tax Settings

<table>
<tr>
<td>

| Tax Type         | Description                  |
| ---------------- | ---------------------------- |
| 🔘 **No Tax**    | Tax မကောက်ပါ                 |
| 📊 **Inclusive** | ရောင်းဈေးထဲတွင် Tax ပါပြီး   |
| 📊 **Exclusive** | ရောင်းဈေးအပေါ် Tax ထပ်ပေါင်း |

</td>
<td>

```
Tax Calculation Example:

Exclusive 5%:
└── Item: 10,000 Ks
└── Tax: 500 Ks (5%)
└── Total: 10,500 Ks

Inclusive 5%:
└── Total: 10,000 Ks
└── (Item: 9,524 Ks + Tax: 476 Ks)
```

</td>
</tr>
</table>

### 💱 Currency Settings

<table>
<tr>
<td width="50%">

#### Supported Currencies

| Currency        | Symbol | Format   |
| --------------- | ------ | -------- |
| 🇲🇲 Myanmar Kyat | Ks     | 1,000 Ks |
| 🇺🇸 US Dollar    | $      | $10.00   |
| 🇹🇭 Thai Baht    | ฿      | ฿100     |

</td>
<td width="50%">

#### Display Options

- Decimal Places: 0 / 2
- Symbol Position: Before / After
- Thousands Separator: , / .
- Show Currency Code: MMK / USD / THB

</td>
</tr>
</table>

---

<br/>

## 🔔 Alert System

### ⚠️ Low Stock Alerts

<table>
<tr>
<td width="60%">

#### 🔔 How It Works

1. **Set Threshold**: ပစ္စည်းတစ်ခုချင်းစီအတွက် Low Stock Threshold သတ်မှတ်
2. **Auto Monitor**: Stock လက်ကျန်ကို အလိုအလျောက် စစ်ဆေး
3. **Alert**: Threshold အောက်ရောက်သောအခါ Notification ပေး

#### 📊 Alert Dashboard

- 🔴 **Critical**: Stock 0 (Out of Stock)
- 🟠 **Warning**: Stock < Threshold
- 🟢 **OK**: Stock >= Threshold

</td>
<td width="40%">

```
┌──────────────────────┐
│  ⚠️ LOW STOCK ALERT  │
├──────────────────────┤
│                      │
│  🔴 ကြာဇံ            │
│     Stock: 0         │
│     Threshold: 10    │
│                      │
│  🟠 ကော်ဖီမစ်         │
│     Stock: 5         │
│     Threshold: 20    │
│                      │
│  🟠 နို့ဆီ            │
│     Stock: 8         │
│     Threshold: 15    │
│                      │
└──────────────────────┘
```

</td>
</tr>
</table>

### 📲 Notification Settings

| Notification Type        | Description                     |
| ------------------------ | ------------------------------- |
| 🔔 **Push Notification** | Device Notification Bar တွင် ပြ |
| 📊 **In-App Badge**      | App အတွင်း Alert Count ပြ       |
| 📅 **Daily Summary**     | နေ့စဉ် Low Stock Summary        |

---

<br/>

## 🖨️ Printing & Export

### 🧾 Receipt Printing

<table>
<tr>
<td width="50%">

#### Supported Printers

- 🖨️ **Bluetooth Thermal Printers**
  - 58mm POS Printers
  - 80mm POS Printers
  - ESC/POS Compatible

#### Print Content

- Shop Name & Logo
- Date & Time
- Item List with Prices
- Subtotal & Discount
- Tax (if configured)
- Grand Total
- Footer Message

</td>
<td width="50%">

```
┌────────────────────────┐
│    ABC ကုန်စုံဆိုင်      │
│    09-123456789        │
├────────────────────────┤
│ Date: 2026-01-25 14:30 │
│ Receipt: #00123        │
├────────────────────────┤
│ ကြာဇံ x2     5,000 Ks  │
│ ကော်ဖီ x1    2,500 Ks  │
├────────────────────────┤
│ Subtotal:   7,500 Ks   │
│ Discount:    -500 Ks   │
│ Tax (5%):     350 Ks   │
├────────────────────────┤
│ TOTAL:      7,350 Ks   │
├────────────────────────┤
│  ဝယ်ယူမှုအတွက်ကျေးဇူး    │
│    တင်ပါသည်            │
└────────────────────────┘
```

</td>
</tr>
</table>

### 📤 Export Options

<table>
<tr>
<td align="center" width="33%">
<h3>📄</h3>
<strong>PDF Export</strong>
<br/><br/>
Reports များကို PDF ဖိုင်အဖြစ် Export
</td>
<td align="center" width="33%">
<h3>📊</h3>
<strong>Excel Export</strong>
<br/><br/>
Data များကို Excel (.xlsx) ဖိုင်အဖြစ် Export
</td>
<td align="center" width="33%">
<h3>📤</h3>
<strong>Share</strong>
<br/><br/>
Export ထားသော ဖိုင်များကို Share
</td>
</tr>
</table>

---

<br/>

## 💾 Data Management

### 📥 Backup & Restore

<table>
<tr>
<td width="50%">

#### 💾 Local Backup

- Device Storage သို့ Database Backup
- Encrypted Backup File
- Manual Backup Trigger

#### ☁️ Cloud Sync (Optional)

- Supabase Cloud Integration
- Auto Sync (if enabled)
- Cross-device Access

</td>
<td width="50%">

```
┌─────────────────────────┐
│   💾 BACKUP OPTIONS     │
├─────────────────────────┤
│                         │
│  📱 Local Backup        │
│  └── backup_20260125.db │
│                         │
│  ☁️ Cloud Sync          │
│  └── Last: 2 hours ago  │
│                         │
│  [💾 Backup Now]        │
│  [📥 Restore]           │
│                         │
└─────────────────────────┘
```

</td>
</tr>
</table>

### 🗑️ Data Reset

| Reset Type           | Description                        | Warning        |
| -------------------- | ---------------------------------- | -------------- |
| 📊 **Reset Sales**   | ရောင်းချမှုမှတ်တမ်းများ ဖျက်       | ⚠️ Cannot Undo |
| 📦 **Reset Stock**   | Stock data အားလုံး ဖျက်            | ⚠️ Cannot Undo |
| 🗑️ **Factory Reset** | Data အားလုံး ဖျက်၍ အစပိုင်းအတိုင်း | ⚠️ Cannot Undo |

---

<br/>

## 🔐 Security Features

<table>
<tr>
<td width="50%">

### 🔒 Database Encryption

- **SQLCipher** ဖြင့် Database ကို Encrypt
- Data များကို လုံခြုံစွာ သိမ်းဆည်း
- Password Protection

### 🔑 Secure Storage

- Sensitive Data များကို Flutter Secure Storage တွင် သိမ်း
- API Keys, Passwords etc.

</td>
<td width="50%">

### 📱 Device Security

- Root/Jailbreak Detection
- Emulator Detection
- Debug Mode Detection

### 🔐 Access Control

- PIN Lock (Optional)
- Void Sale Authentication
- Settings Protection

</td>
</tr>
</table>

---

<br/>

## 🛠️ System Architecture

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                         🏗️ SYSTEM ARCHITECTURE                              │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  ┌─────────────────────────────────────────────────────────────────────┐   │
│  │                        📱 PRESENTATION LAYER                         │   │
│  │  ┌──────────┐ ┌──────────┐ ┌──────────┐ ┌──────────┐ ┌──────────┐  │   │
│  │  │   POS    │ │  Items   │ │  Stock   │ │ Reports  │ │ Settings │  │   │
│  │  │  Screen  │ │  Screen  │ │  Screen  │ │  Screen  │ │  Screen  │  │   │
│  │  └────┬─────┘ └────┬─────┘ └────┬─────┘ └────┬─────┘ └────┬─────┘  │   │
│  └───────┼────────────┼────────────┼────────────┼────────────┼────────┘   │
│          │            │            │            │            │            │
│  ┌───────┴────────────┴────────────┴────────────┴────────────┴────────┐   │
│  │                         🎮 STATE MANAGEMENT                         │   │
│  │                           (BLoC Pattern)                            │   │
│  │   ┌─────────┐ ┌─────────┐ ┌─────────┐ ┌─────────┐ ┌─────────┐     │   │
│  │   │ POSBloc │ │ItemBloc │ │StockBloc│ │ReportBloc│ │SettBloc│     │   │
│  │   └────┬────┘ └────┬────┘ └────┬────┘ └────┬────┘ └────┬────┘     │   │
│  └────────┼───────────┼───────────┼───────────┼───────────┼──────────┘   │
│           │           │           │           │           │              │
│  ┌────────┴───────────┴───────────┴───────────┴───────────┴──────────┐   │
│  │                        💼 DOMAIN LAYER                             │   │
│  │                     (Use Cases, Entities)                          │   │
│  └────────────────────────────────┬──────────────────────────────────┘   │
│                                   │                                      │
│  ┌────────────────────────────────┴──────────────────────────────────┐   │
│  │                          💾 DATA LAYER                             │   │
│  │   ┌───────────────┐    ┌───────────────┐    ┌───────────────┐    │   │
│  │   │  Repositories │    │     DAOs      │    │   Database    │    │   │
│  │   │               │───▶│    (Drift)    │───▶│  (SQLCipher)  │    │   │
│  │   └───────────────┘    └───────────────┘    └───────────────┘    │   │
│  └───────────────────────────────────────────────────────────────────┘   │
│                                                                          │
│  ┌───────────────────────────────────────────────────────────────────┐   │
│  │                        ☁️ EXTERNAL SERVICES                        │   │
│  │   ┌─────────┐    ┌─────────┐    ┌─────────┐    ┌─────────┐       │   │
│  │   │ Supabase│    │Bluetooth│    │ Camera  │    │  Files  │       │   │
│  │   │  Cloud  │    │ Printer │    │ Scanner │    │ Storage │       │   │
│  │   └─────────┘    └─────────┘    └─────────┘    └─────────┘       │   │
│  └───────────────────────────────────────────────────────────────────┘   │
│                                                                          │
└─────────────────────────────────────────────────────────────────────────┘
```

---

<br/>

## 📱 System Requirements

<table>
<tr>
<td width="50%">

### 📲 Minimum Requirements

| Requirement     | Value               |
| --------------- | ------------------- |
| Android Version | 5.0 (Lollipop) +    |
| RAM             | 2 GB                |
| Storage         | 100 MB              |
| Camera          | For Barcode Scanner |

</td>
<td width="50%">

### ✨ Recommended

| Requirement     | Value               |
| --------------- | ------------------- |
| Android Version | 10.0 +              |
| RAM             | 4 GB                |
| Storage         | 500 MB              |
| Bluetooth       | For Thermal Printer |

</td>
</tr>
</table>

---

<br/>

## 📝 Version History

<table>
<tr>
<th>Version</th>
<th>Date</th>
<th>Changes</th>
</tr>
<tr>
<td><strong>v1.0.3</strong></td>
<td>2026-01-25</td>
<td>
✅ Currency Settings<br/>
✅ Tax Configuration<br/>
✅ Stock Alerts Enhancement<br/>
✅ Bug Fixes
</td>
</tr>
<tr>
<td><strong>v1.1.0-fifo</strong></td>
<td>2026-01-18</td>
<td>
✅ FIFO Stock Tracking<br/>
✅ Transaction Integrity<br/>
✅ Void Sale with Stock Restoration<br/>
✅ FIFO Cost Report
</td>
</tr>
<tr>
<td><strong>v1.0.0</strong></td>
<td>2026-01-17</td>
<td>
🎉 Initial Release<br/>
✅ Basic POS<br/>
✅ Item/Category Management<br/>
✅ Sales History
</td>
</tr>
</table>

---

<br/>

<div align="center">

## 📞 Contact & Support

<table>
<tr>
<td align="center">
<h3>📧</h3>
<strong>Email</strong>
<br/>
sainmhat@gmail.com
</td>
<td align="center">
<h3>🐛</h3>
<strong>Bug Reports</strong>
<br/>
GitHub Issues
</td>
<td align="center">
<h3>💡</h3>
<strong>Feature Requests</strong>
<br/>
GitHub Discussions
</td>
</tr>
</table>

---

<br/>

<p>
  <strong>Made with ❤️ for Myanmar Small Businesses</strong>
</p>

<p>
  <img src="https://img.shields.io/badge/🇲🇲-Myanmar-red?style=for-the-badge" alt="Myanmar"/>
</p>

<br/>

**✨ ဆိုင်မှတ် - သင့်ဆိုင်အတွက် ယုံကြည်စိတ်ချရသော POS ✨**

---

<sub>© 2026 Sain Mhat. All Rights Reserved.</sub>

</div>
