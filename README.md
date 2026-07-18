# 💻 ThinkCentre M73 / NEC4 黑苹果 EFI 引导

本仓库提供联想 ThinkCentre M73 及同配置 NEC4 的黑苹果 OpenCore (OC) 引导配置文件。

---

## 🖥️ 硬件配置清单 (Specifications)

* **电脑型号**：联想 ThinkCentre M73 / NEC4 (H81 主板)
* **处理器**：Intel 4代 Haswell 核心（对应驱动）
* **显卡**：Intel HD Graphics 4600 (核显)
* **网卡/蓝牙**：博通 BCM94352HMB (半高 mini-PCIe)

---

## ⚠️ 食用前必看 (Important)

* **已移除三码**：为了隐私与安全，已移除 `MLB`、`SystemSerialNumber` 和 `SystemUUID`。
* **自行添加**：请在部署前使用 OpenCore Configurator 或 ProperTree 生成并填入你的**三码**，否则无法激活 iCloud/iMessage 等服务。

---

## 🛠️ 驱动状态与避坑指南 (Status)

| 硬件组件 | 驱动状态 | 详细说明 |
| :--- | :--- | :--- |
| **🎨 Intel HD4600** | 🟢 正常驱动 | 核显完美内驱，支持视频硬解。 |
| **💤 睡眠与唤醒** | 🟢 正常驱动 | 睡眠正常。 |
| **📶 BCM94352HMB** | 🟢 完美工作 | 蓝牙、Wi-Fi、**隔空投送 (Airdrop)** 与接力功能均完美。 |

### 🛑 高版本 macOS 特别说明（Monterey 及之后）
由于 Apple 删除了对 Haswell 核显及部分博通网卡的原生支持：
1. **必须使用 OCLP**：安装完 macOS Monterey / Ventura / Sonoma / Sequoia 后，必须运行 **OpenCore Legacy Patcher (OCLP)**。
2. **打补丁**：通过 OCLP 注入 **Graphics: Haswell** 和 **Networking: Broadcom** 补丁，才能恢复核显加速和 Wi-Fi 蓝牙功能。

---

## 🌟 觉得好用？
就酱！既然都免费白嫖成功了，走过路过不要忘记点个 **Star (星星) ✨** 支持一下作者！
