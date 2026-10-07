# 🎮 Cosmetics to QMod Converter

Convert Beat Saber cosmetics files (sabers, avatars, platforms, blocks) into `.qmod` format for Meta Quest 1.40.0+

![License](https://img.shields.io/badge/license-MIT-blue)
![Platform](https://img.shields.io/badge/platform-Windows-brightgreen)
![Version](https://img.shields.io/badge/version-1.0.0-orange)

## 📥 [DOWNLOAD APP](https://github.com/abeatsabermodmaker228/Cosmetics-to-QMod-Converter/releases/download/v1.0.0/QmodCosmetics.exe) 📥

---

## 🚀 Features

- ✅ Drag & Drop Support
- ✅ Auto-Detection of sabers, avatars, platforms, blocks
- ✅ Automatic `manifest.json` generation
- ✅ Beat Saber Quest 1.40.0 target
- ✅ Converts `*.glb` and other asset files into `.qmod`
- ✅ Standalone Windows executable

---

## 📋 What It Does

Takes a folder like this:

```text
MyCosmetics/
├── sabers/
│   └── NeonSaber.glb
├── avatars/
│   └── CuteAvatar.glb
├── platforms/
│   └── RainbowPlatform.glb
├── blocks/
│   └── FireBlock.glb
└── README.md
```

And packages it into a `.qmod` file with a valid structure:

```text
MyCosmetics.qmod
├── manifest.json
└── cosmetics/
    ├── sabers/NeonSaber.glb
    ├── avatars/CuteAvatar.glb
    ├── platforms/RainbowPlatform.glb
    └── blocks/FireBlock.glb
```

---

## 🎯 How to Use

### Command-line usage
```bash
QmodCosmetics.exe "C:\path\to\cosmetics\folder"
```

### Advanced usage
```bash
QmodCosmetics.exe "C:\cosmetics" "C:\output\MyMod.qmod" "MyMod" "1.0.0" "YourName" "Custom Quest cosmetics"
```

---

## 📁 Folder Structure Requirements

Place files inside these folder names:

```text
YourModFolder/
├── sabers/
├── avatars/
├── platforms/
├── blocks/
└── optional extra files
```

The app detects those folder names automatically.

---

## 📝 Generated Manifest Example

```json
{
  "id": "com.yourname.mymod",
  "name": "My Cosmetics Pack",
  "version": "1.0.0",
  "description": "Custom Beat Saber cosmetics",
  "author": "Your Name",
  "gameVersion": "1.40.0",
  "modFormatVersion": 2,
  "cosmetics": [
    {
      "type": "saber",
      "path": "cosmetics/sabers/NeonSaber.glb",
      "name": "NeonSaber"
    },
    {
      "type": "avatar",
      "path": "cosmetics/avatars/CuteAvatar.glb",
      "name": "CuteAvatar"
    }
  ]
}
```

---

## 🔧 Build from Source

### Prerequisites
- .NET 8 SDK
- Windows 10/11

### Build
```bash
git clone https://github.com/abeatsabermodmaker228/Cosmetics-to-QMod-Converter.git
cd Cosmetics-to-QMod-Converter
dotnet build -c Release
```

Your executable will be created here:
```text
bin/Release/net8.0/QmodCosmetics.exe
```

---

## ⚠️ Important Notes

1. This tool packages cosmetic assets into a valid `.qmod` archive.
2. The asset itself still needs to be compatible with the Beat Saber Quest content format.
3. The generated manifest targets Beat Saber Quest **1.40.0**.
4. If your game version differs, update the manifest manually.

---

## 📄 License

MIT License

---

## 🤝 Contributing

Open an issue or submit a pull request if you want to improve the tool.

---

**Made for the Beat Saber modding community**
