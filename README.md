# ⛽ Alisizm Fuel 

[![Tebex](https://img.shields.io/badge/Purchase-Tebex-orange?style=for-the-badge&logo=tebex)](https://alisizm.tebex.io/category/3229334)
[![YouTube](https://img.shields.io/badge/Showcase-YouTube-red?style=for-the-badge&logo=youtube)](https://www.youtube.com/watch?v=-nzuRk5Ordw&t=1s)

Alisizm Fuel is a modern, highly optimized, multi-framework fuel and charging system for FiveM servers. It seamlessly handles both gasoline and electric vehicles in one unified workflow, featuring a dynamic holographic refuel UI and a strict focus on low resource consumption (resmon).

---

## 🔗 Links
* **🛒 Purchase:** [Tebex Store](https://alisizm.tebex.io/category/3229334)
* **🎥 Showcase Video:** [YouTube](https://www.youtube.com/watch?v=-nzuRk5Ordw&t=1s)

---

## ✨ Key Features
* **Unified System:** Full support for both gas and electric vehicles (EV).
* **Interactive Workflow:** Complete nozzle mechanics (take, attach to vehicle, fill, return).
* **Electric Charging:** Includes EV charging station and charging gun support.
* **Holographic UI:** Dynamic, world-space fueling panel displayed near the vehicle.
* **Advanced Billing:** Partial refuel billing (pay only for what was dispensed) and safe fuel reversion if a payment fails.
* **Player Control:** Player is locked during fueling, with the ability to cancel anytime using the `(X)` key.
* **Optional TextUI ('E' Key) Support:** Can be configured to work with standard 'E' keypresses (TextUI/DrawText) for servers that do not want to use target systems.
* **Backward Compatibility:** Export/Event bridge available for LegacyFuel-style scripts.
* **Smart EV Detection:** Uses native detection, handling fallbacks, and manual model list support.

### ⚙️ Framework & Integration Support
| Frameworks | Target / Interaction Systems |
| :--- | :--- |
| ✔️ Qbox | ✔️ `ox_target` |
| ✔️ QB-Core | ✔️ `qb-target` |
| ✔️ ESX | ✔️ `qtarget` |
| | ✔️ Custom target adapter mode |
| | ✔️ **TextUI / Keypress ('E') Mode** |

### 💾 Persistent Fuel System
Fuel states are securely stored in the `alisizm_fuel_state` SQL table based on vehicle plates.
* Loads fuel state upon entering a vehicle.
* Periodically auto-saves while driving.
* Saves upon exiting the vehicle, session end, or resource stop.
* Garage-friendly compatibility for `player_vehicles` / `owned_vehicles` fuel fields.

### 🌍 Localization
Multi-language support configured easily via `Config.Locale`. Supported languages include:
`EN` | `TR` | `ES` | `DE` | `FR` | `RU` | `PT` | `IT` | `PL` | `RO`

### 🚀 Performance & Security
* **Low Resmon:** Optimized thread intervals and logic loops that only run when necessary.
* **Prop Logic:** Ground placement logic for charging props with delayed collision handling.
* **Resource Protection:** The script enforces the resource name (`alisizm-fuel`). Renaming blocks runtime and generates a console warning.

> **Tebex Package Notes:** 
> The script is Escrow-ready. The `config.lua` and `locales/*.lua` files remain fully editable, allowing server owners to easily customize settings and translations.

---
---

# ⛽ Alisizm Fuel (Türkçe)

Alisizm Fuel, FiveM sunucuları için geliştirilmiş modern, optimize ve çok framework destekli bir yakıt/şarj sistemidir. Benzinli ve elektrikli araçları tek bir sistemde yönetir, gerçek zamanlı holografik dolum paneli sunar ve düşük resmon hedefiyle çalışır.

## 🔗 Bağlantılar
* **🛒 Satın Al:** [Tebex Mağazası](https://alisizm.tebex.io/category/3229334)
* **🎥 Tanıtım Videosu:** [YouTube](https://www.youtube.com/watch?v=-nzuRk5Ordw&t=1s)

---

## ✨ Öne Çıkan Özellikler
* **Tek Sistem:** Benzinli ve elektrikli araçlar için birleştirilmiş yakıt sistemi.
* **Etkileşimli Akış:** Nozzle (tabanca) alma, araca takma, dolum ve geri bırakma mekaniği.
* **Elektrikli Araç (EV) Desteği:** Elektrikli araç şarj istasyonu ve şarj tabancası içerir.
* **Holografik Arayüz:** Araç yanında dinamik olarak beliren world-space dolum paneli.
* **Gelişmiş Ödeme:** Kısmi dolumda sadece kullanılan kadar ücret alma ve yetersiz bakiye durumunda yakıt geri alma (revert) koruması.
* **Karakter Kontrolü:** Dolum sırasında karakter kilidi ve iptal `(X)` desteği.
* **İsteğe Bağlı 'E' Tuşu (TextUI) Desteği:** Target sistemi kullanmak istemeyen sunucular için standart 'E' tuşu (TextUI/DrawText) ile etkileşim seçeneği.
* **Geriye Dönük Uyumluluk:** LegacyFuel benzeri scriptlerle uyumluluk için export/event köprüsü.
* **Akıllı EV Tespiti:** Native kontrol, handling fallback ve manuel model listesi desteği.

### ⚙️ Framework ve Target Desteği
| Framework | Target / Etkileşim Sistemleri |
| :--- | :--- |
| ✔️ Qbox | ✔️ `ox_target` |
| ✔️ QB-Core | ✔️ `qb-target` |
| ✔️ ESX | ✔️ `qtarget` |
| | ✔️ Custom target (adapter mantığı) |
| | ✔️ **TextUI / 'E' Tuşu ile Etkileşim** |

### 💾 Kalıcı Yakıt Sistemi (Persistence)
Plaka bazlı kayıtlar `alisizm_fuel_state` tablosunda güvenle tutulur.
* Araca binerken yakıt verisini yükleme.
* Sürüş sırasında periyodik otomatik kayıt.
* Araçtan inince, işlem bitince veya script kapanışında son yakıtı kaydetme.
* Garage uyumluluğu için `player_vehicles` / `owned_vehicles` yakıt kolon desteği.

### 🌍 Çoklu Dil Sistemi
`Config.Locale` üzerinden aktif dili kolayca seçebilirsiniz. Desteklenen diller:
`EN` | `TR` | `ES` | `DE` | `FR` | `RU` | `PT` | `IT` | `PL` | `RO`

### 🚀 Performans ve Güvenlik
* **Düşük Resmon:** Sadece gerektiğinde aktif çalışan kontrol döngüleri ve optimize thread aralıkları.
* **Prop Mantığı:** Şarj prop zemin oturtma ve geç yüklenen collision için optimize yaklaşım.
* **İsim Koruması:** Resource adı `alisizm-fuel` olmazsa script çalışmayı durdurur ve konsol uyarısı verir.

> **Tebex Paket Notu:** 
> Escrow yapılandırması hazırdır. `config.lua` ve `locales/*.lua` açık bırakılacak şekilde ayarlanmıştır; sunucu sahipleri ayarları ve çevirileri dilediği gibi düzenleyebilir.
